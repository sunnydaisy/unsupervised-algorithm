# Unsupervised Learning Study
### 🏖 회사 방학기간을 통한 프로젝트 진행을 위한 비지도학습 공부 :)

<br>

>1. 목표: 비지도학습 책 완료 및 프로젝트 내 알고리즘 적용
>2. 일정: 8/3~
>3. 프로젝트 시작: 8/8~


## 지도학습 통한 신용카드 사기탐지 시스템
- 스케일러  

종류 | 설명 
---- | ---- 
StandardScaler |	기본 스케일. 평균과 표준편차 사용\n 이상치가 있는 경우 균형 잡힌 척도를 보장할 수 없다.
MinMaxScaler |	최대/최소값이 각각 1, 0이 되도록 스케일링\n 이상치가 있는 경우 변환된 값이 매우 좁은 범위로 압축
MaxAbsScaler |	최대절대값과 0이 각각 1, 0이 되도록 스케일링\n 큰 이상치에 민감
RobustScaler |	중앙값(median)과 IQR(interquartile range) 사용. 아웃라이어의 영향을 최소화

-> 대부분의 스케일링 기법에서 아웃라이어는 변환 효과를 저해하는 요소
<!-- <p align="center"> -->
<img src = "https://mkjjo.github.io/img/posting/2019-01-10-001-robustscaler.png" width="70%" >

+ 정밀도-재현율 곡선  
    + 임계값이 너무 높게 설정되며 양성으로 예측되는 경우가 거의 없으므로 정밀도는 높지만 재현율은 낮음
    + 반대로, 임계값이 너무 낮아지면 더 많은 케이스 양성을 예측되어 일반적으로 정밀도가 감소하고 재현율이 증가  
-> 정밀도에 대한 가중평균으로 평균 정밀도 계산 가능하며, 이 점수가 높을수록 더 좋은 솔루션임
<img src = "https://user-images.githubusercontent.com/47199328/128221597-3c85fe35-db7b-42e7-b255-dee10399f9f9.png" >

## 📋코드 작성 꿀팁
- 파일 zip으로 공유 시 동일 폴더 파일 접근할 수 있도록 함
```python
current_path = os.getcwd()
file = os.path.sep.join(['', 'dataset', 'credit_card_data', 'creditcard.csv'])
data = pd.read_csv(current_path + file)
```



