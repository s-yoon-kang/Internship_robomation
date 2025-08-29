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

  ![Image](https://github.com/user-attachments/assets/d049f383-0312-46b3-8663-1aba726f1e6d) ![Image](https://github.com/user-attachments/assets/d049f383-0312-46b3-8663-1aba726f1e6d) ![Image](https://github.com/user-attachments/assets/d049f383-0312-46b3-8663-1aba726f1e6d)
 
<br><br>


---


## 1. 준비물
[*예제 파일 다운로드*](https://www.dropbox.com/scl/fi/f0rkememc39vpk95tmla7/Raccoon_-_.block?rlkey=1dmg1zew13hdg66i8yact50ib&st=hj2ks7rr&dl=0)

| 제품명(수량) | 이미지 | 제품명(수량) | 이미지 | 
| :---: | :---: | :---: | :---: |
| Raccoon<br> (1개) | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/6aed75da-3092-4295-9ef7-e8956efa5bae" /> | 펜홀더 말단 장치<br> (1개) | <img width="50" alt="Image" src="https://github.com/user-attachments/assets/0f4d20b6-66ca-44e2-af8a-eda52755e7d6" /> |
| 종이<br> (1장) | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/3c9e969b-1786-42a1-9977-0cd97f44d07a" /> | Block Composer | <img width="200" alt="Image" src="https://github.com/user-attachments/assets/f06909aa-91f6-4f47-8c4d-2a0044d99c49" /> |

  
<br><br>


---


## 2. 초기 환경 구성
- 그림을 그릴 수 있는 **종이(A4 이상)** 를 **평평한 바닥**에 놓습니다.

  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/d74f4bb8-999d-4f8a-8866-d8ac4dcae60f" />


<br><br>

- 종이 위 **끝 부분**에 Raccoon을 올려 종이가 움직이는 것을 방지합니다.

  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/80ae2c02-982a-4d2e-b676-17014777ff10" />


<br><br>


---


## 3. 작동하기
- 오른쪽 위 **실행 버튼**을 클릭합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/d556d3d1-afde-44cc-99ca-3cd33f6aac8b" />


<br><br>

- 그리고 싶은 **도형의 이름**을 입력합니다.

  <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/625fe4dd-2405-491e-b0b4-23c766d49048" />


<br><br>

- Raccoon의 **준비 자세**가 끝나면 **Space**를 눌러 도형 그리기를 시작합니다.

  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/191c9df5-893a-4139-b4a1-40b8abc711da" />
  

<br><br>


| 도형 <br> (이름) | 원 (동그라미) | 삼각형 (세모) | 사각형 (네모) | 하트 | 별 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 이미지 | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/e4bb6d7d-51ae-46f8-bbc0-cbc3b0d1058b" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/df64d4d0-d80b-49cd-95aa-5605cbb50b6d" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/c00faed6-1256-457c-9b39-adf186ddb9bc" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/475c97ad-a669-4231-a44f-5f722f535ccb" /> | <img width="150" alt="Image" src="https://github.com/user-attachments/assets/b116c396-5cfd-405a-9937-7451ce357c4d" /> |


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

  ![Image](https://github.com/user-attachments/assets/c5655888-0d0c-4064-a68f-d58aeaf1c8ec)


<br><br>

- 사용자에게 그림을 그릴 **도형의 이름**을 입력 받습니다.

  ![Image](https://github.com/user-attachments/assets/f3f32a63-2c39-4f9c-8d1e-3df05c0db90f)


<br><br>

- 입력 받은 도형에 따라 **초기 설정**을 수행합니다.
  - **원**: **시작 위치(220, 0)** 를 설정하고 **각도를 0**으로 초기화 합니다.
  
    ![Image](https://github.com/user-attachments/assets/58c2b72f-13fa-4c1c-9b6e-43bc4e7b8149)
    
    <br>
    
  - **하트**: **시작 위치(165, 0)** 를 설정하고 **각도를 0**으로 초기화 합니다.
      
    ![Image](https://github.com/user-attachments/assets/56a6f7a6-3816-43aa-a89f-9add61a3ee58)
    
    <br>
    
  - **삼각형**: 삼각형의 **세 꼭짓점**을 **배열**로 지정하고 순차적으로 가져옵니다.
      
    ![Image](https://github.com/user-attachments/assets/1ff03b65-58d8-4cc9-a234-d998f0449378)
    
    <br>
    
  - **사각형**: 사각형의 **네 꼭짓점**을 **배열**로 지정하고 순차적으로 가져옵니다.
      
    ![Image](https://github.com/user-attachments/assets/b69000f0-46f5-4ae7-932a-6479c7525af4)
    
    <br>
    
  - **별**: 별의 **다섯 꼭짓점**을 **배열**로 지정하고 순차적으로 가져옵니다.
      
    ![Image](https://github.com/user-attachments/assets/25806419-f2d7-414f-948b-75315e36d8af)
    
    <br>
    


<br><br>

- 초기 **준비 자세**로 이동합니다.
  
  ![Image](https://github.com/user-attachments/assets/39e81463-0d94-4b49-88e6-49c92ea9295c)


<br><br>

- **P 제어**를 위해 **속도 제어 모드**로 설정합니다.
  
  ![Image](https://github.com/user-attachments/assets/3b78083e-c5d9-4b54-bc28-c696d397045a)
  

<br><br>

- **관절의 속도**를 **0으로 초기화** 합니다.
  
  ![Image](https://github.com/user-attachments/assets/c452f6c1-5959-4906-b157-4e717a1b89da)


<br><br>


</details>


<br>


---


<details>
<summary><b>무한 반복하기():</b></summary>
    
    
- 만약 **Space 키**가 눌렸다면, 사용자의 **입력에 따른 도형**을 그립니다.

  ![Image](https://github.com/user-attachments/assets/ee190a4a-c9db-45f6-a136-896b6067225e)


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

  ![Image](https://github.com/user-attachments/assets/68602fe9-dc15-435e-b06e-76161b9d2c9f)


<br><br>

</details>

<br>

<details>
<summary><i>circle(원)</i></summary>

<br>

- **원의 방정식**을 이용해 **P 제어**로 원을 그리는 함수입니다.

  ![Image](https://github.com/user-attachments/assets/07eded66-e587-49a3-af23-8c89ef354dd9)

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

  ![Image](https://github.com/user-attachments/assets/48494519-91f7-490f-a782-de757b169873)

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

  ![Image](https://github.com/user-attachments/assets/bebe4b36-eb9f-4ae2-bccb-e7e639ca9d37)


<br><br>

</details>

<br>

<details>
<summary><i>rectangle(사각형)</i></summary>

<br>

- **사각형 꼭짓점 배열**을 가지고 **선형 보간법**을 이용해 **점과 점 사이를 잇는 직선**을 그립니다.

  ![Image](https://github.com/user-attachments/assets/c49b2db6-7f5c-41ed-9003-b3698ad82c29)


<br><br>

</details>

<br>

<details>
<summary><i>star(별)</i></summary>

<br>

- **별 꼭짓점 배열**을 가지고 **선형 보간법**을 이용해 **점과 점 사이를 잇는 직선**을 그립니다.

  ![Image](https://github.com/user-attachments/assets/9fd42382-f5f8-48c1-a768-d67b3d18a4f6)


<br><br>

</details>

</details>

<br>


---


## 7. 관련 내용

[4DoF Kinematics](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/4Dof-Kinematics(%EA%B8%B0%EA%B5%AC%ED%95%99))

[P 제어 이론]([https://github.com/RoboidStudioLAB/Wiki_Image/wiki/P-%EC%A0%9C%EC%96%B4-%EC%9D%B4%EB%A1%A0](https://github.com/RoboidStudioLAB/Wiki_Image/wiki/P-%EC%A0%9C%EC%96%B4(%EB%B9%84%EB%A1%80-%EC%A0%9C%EC%96%B4)))

<br>

<img width="10000000" alt="Image" src="https://github.com/user-attachments/assets/aececf51-c059-4081-9fa8-87de0162b0b0" />

<br><br>
