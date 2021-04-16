4.2
제출 후 확인용 이미지 2개 업로드
4.16
00주차 재실행 후 ipynb파일 및 00주차 관련 파일들 업로드



00주차 내용정리

pandas를 통해 진행 (이후 pd)
1. pd.read_csv('경로') - csv파일 입력
  train.pd.read_csv('/content/drive/MyDrive/argos_team/train.csv')
  
  탐색적 자료분석 Exploratory Data Analysis (EDA)
  
2. pd.DataFrame.head(n) - 데이터프레임을 위에서 n개 출력(default 5)
  train.head(10)
  
3. pd.DataFrame.tail(n) - head()와 동일, 아래에서 부터 출력
  train.tail(6)
  
4. pd.DataFrame.shape - 행과 열의 개수가 저장되어있는 애트리뷰트
  train.shape
  
5. pd.DataFrame.info() - 컬럼별 정보를 알려줌
  train.info()
 #   Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   PassengerId  891 non-null    int64  
 1   Survived     891 non-null    int64  
 2   Pclass       891 non-null    int64  
 3   Name         891 non-null    object
 
6. pd.DataFrame.describe() - 숫자형 (int, float) column들의 기술 통계량(해당 column을 대표할 수 있는 통계값)을 보여주는 함수
  train.describe()
  	  PassengerId	Survived	  Pclass	    Age	        SibSp	      Parch	      Fare
count	891.000000	891.000000	891.000000	714.000000	891.000000	891.000000	891.000000
mean	446.000000	0.383838	  2.308642	  29.699118	  0.523008	  0.381594	  32.204208
std	  257.353842	0.486592  	0.836071	  14.526497  	1.102743	  0.806057   	49.693429

7. pd.Series.value_counts() - series 내 고유값들 각각의 개수를 보여주는 함수
  train['Embarked'].value_counts()
S    644
C    168
Q     77
Name: Embarked, dtype: int64

8. pd.Series.unique() - 해당 series의 고유값들만 보여주는 함수
  train['Embarked'].unique()
  array(['S', 'C', 'Q', nan], dtype=object)
  
9. pd.DataFrame.groupby() - 집단에 대한 통계량 확인
  train.groupby('Sex').mean()
Sex			PassengerId	Survived	Pclass	  Age	      SibSp	    Parch			Fare
female	431.028662	0.742038	2.159236	27.915709	0.694268	0.649682	44.479818
male	  454.147314	0.188908	2.389948	30.726645	0.429809	0.235702	25.523893

10. pd.Series.plot(kind = "bar") - 막대 그래프
  train.groupby('Pclass').mean()['Survived'].plot(kind = 'bar', rot = 0)
  // train 내의 Pclass에 대한 평균값 중 생존여부에 대한 그래프 rot은 x축 이름의 기울기
  
11. pd.Series.plot(kind = 'hist') - 히스토그램
  train['Age'].plot(kind = 'hist', bins = 30)
  train['Age'].plot(kind = 'hist', bins = 30, grid = True) // grid를 통해 보조선을 추가
  
12. pd.DataFrame.plot(x, y, kind = 'scatter') - 산점도, 두 변수간의 관계를 시각화
  train.plot(x = 'Age', y = 'Fare', kind = 'scatter')
  
  데이터 전처리
  
13. pd.Series.isna() - 결측치(데이터에 값이 없는 것) 여부를 확인한다.
    pd.Series.isna().sum() - 그 숫자를 센다.
      Age            177
      SibSp            0
      Cabin          687
      Embarked         2

14. pd.DataFrame.fillna(f) - 결측치를 f로 채운다.
  train['Age'] = train['Age'].fillna(28) -> 나이의 결측치가 28로 저장됨
  
15. pd.Series.map() - 시리즈 내 값을 변환
  train['Sex'] = train['Sex'].map({'male':0, 'female':1}) -> 성별의 male과 female을 0과 1로 변환하여 저장
  
  변수 선택 및 모델 구축
  
학습
X_train = train[['Sex', 'Pclass']] -> train에서 필요한 컬럼만 저장(입력)
y_train = train['Survived'] -> train에서 필요한 컬럼만 저장(결과)
결과
X_test = test[['Sex', 'Pclass']] -> 분석을 진행할 테이블에서 필요한 컬럼만 저장(입력)

lr = LogisticRegression() - 로지스틱 회귀 모형
dt = DecisionTreeClassifier() - 의사결정 나무 모델

  모델 학습 및 검증

각각 모델에 학습
model.fit()
  lr.fit(X_train, y_train)
  dt.fit(X_train, y_train) 

결과예측
model.predict()
  lr.predict(X_test)

확률 예측
model.predict_proba()
  lr.predict_proba(X_test)
  lr_pred = lr.predict_proba(X_test)[:,1] -> 예측 결과 중 전체 행(인원)에 대한 , 생존확률 (0->사망확률, 1->생존확률)
  
결과 저장
pd.DataFrame.to_csv()
  submission['Survived'] = lr_pred
  submission.to_csv('logistic_regression_pred.csv', index = False)
