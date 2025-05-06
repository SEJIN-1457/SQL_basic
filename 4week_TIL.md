# 4.4 날짜 및 시간 데이터 이해하기
- CURRENT_DATETIME([time zone]) : 현재 DATETIME 출력
- EXTRACT(~ FROM ~) : DATETIME에서 특정부분만 추출하고 싶은 경우 (일자별, 월별)
  ![image](https://github.com/user-attachments/assets/01b2975e-0f1a-4b91-99aa-9a074b61d963)
- EXTRACT(DAYOFWEEK FROM datetime_col) : 요일을 추출하고 싶은 경우 (일요일로 시작하는 한 주 범위의 값이 반환)
- DATETIME_TRUNC : DATE와 HOUR만 남기고 싶은 경우 (ex. 분, 초 자르기)
  ![image](https://github.com/user-attachments/assets/69d009f1-5a1b-4994-b06a-3bd0c9bc8084)
- PARSE_DATETIME : 문자열로 저장된 DATETIM은 DATETIME 타입으로 바꾸고 싶은 경우
- FORMAT_DATETIME : DATETIME 타입 데이터를 특정 형태의 문자열 데이터로 변환하고 싶은 경우
- LAST_DAY : 마지막 날을 알고 싶은 경우 (자동으로 월의 마지막 값을 계산)
  ![image](https://github.com/user-attachments/assets/41b56354-01db-4ae4-b583-e6ad1dbc740a)
- DATETIME_DIFF(첫 DATETIME, 두번째 DATETIME, 궁금한 차이) : 두 DATETIME의 차이를 알고 싶은 경우
- 정리
  ![image](https://github.com/user-attachments/assets/fc63de4c-e265-48f2-b001-7fac470d286f)

# 4.5 시간 데이터 연습문제
- 1번
  ![image](https://github.com/user-attachments/assets/aac79e3f-90d0-4210-932a-0d526b94096f)
- 2번
  ![image](https://github.com/user-attachments/assets/f8fbdc0f-92b8-4dd9-b0b3-f28034c51585)
  ![image](https://github.com/user-attachments/assets/93908cf0-528f-48c1-b826-2436113215ab)
- 3번
  ![image](https://github.com/user-attachments/assets/bd33fd27-92f2-4fb1-8f77-c4ac514df9a8)
- 4번
  ![image](https://github.com/user-attachments/assets/1be02a37-4387-4e5f-bafa-0371354016b5)
- 5번
  ![image](https://github.com/user-attachments/assets/f80049a3-9d16-4e31-8e80-ed829528d289)

# 4.6 조건문 함수
- 조건문
  ![image](https://github.com/user-attachments/assets/5cf55aef-35ed-43ca-bc4f-ce59cc3b9ee0)
- 조건문 함수가 사용되는 이유
  ![image](https://github.com/user-attachments/assets/ae5e1f6f-da18-41e2-889a-7618d6dace39)
- 1) CASE WHEN (다조건, 순서에 유의)
  ![image](https://github.com/user-attachments/assets/f4320152-4f2f-46df-8413-b0a5709f54cc)
  ![image](https://github.com/user-attachments/assets/54b58b16-5525-4ba7-b5d7-738e0827bf26)
  ![image](https://github.com/user-attachments/assets/e1d0f46c-e841-4b3e-8df0-13d5395d6166)
- 2) IF (단일 조건)
  ![image](https://github.com/user-attachments/assets/7968a6af-65a0-44cb-8d2b-d63c5a2788d7)

# 4.7 조건문 함수 연습문제
- 1번
  ![image](https://github.com/user-attachments/assets/5e55661f-2cda-4588-ac13-f9e8e1262abc)
- 2번
  ![image](https://github.com/user-attachments/assets/f6685ccd-8ab6-4903-b176-d2461a3a562e)
- 3번
  ![image](https://github.com/user-attachments/assets/5d71f13a-3a6f-437d-a45a-2538e01dfa78)
- 4번
  ![image](https://github.com/user-attachments/assets/48efbcb6-6273-4507-8385-93fb90773b0f)
- 5번
  ![image](https://github.com/user-attachments/assets/a184565f-a7ae-4b2c-a1a1-6fd45b382d91)
  *"이후"라는 사전적 의미엔 기준이 되는 시점을 포함합니다. 이 부분을 포함하지 않고, > "2023-01-01"라고 작성했는데, >= "2023-01-01"로 수정해야 함
- 6번
  ![image](https://github.com/user-attachments/assets/9326446d-294b-4eaa-80a9-7afef32878b3)

# 4.8 정리
- 컬럼 변환하기
  ![image](https://github.com/user-attachments/assets/cd17c0d5-3aac-4326-9e65-f15ea4ce9d1e)
  - 숫자 : 사칙연산 SAFE_DIVIDE
  - 문자 : CONCAT, SPLIT< REPLACE, TRIM, UPPER
  - 시간, 날짜 : EXTRACT(HOUR FROM datetime), DATETIME_TRUNC, PARSE_DATETIME
  - 부울 : 데이터 타입 변경하기(SAFE_CAST), 조건문(CASE WHEN, IF)


![image](https://github.com/user-attachments/assets/27568687-84fe-4e2e-bb72-5c875ceb34f7)
