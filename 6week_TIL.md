![image](https://github.com/user-attachments/assets/d94740a5-4f7d-4bfd-9667-c6fcc4dcfb4f)



## 6-1. 인트로
- 가독성을 챙기기 위한 SQL 스타일 가이드
- 데이터 결과 검증
- 데이터 결과 검증 예시

## 6-2. 가독성을 챙기기 위한 SQL 스타일 가이드
### 데이터 결과 검증을 하기 전에 실수는 언제 발생?
- 문법을 잘못 알고 있는 경우
- 테이터를 잘못 알고 있는 경우
- 데이터를 파악하지 않고 쿼리를 작성하는 경우
- 쿼리가 복잡한 경우

### 내가봐도 남이봐도 가독성있게 잘 작성하자 (조직마다 가이드 다름 유의)

### 예약어는 대문자로 작성
- SELECT, FROM, WHERE, 각종 함수

### 컬럼 이름은 snake_case로 작성
- Not CamelCase! (단, 회사 기준이 Camel이라면 그렇게,,)

### 명시적 VS. 암시적인 이름
- Alias로 별칭 지을 떄에는 명시적인 이름 적용
  - AS a, AS b 등 컬럼의 의미를 한번 더 생각하게 하는 이름이 아닌 명시적인 것을 사용

### 왼쪽 정렬
- 기본적으로 왼쪽 정렬을 기준으로 작성

### 예약어나 칼럼은 한 줄에 하나씩 권장
- 칼럼은 바로 주석처리할 수 있는 장점이 있기에 한 줄에 하나씩 작성
- ![image](https://github.com/user-attachments/assets/0ad70c13-ce78-4ed0-bf1f-e20317f0581a)

### 쉼표는 칼럼 바로 뒤에
- 사바사 의견이 갈리는 부분
- 그래도 BigQuery는 마지막 쉼표를 무시해서 뒤에 작성해도 무방
- ![image](https://github.com/user-attachments/assets/52d3affe-8c6e-4a11-a816-68713f5be034)

## 6-3. 가독성을 챙기기 위한 WITH문 & 파티
### WITH 구문
![image](https://github.com/user-attachments/assets/0f2c11e1-a248-418d-b393-cb4c796d7605)

### 파티션
- 테이블엔 파티션이란 것이 존재할 수 있음
- 왜 쓰냐?
  - 쿼리 성능 향상
    - 전체 데이터를 스캔하는 것보다 파티션을 설정한 곳만 스캔하는 것이 더 빠름
  - 데이터 관리 용이성
    - 특정 일자의 데이터를 모두 변경하거나 삭제해야하면 파티션을 설정해서 삭제할 수 있음
  - 비용
    - 파티션에 해당되는 데이터만 스캔해서 비용을 줄일 수 있음 (BigQuery는 쿼리 용량에 비례해서 과금)

## 6-4. 데이터 결과 검증 정의
### 카일스토리
- 갑작스럽게 데이터 추출을 해야하는 상황에 빠르게 데이터를 추출 후 공유해야 한다면?
- 근데 거기에 오류도 있고, 다시 공유하면서 정정 .... ㅜ
### 데이터 결과 검증을 어떻게 할 수 있을까?
- 항상 그 실수 이후에 어떻게 해야 다시 반복되지 않을까 생각하는 마인드셋 필요!
- SQL 쿼리 후 얻은 결과가 예상과 일치하는지 확인하는 과정 (분석결과의 정확성, 신뢰성 확보)
### 제일 중요한 부분
- 문제를 잘 정의하고, 미리 작성해보기
- 도메인 특수성(이런 규칙 등) 잘 파악하기
- SQL 쿼리 템플릿과 맥락이 유사
### 데이터 결과를 검증하는 흐름
![image](https://github.com/user-attachments/assets/e51ef5b9-b90b-48ab-bd8a-72a881e812bd)
### 검증 시 자주 활용하는 SQL쿼리
- COUNT(*): 행 수를 확인. 의도한 데이터의 행 개수가 맞는가?
- NOT NULL: 특정 컬럼에 NULL이 존재하는가? 필수 필드가 비어있지 않은가? (데이터가 잘 저장되어 있는가?)
- DISTINCT: 데이터의 고유값을 확인해 중복 여부 확인 COUNT(DISTINCT 컬럼) = COUNT(컬럼)
- IF문, CASE WHEN: 의도와 같다면 TRUE, 아니면 FALSE

## 6-5 데이터 결과 검증 에시
![image](https://github.com/user-attachments/assets/daf94cab-9448-4da3-8357-0a612a515f46)
![image](https://github.com/user-attachments/assets/38ec1599-366b-4545-91c7-307d5dff6d9d)
### 1) 전체 데이터 파악
### 2) 특정 user_id 선정
### 3) 승률 직접 COUNT : 결과예상
### 4) 쿼리 작성
### 5) 실제와 비교

## 6.6 정리
![image](https://github.com/user-attachments/assets/a26fac92-9860-4655-b1d1-b3279eb15d96)

