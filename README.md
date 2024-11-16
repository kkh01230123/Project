# Project
# 1. 개발환경 구축:
# 1-1. github 레파지토리 생성
# 1-2. 프로젝트를 진행할 폴더 생성
# 1-3. 프로젝트를 위한 가상환경 생성 및 필요 라이브러리 설치
#   python -m venv '가상환경이름'
#   .\가상환경이름\Scripts\Activate.ps1
#   pip install jupyter
#   pip install pandas numpy matplotlib seaborn
#   pip install scikit-learn
# 1-4. 필요 데이터셋 다운 및 깃 연결
#   git init
#   git commit -m "커밋 메시지"
#   git remote add origin "원격 저장소 url"
#   git push origin main
# 3. 데이터 분석 및 머신러닝
# 2-1. train 데이터로 EDA 진행
# 2-1-1. 생존자:
#   생존자 비율 확인
# 2-1-2. 성별:
#    성별 별 생존자 비율 확인
# 2-1-3. 티켓 클래스:
#    티켓 클래스 별 생존자 비율 확인
# 2-1-4. 결측치 처리:
#    'Age', 'Cabin', 'Embarked'칼럼 결측치 처리
# 2-1-5. 나이:
#    나이 별 생존자 비율 확인
# 2-1-6. 동승자(형제자매, 부모자식):
#    동승자 별 생존자 비율 확인
# 2-1-7 탑승지:
#    탑승지 별 생존자 비율 확인
# 2-1-8 탑승 요금:
#    탑승 요금 별 생존자 비율 확인
# 2-1-9 추가 분석:
#    위의 분석 내용을 바탕으로 추가적인 분석 (ex)생존자가 가장 많은 그룹 or 가장 적은 그룹
# #2-2 데이터 전처리 및 모델 학습:
#    train 데이터와 test 데이터 전처리 후 모델 학습