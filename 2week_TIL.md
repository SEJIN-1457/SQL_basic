![image](https://github.com/user-attachments/assets/55ae0d23-a142-499e-8487-beb4676532d7)


### 포켓몬 중에 type2가 없는 포켓몬의 수를 작성하는 쿼리를 작성하라.

- is NULL (+ AND, OR 사용방법)
- NULL : 아무것도 없는 값 (!= 0, " ")
- '포켓몬의 수'니까 COUNTt 사용
  
![image](https://github.com/user-attachments/assets/46722db5-7cdf-404e-b0f3-9826c4fd3dc1)

### type2가 없는 포켓몬의 type1과 type1의 포켓몬 수를 알려주는 쿼리를 작성해주세요. (단, type1의 포켓몬 수가 큰 순으로 정렬)

- 테이블 : pokemon
- 조건 : type2가 없는 포켓몬
- 컬럼 : type1
- 집계 : '포켓몬 수'니까 COUNT사용
- 정렬 : type1의 포켓몬 수가 큰 순으로 정렬(ORDER BY) -> 내림차순(DESC) => ORDER BY 포켓몬 수 DESC

![image](https://github.com/user-attachments/assets/ee4b6cea-9bb1-4fd7-afdd-dcf784d9ddde)


### type2 상관없이 type1의 포켓몬 수를 알 수 있는 쿼리를 작성해주세요

- 테이블 : pokemon
- 조건 : type2 상관없이 -> 조건인가? 아닌가? => 조건이 아님!
- 컬럼 : type1
- 집계 : '포켓몬 수'니까 COUNT사용

![image](https://github.com/user-attachments/assets/48613d00-119b-4185-ad11-a4f698df179f)
- DISTINCT 개념
![image](https://github.com/user-attachments/assets/d8620f8c-9e6b-4785-8cd9-582cf07ad8d1)


### 전설 여부에 따른 포켓몬 수를 알 수 있는 쿼리를 작성해주세요

- 테이블 : pokemon
- 조건 : 전설 여부? => 조건 아님. 컬럼
- 컬럼 : 전설(is_legendary)
- 집계 : 포켓몬 수

 ![image](https://github.com/user-attachments/assets/7a6d714a-ed36-4413-8cc5-ea4dce316e99)
 - 꿀팁 : GROUP BY 1 -> SELECT의 첫 컬럼을 의미 (여기선 is_legendary)
 - 1, 2 등 사용 가능


### 동명 이인이 있는 이름은 무엇일까요?

- 꿀팁 : 집계후 조건 삽입 => HAVING, 원본데이터 FROM 절에 있는 데이터에 조건을 삽입 시 WHERE 사용!
![image](https://github.com/user-attachments/assets/d04283ac-c57a-450b-8b29-86c15e152590)


### trainer 테이블에서 "Iris" 트레이너의 정보를 알 수 있는 쿼리를 작성해주세요

![image](https://github.com/user-attachments/assets/0134d501-a179-41db-bb9b-1e2b862c4851)



### trainer 테이블에서 "Iris", "Whitney", "Cynthia" 트레이너의 정보를 알 수 있는 쿼리를 작해주세요.

- AND 써야할 듯 하지만, OR 써야 함. (AND는 저 세 개 이름을 동시에 갖고 있는 트레이너를 찾는 것임)

![image](https://github.com/user-attachments/assets/af20acf6-8b0d-4100-8d19-2b22f22211b9)
- 꿀팁 : OR 여러 개 쓸 경우 -> IN (OR 괄호 내용들) 쓰면 더 편함

### 전체 포켓몬 수는 어떻게 되나?

![image](https://github.com/user-attachments/assets/719e6607-e474-4f61-b8dc-30fa1bfc23c2)

### 세대 별로 포켓몬 수가 얼마나 되는지 알 수 있는 쿼리를 작성해주세요

![image](https://github.com/user-attachments/assets/c27440a2-126c-440a-be9c-bd321bda1004)

### type2가 존재하는 포켓몬의 수는 얼마나 되나요?

![image](https://github.com/user-attachments/assets/27436072-cb60-4b49-9ea8-7dfdab414ee9)

### type2가 있는 포켓몬 중에 제일 많은 type1은 무엇인가요?

![image](https://github.com/user-attachments/assets/7a901acb-f2e4-4916-912e-7d09b10291e3)
- 꿀팁 : LIMIT 설정 안 하면 내림차순으로 쫘르륵 펼쳐짐. 우리가 원하는 것은 가장 많은 것 1순위 -> LIMIT 1으로 제

### 단일 타입 포켓몬 중 많은 type1은 무엇일까요?
- 단일 ㅏ입 -> 하나의 타입만 존재 -> type2가 NULL이어야 함 (type2 is NULL)

![image](https://github.com/user-attachments/assets/a6a051c9-f614-4ef4-b30d-8eeda83c26ee)


### 포켓몬의 이름에 "파"가 들어가는 포켓몬은 어떤 포켓몬이 있을까요?
- WHERE name LIKE "파%" -> 파로 시작하는 단어 / "%파" -> 파로 끝나는 단어

![image](https://github.com/user-attachments/assets/01950640-01ae-40ea-9da3-d85cbd855bcb)

### 뱃지가 6개 이상인 트레이너는 몇 명이 있나요?

![image](https://github.com/user-attachments/assets/c7454728-6296-4313-a462-f397390c5fb6)

### 트레이너가 보유한 포켓몬(trainer_pokemon)이 가장 많은 트레이너는 누구일까요?

![image](https://github.com/user-attachments/assets/4419dd0b-6753-4648-8299-b8636f0a44e5)


### 포켓몬을 많이 풀어준 트레이너는 누구일까요?

![image](https://github.com/user-attachments/assets/917cb499-3c93-4771-8094-4fd82cbcaae4)


### 트레이너 별로 풀어준 포켓몬의 비율이 20%가 넘는 포켓몬 트레이너는 누구일까요?
- 풀어준 포켓몬의 비율 = 풀어준 포켓몬 수/전체 포켓몬 수
  
![image](https://github.com/user-attachments/assets/f7ea150a-764c-4846-af7c-13459c634ddd)


### 요약 정리
![image](https://github.com/user-attachments/assets/e459f9f5-45fd-4747-93a2-32564f5c748c)
- 추가로 ORDER BY ~ DESC, LIMIT, DISTINCT 도 배움


### 새로운 집계 함수 소개
- 원래 GROUP BY 컬럼을 명시했어야 됐는데, GROUP BY ALL도 적을 수 있게 됨


### SQL 쿼리 잘 작성하는 법
![image](https://github.com/user-attachments/assets/99c061d9-43d9-4d50-ad83-2e865c983234)

### 쿼리 작성 템플릿
- 쿼리를 작성하는 목표, 확인할 지표 :
- 쿼리 계산 방법 :
- 데이터의 기간 :
- 사용할 테이블 :
- Join KEY(두 개 이상 연결 시) :
- 데이터 특징 :


  SELECT

  FROM
  WHERE
  => 템플릿 구조화

### 생산성 도구 : Espanso
- 특정 단어가 감지되면 정의된 것으로 바꿔줌!
- ;sp -입력시-> 우리가 구조화한 템플릿 자동으로 나옴.
  






  
