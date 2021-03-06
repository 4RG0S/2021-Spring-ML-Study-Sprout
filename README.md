# 2021-Spring-ML-Study-Sprout
- K-사이버 시큐리티 챌린지 2021 참가를 목표로 스터디하는 팀
- 기계학습 공부
  - 데이콘(https://dacon.io/main)의 대회와 교육자료를 바탕으로 데이터 분석과 머신러닝 코딩 실습 예정
  - 기계학습 모델에 대한 이해

- 이번 학기는 신입생도 있어서 가볍게 시작할 수 있는 탐색적 데이터 분석과 이미지 분류 위주로 진행할 계획입니다
- 커리큘럼
  - 타이타닉 생존자 예측(기초)
  - 타이타닉 생존자 예측(심화)
  - 서울시 따릉이 수요 예측(기초)
  - 서울시 따릉이 수요 예측(심화) or 기타 대회
  - MNIST 숫자 이미지 분류 
  - 의류 클래스 예측

- 사용 언어 및 도구
  - 파이썬, 사이킷런, 케라스, 코랩

- 운영방식
  - 매주 과제 수행 후 깃에 업로드 and 격주 발표
  - 중간고사가 있으면 2주 휴뮤
  - 교육이 아니라 스터디라는 점 명심해 주시길 바랍니다

-
-
- 0주차 : 타이타닉 생존자 예측 실습 기초
  - 해당 영상 3개를 모두 보면서 똑같이 따라하기 https://www.youtube.com/watch?v=NpB2hxrQ2Ck&list=PLrJaZ4ogQUHww5WsXIPOkWDQfkAapnayC
  - 4/2일까지 완료하시고 인증하시면 됩니다(인증 방법은 영상을 끝까지 따라하시면 자연스럽게 알 수 있습니다)
  - 교육이 아니라 스터디임으로 궁금한 점은 언제든지 단톡방에 올려주시면 됩니다
  - 그리고 모두가 함께 고민해봅시다(잘 몰라도 아는 척 해주세요...)
- 0주차 리뷰(4/3) :
  - 세부 폴더 만들기, .ipynb 파일 업로드, 자신이 무엇을 했는지 기록 남기기 (모범예시 : https://github.com/4RG0S/2021-Spring-ML-Study-Sprout/tree/main/202102712)
  - 의사 결정 나무와 로지스틱 회귀의 평점이 너무 똑같이 나왔다...? 이유가 뭘까? (스터디를 진행하다보면 자연스럽게 알 수 있음)
  - 조금이라도 모르는 것을 부끄러워 하지 마시고 단톡에 올려주세요... 여러분의 궁금함이 스터디 발전에 도움됩니다 
  - 모두 함께 고민해봅시다^^
  -
- 1주차 : 타이타닉 생존자 데이터 시각화
  - 1-1
  - https://www.finereport.com/kr/%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%8B%9C%EA%B0%81%ED%99%94%EC%9D%98-%EC%B2%AB-%EB%B0%9C%EA%B1%B8%EC%9D%8C-%EC%9D%B4%EA%B2%83%EB%A7%8C-%EC%95%8C%EB%A9%B4-%ED%95%A0-%EC%88%98-%EC%9E%88%EB%8B%A4/?utm_campaign=article&utm_medium=facebook3%281%29&utm_source=lydia-f3&utm_term=2021 
  - 위 링크를 읽어 보자
  - 과연 그래프가 이것만 있을까? 유료툴이 아닌 무료로 하는 법은?
  - 파이썬으로 데이터 시각화하기 https://zzsza.github.io/development/2018/08/24/data-visualization-in-python/ (4/16까지, 4/9중간점검)
  - 어떤 데이터(Feature)를 어떤 그래프로 어떻게 시각화를 해야할까?
  - 코랩 등 주피터 노트북으로 작업해서 깃헙에 올리기 (이번 주차 내용은 시간과 고민이 약간 필요한 내용입니다, 미루지 말고 조금조금씩 하시는 것을 권장합니다)
  - 무료 인강 : https://www.inflearn.com/course/%EB%8D%B0%EC%9D%B4%ED%84%B0-%EC%8B%9C%EA%B0%81%ED%99%94-%EC%B0%A8%ED%8A%B8%EB%B6%84%EC%84%9D#
  - 위 링크를 참고해서 진행해도 되고 다른 (유튜브)영상 또는 블로그 등을 참고해도 무관
  -
  - 1-2
  - 머신러닝 개념 입문 : 선형회귀(다중선형회귀), 로지스틱회귀, 의사결정나무 란? + 탐색적 데이터 분석
  - 위 내용을 검색해서 개념을 알고가자 (깊게 몰라도 되요 간단한 개념만!) ppt에 정리해서 pdf형식으로 깃허브에 업로드 (4/16일까지)
- 1주차 리뷰(4/17) :
  - 진건승 1-2 발표
  - 팀원 대부분 과제가 미완성이다...
  - 미완성이라도 꾸준하게 업로드 해주세요
  - 중간고사 잘 보시고 2주 후 뵙겠습니다
-
- -중간고사- (4/18~5/1)
  - 머리식힐 때 생각해보기
  - 타이타닉 생존자 예측은 이산적인 데이터를 이진 분류하는 문제
  - 어떻게 해야 성능을 높일 수 있을까?
  - 검색 키워드 (Feature, 데이터 전처리, 데이터 사이언티스트 다이어그램, knn 알고리즘, Naive Bayes, cnn 알고리즘, Ensemble )
- 
- 2주차 : 타이타닉 평점 높이기
  - 미완성 시각화 완성하기
  - 시각화 등 탐색적 데이터 분석한 내용을 바탕으로 평점 높이기
  - 기간 : 5/2 ~ 5/8 
- 2주차 리뷰(5/15)
  - 2주차 리뷰 내용 ~
- 
- ~~3주차 : 따릉이 데이터 분석~~
  - ~~1-1~~
  - ~~0주차와 같이 https://www.youtube.com/watch?v=WreGAJxukpA&list=PLrJaZ4ogQUHy1nYmWomNRGr4HtY1fjIBS 해당 영상들을 보고 따라하기~~
  - ~~1주차의 데이터 시각화하기 해당 프로젝트 적용~~
  - ~~2주차의 평점 높이기 해당 프로젝트에 적용~~
  - ~~기간은 5/8 ~ 5/14 입니다~~
  - 
  - ~~1-2~~
  - ~~시계열 데이터란 무엇인가?~~
- ~~3주차 리뷰(5/15)~~
  - ~~3주차 리뷰 내용 ~~
-
- 3주차 : 손글씨 이미지 분류하기 - OpenCV
  - CNN 알고리즘
  - OpenCV를 사용해서 MNIST 속 숫자 찾기
  - 사용한 소스코드 업로드
- 3주차 리뷰(5/16)
  - 대부분 팀원이 깃허브에 업로드를 안했다...
  - 열심히 해주세요
-
- 4주차 : Orange를 이용한 손글씨 이미지 분류
  - 1-1
  - https://www.youtube.com/watch?v=HNaaZCh2DWk
  - https://www.youtube.com/watch?v=6SCb5hDmVYk&t=519s
  - 위 두 영상을 보고 실습 따라하기
  - 결과 캡쳐 및 깃허브에 업로드
  - 리드미에 리뷰 작성
  - 1-2
  - 멀티 퍼셉트론이란?
  - 공부하고 내용 남기기(리드미, 피피티, 블로그 상관 없음)
- 4주차 리뷰(5/22) - 데브데이로 인해 온라인 모임은 하지 않겠습니다
- 리뷰 내용 ~ 
-
- 5주차 : 손글씨 이미지 분류하기 - CNN
  - 파이토치 케라스 등 사용하기
  - https://dacon.io/competitions/open/235596/talkboard/400649?page=1&dtype=recent
  - https://dacon.io/competitions/open/235596/talkboard/400683?page=1&dtype=recent
  - 위 두 영상 참고하고 따라하기
  - 응용 : 0~9가 아닌 0 또는 1 만 분류하는 모델을 만들어보자
- 5주차 리뷰(5/29)
  - 리뷰 내용 ~
  -
- 한 학기 모두 정말 수고하셨습니다.
-
- 0xFF주차 
  - 이렇게 끝내는게 아쉬워서 보너스를 가져왔습니다
  - https://www.youtube.com/watch?v=5ke6zRNrYF8&list=PLrJaZ4ogQUHxh9nUOy26xvJpgHGr2-4Ju&index=2
  - 위 유튜브 영상(14분)을 보고 알게된 내용을 정리해서 pdf로 올려주세요
  - 실습은 하면 좋겠지만 하지 않으셔도 됩니다
  - 최근 캐글 등 대회에서 최종 결과물로 도커 파일 제출을 요구하는 대회가 많습니다 
  - 위 영상에 안내된 블로그에 방문해서 정독하시는 것을 매우 추천합니다
-
- 0xFF주차 리뷰(없음)
  - 6/23까지 진행해주시면 됩니다
  - 내용이 짧아서 짧게 하면 1시간이면 끝나고 조금 더 깊게 해보고 싶으시면 영상에 소개된 블로그를 보고 알게된 내용도 같이 정리하시면 좋습니다
-
- 다들 좋은 방학 되세요^^
