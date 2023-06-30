# machine_learing
지역별 상수원 수요 파악을 위한 배수지별 유량 적산차 예측

[2022 제 2회 K-water AI 경진대회] 수돗물 수요 예측 AI 알고리즘 개발
위의 대회를 이용한 프로젝트

📍 주제 및 목표
    + 주제 : 지역별 상수원 수요 파악을 위한 배수지별 유량 적산차 예측
    + 목표 : 대상지(경상북도 김천시 율곡동)의 상수원 사용량에 따라 달라지는 배수지의 유량 적산차를 예측. 정확한 수요 예측은 수자원 사용 및 수
            자원 공급에 필요한 에너지 소비를 최적화하는 데에 기여

📍 예측 유형 : 24 to 24
    
    ⬝ 배수지의 유량 적산차(24시간 단위)가 제공, 매 시점부터 총 1일(1×24 = 24시간) 분량의 적산차 변화를 예측

📊 전처리
   ⬝ 이상치 처리를 위한 상안값을 1000으로 설정
   ⬝ 이상치는 전 후 데이터 값을 통해 선형 보간
   ⬝ Min-Max scaling 이용

📈 모델링
    ⬝ 시도 모델 : RNN, LSTM
    ⬝ 최종 모델 : LSTM
