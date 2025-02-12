# 신재생 에너지(태양열) 설비(접속반) 건전성 평가 모델 개발

## 👥 팀 구성

- **팀장**: 이원 ([GitHub](https://github.com/yusongod0303))
- **팀원**:
  - 팀원: 이유송 ([GitHub](https://github.com/yusongod0303))
  - 팀원: 임혁진 ([GitHub](https://github.com/example2))

## 📌 프로젝트 개요
**제10회 공공데이터 활용 비즈니스 아이디어 공모전 - 빅데이터 분석 부문 장려상**

신재생 에너지 설비의 핵심 구성 요소인 **접속반(Junction Box)**의 **건전성 평가 모델**을 개발하였습니다.
이 모델은 접속반의 고장을 사전에 예측하여 설비의 안정적인 운영을 지원하고, **주의, 경고, 위험** 단계를 제공하여 효과적인 유지보수를 가능하게 합니다.

## 🚀 문제 정의
기존의 태양광 설비 점검 방식은 **사후 관리 중심**으로, 고장이 발생한 후 대응하는 방식이었습니다.
이를 해결하기 위해 **고장을 사전에 예측**하여 유지보수 효율을 높일 수 있는 시스템이 필요했습니다.

## 🛠 솔루션 개요
- **데이터 분석 및 시각화**: 접속반 센서 데이터 + 날씨 데이터 분석
- **머신러닝 기반 예측 모델**: 랜덤 포레스트, 선형 회귀 적용
- **건전성 평가 시스템 개발**: 온도 임계값을 기반으로 주의/경고/위험 단계 분류

## 🏗 기술 스택
- **언어**: Python
- **라이브러리**: pandas, numpy, matplotlib, seaborn, scikit-learn
- **모델링**: Random Forest, Linear Regression
- **데이터 시각화**: Matplotlib, Seaborn

## 📊 데이터 설명
### 1. 접속반 데이터
- **수집 주기**: 1분 단위 & 10분 단위
- **주요 변수**: 온도, 전압, 전류 등

### 2. 날씨 데이터
- **수집 주기**: 1시간 단위
- **주요 변수**: 기온, 습도, 풍속 등

## 🔍 모델링 과정
1. **데이터 전처리**
   - 결측값 처리 및 이상치 제거
   - 데이터 정규화 및 표준화
2. **데이터 분석 및 상관관계 파악**
   - 특정 변수 간 높은 상관 관계 확인
3. **머신러닝 모델 적용**
   - 랜덤 포레스트 → 과대적합 발생
   - 선형 회귀 → 최적 성능 확인
4. **건전성 평가 기준 설정**
   - 특정 온도 이상 상승 시 **주의, 경고, 위험 단계 분류**
