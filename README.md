섹션6. 다량의 자료를 연결: JOIN

**5-1. Intro**
![image](https://github.com/user-attachments/assets/00e8931a-60e5-4792-ae55-491eceb09219)
![image](https://github.com/user-attachments/assets/fa1abfd6-ee9b-4ce7-b8b0-b5089b9bd21d)

**5-2. JOIN 이해하기**
- 서로 다른 데이터 테이블을 연결하는 것
- 많은 문제 풀이를 통한 체화가 필요
- 두 데이터 어떻게 연결?
- ![image](https://github.com/user-attachments/assets/522c6f45-75d1-4a8b-9dbd-33dd9569cbe3)
- ![image](https://github.com/user-attachments/assets/27eb96e8-4d83-46f1-9415-deae12f0793d)
- ![image](https://github.com/user-attachments/assets/cd3dd244-93b0-4146-8c7b-6babb0b527b4)
- JOIN 
  - 서로 다른 데이터 테이블 연결
  - 공통 컬럼 있어야 JOIN 가능
  - 보통 id를 key로 많이 사용


**5-3. 다양한 JOIN 방법**
- (INNER) JOIN : 두 테이블의 공통 요소만 연결
- LEFT/RIGHT (OUTER) JOIN : 왼쪽/오른쪽 테이블 기준으로 
- FULL (OUTER) JOIN : 양쪽 기준으로
- CROSS JOIN : 두 테이블의 각각의 요소 곱하기 (데이터 뻥튀기 조심)
- ![image](https://github.com/user-attachments/assets/456f46d6-c0d7-4a39-a0b0-33c20a71b0d0)
- ![image](https://github.com/user-attachments/assets/fb571d59-5987-4553-bef2-b61af59b79ba)


**5-4. JOIN 쿼리 작성하기**
- ![image](https://github.com/user-attachments/assets/363513dc-e19f-44d9-b003-de66be60fea2)
- ![image](https://github.com/user-attachments/assets/676bbe49-04e3-47f4-806e-72a42b17eeb0)
- ![image](https://github.com/user-attachments/assets/9c8b94a1-903a-49fd-959b-eb89842499e7)
- CROSS JOIN은 ON 필요 X

- SELECT
-  tp.*,
-   t.* EXCEPT(id), #trainer_id => tp에 있어 중복 피하기 위함.
-   p.* EXCEPT(id) #pokemon_id => tp에 있어 중복 피하기 위함.
- FROM basic.trainer_pokemon AS tp
- LEFT JOIN basic.trainer AS t
- ON tp.trainer_id=tp.id
- LEFT JOIN basic.pokemon AS p
- ON tp.pokemon_id=p.id


**5-5. JOIN을 처음 공부할 때 헷갈렸던 부분**
- 1. 어떤 JOIN 사용?
  - 하려는 '작업 목적 따라'
  - 교집합 : INNER
  - 합집합 : CROSS
  - 그 외 LEFT / RIGHT_LEFT추천(하나를 계속 확용)

- 2. 어떤 Table이 왼쪽?
  - (예) 주문한 유저들의 00 => '주문한' 유저만 확인하면 됨 => order 테이블 (왼) + user 테이블 (오)
  - (예) 유저 중 주문하지 않은 유저들은? => 모든 '유저' 필요 => user 테이블 (왼) + order 테이블 (오)

- 3. 여러 Table 연결 가능?
  - 제한 없음.
  - 단, 너무 많이 JOIN할 경우, 아예 JOIN한 테이블 만드는 편이 나음.

- 4. 컬럼 모두 다 선택해야?
  - 현업에선 필요한 컬럼만.
  - id값은 유니크한 값인지 확인 위해 되도록 포함.

- 5. NULL이 뭐지?
  - NULL : 값이 없음. 0과 다름.
  - ![image](https://github.com/user-attachments/assets/b2ef457f-78e9-45fe-8e86-5f85461cdb6c)


*5-6. JOIN 연습문제 1~2번*
- 1. 트레이너가 보유한 포켓몬들은 얼마나 있는지 알 수 있는 쿼리를 작성해주세요.
  - 보유했다의 정의는 status가 Active,Training인 경우를 의미
- 2. 각 트레이너가 가진 포켓몬 중에서 'Grass'타입의 포켓몬 수를 계산해주세요.
  - (단,편의를위해type1기준으로계산해주세요)
​
*5-6. JOIN 연습문제 3~5번*
- 3. 트레이너의 고향(hometown)과 포켓몬을 포획한 위치(location)를 비교하여, 자신의 고향에서 포켓몬을 포획한 트레이너의 수를 계산해주세요.
  - status상관없이구해주세요
- 4. Master등급인 트레이너들은 어떤타입의 포켓몬을 제일 많이 보유하고 있을까요?
- 5. Incheon출신 트레이너들은 1세대, 2세대 포켓몬을 각각 얼마나 보유하고 있나요?

**5-7. 정리**
- JOIN : 여러 테이블을 연결해야 할 때 사용하는 문법
- Key : 공통적으로 가지고 있는 컬럼
- JOIN 종류
  - INNER / LEFT/RIGHT / FULL / CROSS
  - 정리표 프린트해서 외우면 도움됨.

![image](https://github.com/user-attachments/assets/fda674dc-6a48-4d4a-bc68-c64c22c17b3e)


**(연습 문제 풀이의 경우, 기록에 대한 부담 없이 들어주세요 :))**

**6개** 강의를 수강하고, 알게 된 점들을 깃허브에 정리하여

링크를 스프레드시트 ‘SQL’ 시트에 붙여넣어주세요 :)

**수행 인증샷은 필수입니다!**

오늘도 수고하셨습니다 🔅
