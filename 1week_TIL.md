![image](https://github.com/user-attachments/assets/ba930821-89d9-41fc-a01d-6c095a5dadd2)



# 데이터 탐색(SELECT, FROM, WHERE)

## 포켓몬으로 SELECT 이해하기
![image](https://github.com/user-attachments/assets/28517a7c-8b77-4a62-b83c-0d89981198b1)

## Row / Column 구별
----Row----->

↓ col ↓



## SQL 쿼리구조
- SELECT : 테이블의 어떤 컬럼을 선택할 것인가?
- FROM ____ : 어떤 테이블에서 데이터를 확인할 것인가?
- WHERE : 만약 원하는 조건이 있다면?

#### 예시
![image](https://github.com/user-attachments/assets/28e52102-414d-471b-80ce-04bf3233099f)

###### SELECT * FROM: 모든 컬럼을 출력하겠다 -> raw가 많다? 그럼 비추 (돈 듦)
###### SELECT * EXCEPT(제외할 컬럼) : 일부 컬럼을 제외하겠다

## 쿼리 연습
![image](https://github.com/user-attachments/assets/ac77f064-97f4-4e59-b432-542da65ddb2d)

## SQL 문법 핵심 정리
- 쿼리 엔진 실행 순서 : FROM(테이블 위치 확인) > WHERE(필터링할 조건 확인) > SELECT(출력)
###### 단, 순서는 SELECT-FROM-WHERE임!



# SELECT문 연습
#### 1번
![image](https://github.com/user-attachments/assets/8f4edf70-c40f-460f-bfbf-41d2c82318bf)
![image](https://github.com/user-attachments/assets/1ed27dce-7cbb-47b2-be06-b4463b57a845)

#### 2번
![image](https://github.com/user-attachments/assets/83b494d1-73bb-470b-bf29-4586d1064615)
![image](https://github.com/user-attachments/assets/07a2614c-d08b-46ba-9456-1d1c6a5fb52b)

#### 3번
![image](https://github.com/user-attachments/assets/c668d71a-10b3-4a5c-894a-f1c7ba078f39)
![image](https://github.com/user-attachments/assets/fb291247-f956-415a-bb2a-3ce6af52edaa)

#### 4번
![image](https://github.com/user-attachments/assets/39e9fab7-838e-427d-b37a-a92adb82299c)
![image](https://github.com/user-attachments/assets/b71f2769-76e1-4d1d-8360-cfbb5fa6eb33)

#### 5번
![image](https://github.com/user-attachments/assets/5eb7aff5-cbbe-4440-8910-7ae887e384c9)
![image](https://github.com/user-attachments/assets/266a91e3-ee24-4686-b85c-fb946574ddb0)


# 데이터 탐색 : 요약(집계, 그룹화)
## COUNT, DISTINCT, GROUP BY
#### 집(모아서) 계(계산하다) = 그룹화해서 계산하다
#### GROUP BY : 같은 값끼리 모아서 그룹화한다 (ex. 색상기준으로 모은다! -> GROUP BY 색상)
#### 집계 함수 종류
![image](https://github.com/user-attachments/assets/239cc8ee-2af7-4db1-8bf7-cc98c541f7a0)

#### DISTINCT : 여러값 중에 고유값을 알고 싶은 경우

## 연습문제
![image](https://github.com/user-attachments/assets/7785c954-77a7-4855-84d9-1b8e03a3d06e)
![image](https://github.com/user-attachments/assets/078a0457-226c-4324-be7a-1c3f25812334)

![image](https://github.com/user-attachments/assets/987c5fc7-ee01-4bbc-ad94-668b55e80125)
![image](https://github.com/user-attachments/assets/0f35db7d-c800-49e6-8889-d3963fb1255c)

## 응용
![image](https://github.com/user-attachments/assets/c7f5c3db-dabc-4c84-8a83-1f795eebab0c)

## 조건설정(WHERE, HAVING)
### WHERE : Table에 바로 조건 설정하고 싶은 경우 (집계 전)
### HAVING : GROUP BY한 후에 조건 설정하고 싶은 경우 (집계 후)
![image](https://github.com/user-attachments/assets/1ee09ddc-ed7e-4376-84fc-6a07800158ea)
##### 둘이 같이 쓸 수도 있음

## 서브 쿼리
### SELECT문 안에 존재하는 SELECT 쿼리
- FROM 절에 또 다른 SELECT문을 넣을 수 있음
- 괄호로 묶어서 사용

## 정렬하기 : ORDER BY<컬럼><순서>
### DESC(내림차순), OSC(오름차순_보통 디폴트)
- 쿼리의 맨 마지막에 작성함

## 출력 개수 제한하기 : LIMIT
### 쿼리문의 결과 Row 수를 제한하고 싶을 때 사용
- 이 역시 쿼리문의 제일 마지막에 작성(그 위에 ORDER BY)


![image](https://github.com/user-attachments/assets/8adeb0d9-ce67-49ba-8713-86b4dfe85538)
![image](https://github.com/user-attachments/assets/3f10ec99-e385-46e4-a0d2-d248fe117b06)

## 마무리 요약
![image](https://github.com/user-attachments/assets/6517eee6-62b9-4292-b2c6-bdf7aad4ad2f)
![image](https://github.com/user-attachments/assets/fe27f13b-9508-4291-919b-ae0c647c11f0)


  

