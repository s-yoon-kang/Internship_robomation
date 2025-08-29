# [4DoF Kinematics]
 

### 기구학이란

- 로봇의 **관절 좌표**와 **공간 배치** 간의 **관계**를 다루는 학문입니다.

<br>
 
이 페이지는 로봇팔의 **각 관절 각도**를 이용해 **말단(End-effector)** 위치를 계산하는 방식인 **Forward Kinematics (순기구학)**,
<br>
로봇팔의 **말단(End-effector)** 위치를 이용해 **각 관절의 각도**를 구하는 방식인 **Inverse Kinematics (역기구학)** 에 대해 기술되어 있습니다.

<br>

본 기술 문서에서는 **말단 장치**를 **수평으로 고정**을 기준으로 **3자유도(3DoF, Degrees of Freedom)** 모델을 우선적으로 분석하였고,
<br>
이후 **말단 장치**의 **링크 길이**를 고려하는 방식으로 해석을 진행하였습니다.

<br><br>

---

### 들어가기에 앞서

- 기구학에서 사용되는 파라미터에 대한 **Raccoon** 로봇팔의 수치는 다음과 같습니다.

| Raccoon | 기구학 |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/5c956b0f-3ee2-40a5-98da-ded7ec94d368" width="600" alt="7_3-1" /> | <img src="https://github.com/user-attachments/assets/17d3bd79-796f-4db8-8b7d-57dabf09db2e" height="300" alt="7_3-2" /> |

* **링크 길이** *(단위: mm)*:
  * $L_1 = 0$  *(xy평면 즉, 원점을 Joint 2로 설정하기 위해 0으로 설정)*
  * $L_2 = 100$
  * $L_3 = 100$
  * $L_4 = 92.5$

<br>

* **관절 각도**:
  * $\theta_1 = Joint 1$
  * $\theta_2 = Joint 2$
  * $\theta_3 = Joint 3$
 
 로봇의 말단은 항상 **지면과 수평**으로 설정합니다.

<br><br>

 ---
 
 ## 1. Forward Kinematics (순기구학)
 
 - **각 관절의 각도**를 기반으로 **말단(End-effector)** 의 좌표를 구하는 과정입니다.
 
| 이미지 | 수식 |
| :---: | --- |
| <img src="https://github.com/user-attachments/assets/17d3bd79-796f-4db8-8b7d-57dabf09db2e" height="400" alt="7_3-2" /> | **Z 좌표**: $$Z = L_1 + L_2 \sin(\theta_2) + L_3 \sin(\theta_2 + \theta_3)$$ <br> **P (수평 거리)**: $$P = L_2 \cos(\theta_2) + L_3 \cos(\theta_2+\theta_3) + L_4$$ <br> **X좌표**: $$X = P \cos(\theta_1)$$ <br> **Y좌표**: $$Y = P \sin(\theta_1)$$ |

<br>

- $P$는 **XY** 평면에서의 거리(팔이 뻗어나간 길이)입니다.
- ​X,Y 좌표: $𝜃_1$은 베이스(기둥)에서의 회전 각도라서, $P$를 단순히 원점 기준으로 회전시킨 결과가 X,Y가 됩니다.
- Z 좌표: 팔이 위아래로 꺾이는 각도 $𝜃_2, 𝜃_3$에 따라 높이가 달라집니다.

<br>

* **최종 정리:**

  $X = (L_2 \cos(\theta_2) + L_3 \cos(\theta_2+\theta_3) + L_4)\cos(\theta_1)$
  <br>
  $Y = (L_2 \cos(\theta_2) + L_3 \cos(\theta_2+\theta_3) + L_4)\sin(\theta_1)$
  <br>
  $Z = L_1 + L_2 \sin(\theta_2) + L_3 \sin(\theta_2+\theta_3)$

<br><br>

 ---
 
## 2.Inverse Kinematics (역기구학)
 
- **말단(End-effector)** 의 **위치 (X,Y,Z)** 를 기반으로 각 관절의 각도를 구하는 과정입니다.

| 과정 | 이미지 | 수식 |
| --- | :---: | --- |
| **$\theta_1$ 계산** <br><br> XY 평면에서의 방향을 결정하는 값 <br> 팔이 어느 방향을 향하고 있는가 | <img src="https://github.com/user-attachments/assets/17d3bd79-796f-4db8-8b7d-57dabf09db2e" height="300" alt="7_3-2" /> |  $$\theta_1 = \text{atan2}(Y, X)$$ |
| **평면 좌표 변환** <br><br> $W$ = XY 평면에서 목표점까지의 수평 거리 <br> $H$ = 목표점의 높이 <br> $H'$ = End-effector를 고려한 목표점의 높이 | <img src="https://github.com/user-attachments/assets/9444fb13-d6f4-4907-894a-c51e8d229e8b" height="200" alt="7_3-3" /> |  $$H = Z, \quad W = \sqrt{X^2 + Y^2}$$ <br> $$H' = H - L_4, \quad W' = W$$ |
| **거리 D 계산 및 $\theta_3$ 계산 (코사인 법칙)** | <img src="https://github.com/user-attachments/assets/5522f899-9c55-426e-b2bc-21c3b8858b9d" width="250" alt="7_3-4" /> | $$D = \sqrt{W'^2 + (H' - L_1)^2}$$ <br> $$\cos(\theta_3) = \frac{L_2^2 + L_3^2 - D^2}{2 L_2 L_3}$$ <br> $$\sin(\theta_3) = \pm \sqrt{1 - (\cos(\theta_3))^2}$$ <br> $$\theta_3 = \text{atan2}(\sin(\theta_3), \cos(\theta_3))$$ |
| **$\theta_2$ 계산** <br><br> $\beta$ = 목표점까지 직선이 이루는 각도 <br> $\alpha$ = $L_2$와 $L_3$이 이루는 각도 | <img src="https://github.com/user-attachments/assets/21f32287-28f6-4697-b248-16e32f756627" width="250" alt="7_3-5" /> | $$\beta = \text{atan2}(H'-L_1, W')$$ <br> $$\cos(\alpha) = \frac{D^2 + L_2^2 - L_3^2}{2 L_2 D}$$ <br> $$\sin(\alpha) = \pm \sqrt{1 - (\cos(\alpha))^2}$$ <br> $$\alpha = \text{atan2}(\sin(\alpha), \cos(\alpha))$$ <br> $$\theta_2 = \beta - \alpha$$ |

<br>

* **최종 정리:**

  $\theta_1 = \text{atan2}(Y, X)$
  <br>
  $\theta_2 = \beta - \alpha$
  <br>
  $\theta_3 = \text{atan2}(\sin(\theta_3), \cos(\theta_3))$

<br><br>
