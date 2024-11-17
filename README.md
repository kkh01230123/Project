#  타이타닉 데이터셋 분석 Project
기계학습 및 실습 강의에서 진행하는 중간과제로 타이타닉 데이터셋 분석을 해 보았다.
---
## 1. 개발환경 구축:
### 1-1. github 레파지토리 생성
    - 깃허브에 프로젝트를 업로드할 레파지토리를 먼저 만든다
### 1-2. 프로젝트를 진행할 폴더 생성
    - 프로젝트 파일이나 데이터셋, 가상환경 파일등이 들어갈 파일 생성
### 1-3. 프로젝트를 위한 가상환경 생성 및 필요 라이브러리 설치
    1. python -m venv '가상환경이름'
        - 파이썬 가상환경을 생성하는 코드
    2. .\가상환경이름\Scripts\Activate.ps1
        - 생성한 가상환경을 실행
    3. pip install pandas numpy matplotlib seaborn
        - 데이터 분석에 필요한 파이썬 라이브러리 설치
    4. pip install scikit-learn
        - 머신러닝 분석에 필요한 라이브러리 설치
### 1-4. 필요 데이터셋 다운 및 깃 연결 
    1. git init
        - 깃 초기화
    2. git add .
        - 파일 추가
    3. git commit -m "커밋 메시지"
        - 커밋 생성
    4. git remote add origin "원격 저장소 url"
        - 원격 레파지토리 추가
    5. git push origin main
        - 로컬 변경사항을 깃에 푸시
---
## 2. 데이터 분석 및 머신러닝

---
### 2-1. train 데이터로 EDA 진행
    1. 2-1-1. 생존자
        - 생존자 비율 확인: 생존자와 사망자의 비율을 시각화해서 표현
    
    
    2. 2-1-2. 성별:
        - 성별 별 생존자 비율 확인: 남성 탑승객과 여성 탑승객의 비율과 각 성별 별 생사 비율을 시각화 해서 비교
    
    
    3. 2-1-3. 티켓 클래스:
        - 티켓 클래스 별 생존자 비율: 티켓 클래스 별 승객의 통계와 그 통계에 따른 생존자 비율을 시각화해서 분석
    
    
    4. 2-1-4. 결측치 처리:
        - 'Age', 'Cabin', 'Embarked'칼럼 결측치 처리: Null값이 존재하는 칼럼에서 결측치 처리(Age: 평균값 대체, Cabin: 칼럼 삭제, Embarked: 최빈값 대체)
    
    
    5. 2-1-5. 나이:
        - 나이 별 생존자 비율 확인: 나이 별 승객의 통계와 나이와 생존률의 상관관계를 시각화해서 분석
    
    
    6. 2-1-6. 동승자(형제자매, 부모자식)
        - 동승자 별 생존자 비율 확인: 같이 탑승한 부모자식과 형제자매의 수에 따른 생존자 비율을 통계와 시각화로 분석
    
    
    7. 2-1-7 탑승지:
        - 탑승지 별 생존자 비율 확인: 탑승 항구에 따라 달라지는 생존률을 비교
   
   
    8. 2-1-8 탑승 요금:
        - 탑승 요금 별 생존자 비율 확인: 탑승 요금이 생존률에 영향을 미치는지 확인
   
   
    9. 2-1-9 추가 분석:
        - 위의 분석 내용을 바탕으로 추가적인 분석 (ex)생존자가 가장 많은 그룹 or 가장 적은 그룹
   
### 2-2 데이터 전처리 및 생존자 예측모델 학습(랜덤 포레스트)
    1. train 데이터와 test 데이터 전처리 후 모델 학습
        - 데이터 품질 향상 및 모델 학습의 효율과 성능 극대화
    
    
    2. 머신러닝 라이브러리를 통한 모델 학습(랜덤 포레스트)
        - 처리된 데이터를 사이킷런 라이브러리를 통해서 학습