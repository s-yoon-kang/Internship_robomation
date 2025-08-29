# [Draw Diagram]

**해당 문서는 Raccoon의 테스트 예제 설명 문서입니다.**

***


#### [하드웨어 설명](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/%EB%9D%BC%EC%BF%A4-%ED%95%98%EB%93%9C%EC%9B%A8%EC%96%B4-%EC%84%A4%EB%AA%85)

#### [블록 컴포저 바로가기](https://robomationlab.com/BlockComposer/)
  
#### [로보메이션 깃허브 바로가기](https://github.com/RobomationLAB)

#### [초보자를 위한 블록컴포저 환경설정 가이드](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/%EB%B8%94%EB%A1%9D%EC%BB%B4%ED%8F%AC%EC%A0%80-%ED%99%98%EA%B2%BD-%EC%84%A4%EC%A0%95-%EA%B0%80%EC%9D%B4%EB%93%9C)


---

Raccoon이 사용자의 입력에 따라 다양한 도형을 그리는 예제입니다.
<br>
그릴 수 있는 도형으로 **원**, **세모**, **네모**, **하트**, **별**이 있습니다.
<br>

  ![Image](https://github.com/user-attachments/assets/c625a0af-eaa8-454f-b5a1-95d9c94f1b13) ![Image](https://github.com/user-attachments/assets/c625a0af-eaa8-454f-b5a1-95d9c94f1b13) ![Image](https://github.com/user-attachments/assets/c625a0af-eaa8-454f-b5a1-95d9c94f1b13)

<br><br>


---


## 1. 준비물
[*예제 파일 다운로드*](https://www.dropbox.com/scl/fi/f0rkememc39vpk95tmla7/Raccoon_-_.block?rlkey=1dmg1zew13hdg66i8yact50ib&st=hj2ks7rr&dl=0)

| 제품명(수량) | 이미지 | 제품명(수량) | 이미지 | 
| :---: | :---: | :---: | :---: |
| Raccoon<br> (1개) | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/912bd02f-ecae-4c8c-b7e6-5f952edaa7d3" /> | 펜홀더 말단 장치<br> (1개) | <img width="50" alt="Image" src="https://github.com/user-attachments/assets/adead6a0-2cdd-4fe7-bb95-6e4d01383b48" /> |
| 종이<br> (1장) | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/0368e458-8751-4248-b69d-816506472443" /> | Block Composer | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/f06909aa-91f6-4f47-8c4d-2a0044d99c49" /> |

  
<br><br>


---


## 2. 초기 환경 구성
- 그림을 그릴 수 있는 **종이(A4 이상)** 를 **평평한 바닥**에 놓습니다.

  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/e0614823-5dff-40e6-9a14-5afd0eba123d" />


<br><br>

- 종이 위 **끝 부분**에 Raccoon을 올려 종이가 움직이는 것을 방지합니다.

  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/ed37a779-8a0a-44f0-9529-131b742b1282" />


<br><br>


---


## 3. 작동하기
- 오른쪽 위 **실행 버튼**을 클릭합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/0cf13804-c040-4d9b-afaa-e38ec4421d24" />


<br><br>

- 그리고 싶은 **도형의 이름**을 입력합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/838f5166-764c-40c3-9d02-a4d545c758dd" />


<br><br>

- Raccoon의 **준비 자세**가 끝나면 **Space**를 눌러 도형 그리기를 시작합니다.

  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/70aecb38-53a6-4050-9921-4a62352da8ab" />
  

<br><br>


| 도형 <br> (이름) | 원 (동그라미) | 삼각형 (세모) | 사각형 (네모) | 하트 | 별 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 이미지 | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/9a05bb05-3b66-4610-bbcb-ed96bbe416c6" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/8749847e-6b83-4c88-ba03-b9abca48a39c" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/f32ae16d-c0f3-4561-b559-6e69b3d97abc" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/fdfc9681-e1ed-4bb2-aa3d-66e3d2d9179a" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/90308509-576a-480c-b1fe-eaa6fc5e2253" /> |


<br><br>


---


## ~~4. 오류 발생시 해결 방법~~
- ~~발생 가능한 오류에 대해서 적어두는 란 입니다.~~

<br><br>


---


## 5. 작동 알고리즘
- 사용자가 원하는 **도형**을 입력하면 **변수 user**에 저장됩니다.


<br>

- 도형에 따라 **초기 설정**을 수행합니다.


<br>

- **각도 제어 모드**로 초기 **준비 자세** 이동 후 **속도 제어 모드**로 변경합니다.


<br>

- **Space**를 누르면 입력한 도형에 따라 **그리기 함수**를 **반복**합니다.


<br><br>


---


## 6. 코드 설명
<details>
<summary><b>시작하기():</b></summary>
    
- Raccoon의 **초기 설정**을 수행합니다.

  ![Image](https://github.com/user-attachments/assets/44701304-51aa-448f-b307-cea0ab342876)


<br><br>

- 사용자에게 그림을 그릴 **도형의 이름**을 입력 받습니다.

  ![Image](https://github.com/user-attachments/assets/2c8d4219-fdb1-4d95-8711-18914b918b9b)


<br><br>

- 입력 받은 도형에 따라 **초기 설정**을 수행합니다.
  - **원**: **시작 위치(220, 0)** 를 설정하고 **각도를 0**으로 초기화 합니다.
  
    ![Image](https://github.com/user-attachments/assets/8b10d9e3-1712-487b-8337-af3559c21eb2)
    
    <br>
    
  - **하트**: **시작 위치(165, 0)** 를 설정하고 **각도를 0**으로 초기화 합니다.
      
    ![Image](https://github.com/user-attachments/assets/584d7593-9c35-44ef-b98d-af4a19ceb2bb)
    
    <br>
    
  - **삼각형**: 삼각형의 **세 꼭짓점**을 **배열**로 지정하고 순차적으로 가져옵니다.
      
    ![Image](https://github.com/user-attachments/assets/c5f293c2-f8cb-4d36-ba94-adfaeb2331f2)
    
    <br>
    
  - **사각형**: 사각형의 **네 꼭짓점**을 **배열**로 지정하고 순차적으로 가져옵니다.
      
    ![Image](https://github.com/user-attachments/assets/05e948e2-29e6-4758-aaf9-f587f8ccc7ff)
    
    <br>
    
  - **별**: 별의 **다섯 꼭짓점**을 **배열**로 지정하고 순차적으로 가져옵니다.
      
    ![Image](https://github.com/user-attachments/assets/c4e7bb56-43b2-4bb2-a902-a97a28baea37)
    
    <br>
    


<br><br>

- 초기 **준비 자세**로 이동합니다.
  
  ![Image](https://github.com/user-attachments/assets/ee94176d-6df1-4cf4-8a43-d68db8be0ac0)


<br><br>

- **P 제어**를 위해 **속도 제어 모드**로 설정합니다.
  
  ![Image](https://github.com/user-attachments/assets/f24736b9-bb29-4730-9e4e-81c9e03d797c)
  

<br><br>

- **관절의 속도**를 **0으로 초기화** 합니다.
  
  ![Image](https://github.com/user-attachments/assets/03990976-7869-4dca-bc4a-be15e9854b12)


<br><br>


</details>


<br>


---


<details>
<summary><b>무한 반복하기():</b></summary>
    
    
- 만약 **Space 키**가 눌렸다면, 사용자의 **입력에 따른 도형**을 그립니다.

  ![Image](https://github.com/user-attachments/assets/3238ca37-64c2-4c93-bdb2-26b7d5c5dfcb)


<br><br>


</details>


<br>


---


<details>
<summary><b>함수</b></summary>

<br>

<details>
<summary><i>역기구학</i></summary>

<br>

- **좌표**에 따른 관절의 **각도**를 계산하는 함수입니다.

  ![Image](https://github.com/user-attachments/assets/c8d3413c-ca40-4ec3-addc-b39e56f6108a)


<br><br>

</details>

<br>

<details>
<summary><i>circle(원)</i></summary>

<br>

- **원의 방정식**을 이용해 **P 제어**로 원을 그리는 함수입니다.

  ![Image](https://github.com/user-attachments/assets/3c715a2d-bedd-4d14-8c78-5a02c67bdc7b)

원점: $$(a, b) = (170, 0)$$

반지름: $$r = 50$$

$$x =  a + r \cos(\theta)$$

$$y =  b + r \sin(\theta)$$

$$z =  -20$$


<br><br>

</details>

<br>

<details>
<summary><i>heart(하트)</i></summary>

<br>

- **하트 방정식**을 이용해 **P 제어**로 하트 그리는 함수입니다.

  ![Image](https://github.com/user-attachments/assets/9d73c5ba-b346-49f8-8b0b-b2fc60f99a85)

원점: $$(a, b) = (150, 0)$$

배율: $$A = 3$$

$$x =  a + A (((13 \cos(\theta) - 5 \cos(2 \theta)) - 2 \cos(3 \theta)) - \cos (4 \theta))$$

$$y =  A (16(\sin(\theta)^3))$$

$$z =  -20$$


<br><br>


</details>

<br>

<details>
<summary><i>triangle(삼각형)</i></summary>

<br>

- **삼각형 꼭짓점 배열**을 가지고 **선형 보간법**을 이용해 **점과 점 사이를 잇는 직선**을 그립니다.

  ![Image](https://github.com/user-attachments/assets/25e1383d-e80a-40c1-b782-50f2b8f27469)


<br><br>

</details>

<br>

<details>
<summary><i>rectangle(사각형)</i></summary>

<br>

- **사각형 꼭짓점 배열**을 가지고 **선형 보간법**을 이용해 **점과 점 사이를 잇는 직선**을 그립니다.

  ![Image](https://github.com/user-attachments/assets/cee89d7e-6f16-4cf5-b4b1-307fab7b0a70)


<br><br>

</details>

<br>

<details>
<summary><i>star(별)</i></summary>

<br>

- **별 꼭짓점 배열**을 가지고 **선형 보간법**을 이용해 **점과 점 사이를 잇는 직선**을 그립니다.

  ![Image](https://github.com/user-attachments/assets/50a36b73-ed74-4922-a454-9905cc585aa9)


<br><br>

</details>

</details>

<br>


---


## 7. 관련 내용

[4DoF Kinematics](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/4Dof-Kinematics(%EA%B8%B0%EA%B5%AC%ED%95%99))

[P 제어 이론](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/P-%EC%A0%9C%EC%96%B4(%EB%B9%84%EB%A1%80-%EC%A0%9C%EC%96%B4))

<br>

<img width="10000000" alt="Image" src="https://github.com/user-attachments/assets/aececf51-c059-4081-9fa8-87de0162b0b0" />

<br><br>
