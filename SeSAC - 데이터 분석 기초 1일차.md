## SeSAC - 데이터 분석 기초 1일차

2022.07.18

---

- 스튜어트 J. 러셀 : 인공지능 : 현대적 접근방식 제 4판
- 공부하는 데이터 분석 with 파이썬

<br>

### 기계는 생각할 수 있는가?

기계는 생각할 수 있다. 하지만 사람처럼 생각할 수 없다. 그 이유는 뭘까?

**인간은 지능을 설명할 수 없다.**

<br>

사람의 생각하는 원리를 설명할 수 없고 감정이 어떻게 생기는지, 머릿속이 어떻게 돌아가는지 알수없다.

우리가 만드는 인공지능은 짝퉁과 같다.

지능적 **행위의 결과물에 대한 모방만 가능하다.**

- 영화 HER
- 영화 이미테이션 게임

<br>

우리가 해야할건 인공지능을 우리처럼 생각할 수 있게 꼬드겨야한다.

AI(인공 지능)은 1956년 다트머스 회의에서 처음으로 사용 되었다.

[인공지능 기술, 다트머스 회의를 통해 부상하다](https://brunch.co.kr/@rudaleeactc/51)

<br>

앨런 튜링에 의하면 지능 이란 추론할 수 있어야한다.

[Wolf, Sheep And Cabbage Game](https://www.proprofsgames.com/wolf-sheep-and-cabbage/)

링크의 게임을 해보자.

<br>

우리는 이 게임을 지능을 통해 풀었는가? 

옮기는 행위의 결과에 따라 문제를 풀던, 설명을 보고 풀던, 아래의 정답을 보고 풀어도 우리는 추론을 통해 풀었을것이다.

<img width="801" alt="스크린샷 2023-07-18 오전 10 59 26" src="https://github.com/kimbap918/TIL/assets/75712723/8571d1d4-1779-4248-8931-8ffaf9e34414">

우리는 위 문제의 조건을 보고 추론을 통해 이 문제의 배열을 풀어낼것이다. 하지만 기계에게 추론이란 매우 힘든 일이다.

<br>

### 인공지능에 꼭 기억해야할 인물

마빈 리 민스키(Marvin Lee Minsky) : 지식의 표현과 추론(knowledge representation and reasoning), 기호주의자

프랑크 로젠블랫(Frank Rosenblatt) : 현대 딥러닝의 단초가 된 퍼셉트론(Perceptron)을 개발, 연결주의자

제프리 에베레스트 힌튼(Geoffrey Everest Hinton) : 인공지능(AI) 분야를 개척한 영국 출신의 인지심리학자이자 컴퓨터 과학자

<br>

📌 지식의 표현과 추론을 할수있는 언어, prolog

[](https://product.kyobobook.co.kr/detail/S000001161313)

[프롤로그 (프로그래밍 언어)](https://ko.wikipedia.org/wiki/프롤로그_(프로그래밍_언어))

[SWI-Prolog](https://www.swi-prolog.org/)

```prolog
male(허생원).
male(동이).
female(분이).

parent(분이, 동이). 
married(허생원, 분이).
married(분이, 허생원).

/*
 * X가 Y의 엄마라면, X는 여자, X는 Y의 부모.
 * */
mother(X, Y) :- female(X). parent(X, Y).
/*
 * X가 Y의 아빠라면, X는 남자, X가 Z와 결혼했다면 엄마는 Z
 * */
father(X, Y) :- male(X). married(X, Z). mother(Z).
```

동이의 아빠는 누굴까?

```prolog
?- father(X, 동이)

X = 허생원
```

<img width="837" alt="스크린샷 2023-07-18 오전 11 52 19" src="https://github.com/kimbap918/TIL/assets/75712723/2e0bc405-a2cf-4517-8a7d-7a934f62d3f2">

<br>

### 기호주의, 연결주의와 퍼셉트론

기호주의자(symbolist) : 인간의 지식을 기호화 하고 새로운 문제를 풀기 위해서 이미 존재하는 지식을 학습 과정에서 사용하는 방법, 그리고 여러가지의 단편적 지식을 합치는 방법을 강조하는 사람들.

연결주의자(connectionist) : 인간의 두뇌에서 어떻게 생각하는지를 모방하여 컴퓨터를 학습시키는 방법, 모델에서 학습의 중요성을 강조하는 사람들.

연결주의 알고리즘, 퍼셉트론(Perceptron) **:** 연결주의를 주장한 프랭크 로젠블랫이 고안한 초기 형태의 인공 신경망. Perception(인지 능력)과 Neuron(뇌 신경세포)를 결합한 단어. 퍼셉트론은 입력신호(input)를 입력받아 다른 하나의 신호(output)을 출력하는 알고리즘이다.

[[4] 인공지능의 2가지 관점: 기호주의와 연결주의](https://m.blog.naver.com/PostView.naver?blogId=mondrian-ai&logNo=222096661818&categoryNo=12&proxyReferer=)

<br>

### (참고)평생학습(continual learning)

[Continual Learning: 꾸준히 성장하는 모델을 만들기 위한 기술](https://tech.scatterlab.co.kr/continual-learning/)

<br>

### CRISP-DM (Cross-Industry Standard Process for Data Mining)

전 세계에서 가장 많이 사용되는 데이터 마이닝 표준 방법론

<img width="686" alt="스크린샷 2023-07-18 오후 1 44 33" src="https://github.com/kimbap918/TIL/assets/75712723/b7af3c6f-b783-4b55-ac2a-fc1d3513be66">

<img width="795" alt="스크린샷 2023-07-18 오후 2 08 03" src="https://github.com/kimbap918/TIL/assets/75712723/3c08a9d7-f685-4d2a-885e-63fdda503bcc">

1. 비즈니스 이해(Business Understanding) : 무엇을 할것인지, 이것을 해도 되는지, 윤리적 이해 등
2. 데이터 이해(Data Understanding) : 데이터로 무엇을 할것인지
3. 데이터 준비(Data Preparation) : 데이터를 어떻게 구할지, 데이터 전처리
4. 모델링(Modelling) : 모델링 기법 선택, 테스트 설계 생성, 모델 생성
5. 평가(Evaluation) : 결과 평가
6. 배포(Deployment) : 배포 및 피드백

<br>

### colab에서 ipynb(interactive python notebook) 실행하기

[Google Colaboratory](https://colab.research.google.com/?hl=ko)

1. colab 링크 실행 후 업로드 버튼 클릭

<img width="1680" alt="스크린샷 2023-07-18 오후 2 14 39" src="https://github.com/kimbap918/TIL/assets/75712723/8c33739a-cfac-4ad1-ab41-06941e610756">

2. 실행할 ipynb 파일 선택

<img width="1680" alt="스크린샷 2023-07-18 오후 2 14 52 (2)" src="https://github.com/kimbap918/TIL/assets/75712723/575e1790-1cf3-4d96-bbe9-a3b7e4b83a7f">

3. 실행 화면

<img width="1680" alt="스크린샷 2023-07-18 오후 2 15 06" src="https://github.com/kimbap918/TIL/assets/75712723/be42072d-41a7-4cf8-ae30-e074e9f96652">

<br>

### colab의 특징

파이썬은 인터프리터로, 줄 단위로 실행이 된다.

1. colab의 코드 셀은 cell 단위로 실행이 된다.
2. (mac) 코드의 실행은 command + return, shift + return
3. 블럭의 `+ 코드` 혹은 `+ 텍스트`를 클릭하여 텍스트와 코드 입력이 가능하다.

<img width="851" alt="스크린샷 2023-07-18 오후 2 49 51" src="https://github.com/kimbap918/TIL/assets/75712723/2d444136-7fe7-4708-a553-a3d561a785e5">

<br>

### 데이터의 분류

정형 데이터와 비정형 데이터로 분류된다.

1. 정형 데이터(structured data)
- 데이터의 통계적 `특징`을 뽑아내기 쉬운 데이터
- 키, 체중, 몸무게 등의 데이터. 액셀에서 표 형식을 가지는 데이터

정형인 이유?

키, 체중, 몸무게의 캡션을 지우고 데이터만 남겨도 칼럼을 보면 이것이 키, 체중, 몸무게 값이 가지는 특징과 범위를 유추할 수 있다.

<br>

2. 비정형 데이터(Unstructured data)

- 데이터의 통계적 `특징`을 뽑아내기 어려운 데이터
- 사진, 비디오, 메일 데이터 등

비정형인 이유?

개의 사진, 동영상의 묶음이 있을 때 특정한 하나의 좌표를 전부 연결한다면 특정 좌표의 값에 해당하는 정보가 모두 달라 특징을 유추할 수 없다.   

<br>

[Google Colaboratory](https://colab.research.google.com/github/rickiepark/hg-da/blob/main/01-3.ipynb#scrollTo=a65810be)

### (링크의 01-3 중)데이터프레임 다루기: 판다스

```python
import pandas as pd
```

```python
# csv(comma separated value)
df = pd.read_csv('남산도서관 장서 대출목록 (2021년 04월).csv', encoding='euc-kr')
```

```python
# low_memory옵션은 대용량의 데이터를 불러오는 경우 각 칼럼의 데이터 타입(dtype)을 추측하는 것이 매우 많은 메모리를 사용하기 때문에 
# 대용량의 데이터를 불러올때 메모리 에러가 발생하는 경우 이를 False로 설정
df = pd.read_csv('남산도서관 장서 대출목록 (2021년 04월).csv', encoding='euc-kr', low_memory=False)
```

```python
df.head()
# 실행결과
```

| index | 번호 | 도서명 | 저자 | 출판사 | 발행년도 | ISBN | 세트 ISBN | 부가기호 | 권 | 주제분류번호 | 도서권수 | 대출건수 | 등록일자 | Unnamed: 13 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 1 | 인공지능과 흙 | 김동훈 지음 | 민음사 | 2021 | 9788937444319 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 1 | 2 | 가짜 행복 권하는 사회 | 김태형 지음 | 갈매나무 | 2021 | 9791190123969 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 2 | 3 | 나도 한 문장 잘 쓰면 바랄 게 없겠네 | 김선영 지음 | 블랙피쉬 | 2021 | 9788968332982 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 3 | 4 | 예루살렘 해변 | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021 | 9788970759906 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 4 | 5 | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음 | 김영사 | 2021 | 9788934990833 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |

```python
# ISBN이 로드시 숫자로 처리되므로 미리 string type로 지정 
# NaN = Not a Number
# 여기서 ISBN은 스칼라(단일차원인)값을 가진다. 남자 여자처럼 구분을 하기 위한 데이터지, 우선 순위를 가진 값(벡터 값)이 아니다.
df = pd.read_csv('남산도서관 장서 대출목록 (2021년 04월).csv', encoding='euc-kr', dtype={'ISBN' : str, '세트 ISBN' : str, '주제분류번호' : str})
df.head
```

```
<bound method NDFrame.head of             번호                    도서명                저자    출판사  발행년도  \
0            1                인공지능과 흙            김동훈 지음    민음사  2021   
1            2           가짜 행복 권하는 사회            김태형 지음   갈매나무  2021   
2            3  나도 한 문장 잘 쓰면 바랄 게 없겠네            김선영 지음   블랙피쉬  2021   
3            4                예루살렘 해변  이도 게펜 지음, 임재희 옮김  문학세계사  2021   
4            5  김성곤의 중국한시기행 : 장강·황하 편            김성곤 지음    김영사  2021   
...        ...                    ...               ...    ...   ...   
401677  401678                韓國現代詩大系            채만묵 編著  한국문화사  1996   
401678  401679                  뉴 웨이브        제임스 모나코 지음    한나래  1996   
401679  401680           (최인훈 장편소설)화두            최인훈 지음    민음사  1994   
401680  401681           독일 문학과 세계 문학            吳漢鎭 編著     벽호  1995   
401681  401682             참으로 소중한 생각            김일상 지음    동문사  1995   

                 ISBN        세트 ISBN 부가기호    권   주제분류번호  도서권수  대출건수  \
0       9788937444319            NaN  NaN  NaN      NaN     1     0   
1       9791190123969            NaN  NaN  NaN      NaN     1     0   
2       9788968332982            NaN  NaN  NaN      NaN     1     0   
3       9788970759906            NaN  NaN  NaN      NaN     1     0   
4       9788934990833            NaN  NaN  NaN      NaN     1     0   
...               ...            ...  ...  ...      ...   ...   ...   
401677  9788977352971  9788977352988  NaN    3  811.608     1     0   
401678  9788985367448  9788985367424  NaN    2   688.04     1     0   
401679  9788937401596  9788937401589  NaN    2    813.6     1     0   
401680  9788947700368  9788947700405  NaN    3   809.05     2     0   
401681  9788970610092  9788970610092    0    1    814.6     0     0   

              등록일자  Unnamed: 13  
0       2021-03-19          NaN  
1       2021-03-19          NaN  
2       2021-03-19          NaN  
3       2021-03-19          NaN  
4       2021-03-19          NaN  
...            ...          ...  
401677  1970-01-01          NaN  
401678  1970-01-01          NaN  
401679  1970-01-01          NaN  
401680  1970-01-01          NaN  
401681  1970-01-01          NaN  

[401682 rows x 14 columns]>
```

```python
df.to_csv('ns_202104.csv')
```

```python
# 파이썬의 컨테이너(container) 타입
# 하나 이상의 숫자나 문자열을 담고있다.
with open('ns_202104.csv') as f:
  for i in range(3):
    print(f.readline(), end='')

# 실행결과
```

```
,번호,도서명,저자,출판사,발행년도,ISBN,세트 ISBN,부가기호,권,주제분류번호,도서권수,대출건수,등록일자,Unnamed: 13
0,1,인공지능과 흙,김동훈 지음,민음사,2021,9788937444319,,,,,1,0,2021-03-19,
1,2,가짜 행복 권하는 사회,김태형 지음,갈매나무,2021,9791190123969,,,,,1,0,2021-03-19,
```

```python
ns_df = pd.read_csv('ns_202104.csv', low_memory=False)
ns_df.head
```

```
<bound method NDFrame.head of         Unnamed: 0      번호                    도서명                저자    출판사  \
0                0       1                인공지능과 흙            김동훈 지음    민음사   
1                1       2           가짜 행복 권하는 사회            김태형 지음   갈매나무   
2                2       3  나도 한 문장 잘 쓰면 바랄 게 없겠네            김선영 지음   블랙피쉬   
3                3       4                예루살렘 해변  이도 게펜 지음, 임재희 옮김  문학세계사   
4                4       5  김성곤의 중국한시기행 : 장강·황하 편            김성곤 지음    김영사   
...            ...     ...                    ...               ...    ...   
401677      401677  401678                韓國現代詩大系            채만묵 編著  한국문화사   
401678      401678  401679                  뉴 웨이브        제임스 모나코 지음    한나래   
401679      401679  401680           (최인훈 장편소설)화두            최인훈 지음    민음사   
401680      401680  401681           독일 문학과 세계 문학            吳漢鎭 編著     벽호   
401681      401681  401682             참으로 소중한 생각            김일상 지음    동문사   

        발행년도           ISBN        세트 ISBN 부가기호    권   주제분류번호  도서권수  대출건수  \
0       2021  9788937444319            NaN  NaN  NaN      NaN     1     0   
1       2021  9791190123969            NaN  NaN  NaN      NaN     1     0   
2       2021  9788968332982            NaN  NaN  NaN      NaN     1     0   
3       2021  9788970759906            NaN  NaN  NaN      NaN     1     0   
4       2021  9788934990833            NaN  NaN  NaN      NaN     1     0   
...      ...            ...            ...  ...  ...      ...   ...   ...   
401677  1996  9788977352971  9788977352988  NaN    3  811.608     1     0   
401678  1996  9788985367448  9788985367424  NaN    2   688.04     1     0   
401679  1994  9788937401596  9788937401589  NaN    2    813.6     1     0   
401680  1995  9788947700368  9788947700405  NaN    3   809.05     2     0   
401681  1995  9788970610092  9788970610092    0    1    814.6     0     0   

              등록일자  Unnamed: 13  
0       2021-03-19          NaN  
1       2021-03-19          NaN  
2       2021-03-19          NaN  
3       2021-03-19          NaN  
4       2021-03-19          NaN  
...            ...          ...  
401677  1970-01-01          NaN  
401678  1970-01-01          NaN  
401679  1970-01-01          NaN  
401680  1970-01-01          NaN  
401681  1970-01-01          NaN  

[401682 rows x 15 columns]>
```

```python
ns_df = pd.read_csv('ns_202104.csv', index_col=0, low_memory=False)
ns_df.head()
# 실행결과
```

|  | 번호 | 도서명 | 저자 | 출판사 | 발행년도 | ISBN | 세트 ISBN | 부가기호 | 권 | 주제분류번호 | 도서권수 | 대출건수 | 등록일자 | Unnamed: 13 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 1 | 인공지능과 흙 | 김동훈 지음 | 민음사 | 2021 | 9788937444319 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 1 | 2 | 가짜 행복 권하는 사회 | 김태형 지음 | 갈매나무 | 2021 | 9791190123969 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 2 | 3 | 나도 한 문장 잘 쓰면 바랄 게 없겠네 | 김선영 지음 | 블랙피쉬 | 2021 | 9788968332982 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 3 | 4 | 예루살렘 해변 | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021 | 9788970759906 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |
| 4 | 5 | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음 | 김영사 | 2021 | 9788934990833 | NaN | NaN | NaN | NaN | 1 | 0 | 2021-03-19 | NaN |

```python
# df를 csv로 변환, index는 포함하지 않는다.
df.to_csv('ns_202104.csv', index=False)

# xlsxwriter 라이브러리 설치
!pip install xlsxwriter

# ns_df를 엑셀로 변환
ns_df.to_excel('ns_202104.xlsx', index=False, engine='xlsxwriter')
```

<br>

[Google Colaboratory](https://colab.research.google.com/github/rickiepark/hg-da/blob/main/03-1.ipynb)

### (03-1) 불필요한 데이터 삭제하기

```prolog
import gdown

# quiet = False : 실행 후 프로그레시브 바를 출력하지 않으려면 True
gdown.download('https://bit.ly/3RhoNho', 'ns_202104.csv', quiet=False)
```

```
Downloading...
From: https://bit.ly/3RhoNho
To: /content/ns_202104.csv
100%|██████████| 57.6M/57.6M [00:00<00:00, 113MB/s]
'ns_202104.csv
```

```python
import pandas as pd

# 데이터를 전처리할때 가장 많이 쓰는 라이브러리
# numpy, pandas
ns_df = pd.read_csv('ns_202104.csv', low_memory=False)
ns_df.head()
```

|      | 번호 | 도서명                               | 저자                        | 출판사     | 발행년도 | ISBN          | 세트 ISBN | 부가기호 | 권   | 주제분류번호 | 도서권수 | 대출건수 | 등록일자   | Unnamed: 13 |
| ---- | ---- | ------------------------------------ | --------------------------- | ---------- | -------- | ------------- | --------- | -------- | ---- | ------------ | -------- | -------- | ---------- | ----------- |
| 0    | 1    | 인공지능과 흙                        | 김동훈 지음                 | 민음사     | 2021     | 9788937444319 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 1    | 2    | 가짜 행복 권하는 사회                | 김태형 지음                 | 갈매나무   | 2021     | 9791190123969 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 2    | 3    | 나도 한 문장 잘 쓰면 바랄 게 없겠네  | 김선영 지음                 | 블랙피쉬   | 2021     | 9788968332982 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 3    | 4    | 예루살렘 해변                        | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021     | 9788970759906 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 4    | 5    | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음                 | 김영사     | 2021     | 9788934990833 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |

```python
# 리스트 슬라이싱 : 리스트 내의 값을 특정부분 잘라내는 것, ['번호':'등록일자']는 '번호'에서 '등록일자' 까지 잘라서 저장하도록 지정 
# 컨테이너 타입의 3가지
# 1. 리스트(list), 2. 튜플(tuple), 3. 딕셔너리(dictionary)
# 여기서 인공지능에 가장 많이 사용하는 타입은 리스트다. 
# 리스트는 [] 대괄호로 묶여있다.
# 튜플은 () 소괄호로 묶여있다.
# 딕셔너리는 {} 중괄호로 묶여있다.

ns_book = ns_df.loc[:, '번호':'등록일자']
ns_book.head()
```

|      | 번호 | 도서명                               | 저자                        | 출판사     | 발행년도 | ISBN          | 세트 ISBN | 부가기호 | 권   | 주제분류번호 | 도서권수 | 대출건수 | 등록일자   |
| ---- | ---- | ------------------------------------ | --------------------------- | ---------- | -------- | ------------- | --------- | -------- | ---- | ------------ | -------- | -------- | ---------- |
| 0    | 1    | 인공지능과 흙                        | 김동훈 지음                 | 민음사     | 2021     | 9788937444319 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 1    | 2    | 가짜 행복 권하는 사회                | 김태형 지음                 | 갈매나무   | 2021     | 9791190123969 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 2    | 3    | 나도 한 문장 잘 쓰면 바랄 게 없겠네  | 김선영 지음                 | 블랙피쉬   | 2021     | 9788968332982 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 3    | 4    | 예루살렘 해변                        | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021     | 9788970759906 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 4    | 5    | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음                 | 김영사     | 2021     | 9788934990833 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |

```python
print(ns_df.columns)

-> Index(['번호', '도서명', '저자', '출판사', '발행년도', 'ISBN', '세트 ISBN', '부가기호', '권',
       '주제분류번호', '도서권수', '대출건수', '등록일자', 'Unnamed: 13'],
      dtype='object')
```

```python
print(ns_df.columns[0])

-> 번호
```

```python
# Unnamed: 13과 같지 않은지 확인, True는 같지 않다.
ns_df.columns != 'Unnamed: 13'

-> array([ True,  True,  True,  True,  True,  True,  True,  True,  True,
        True,  True,  True,  True, False])
```

```python
# ns_df의 Unnamed: 13이 아닌 칼럼을 찾아서 selected_columns에 저장
selected_columns = ns_df.columns != 'Unnamed: 13'
ns_book = ns_df.loc[:, selected_columns]
ns_book.head()
```

|      | 번호 | 도서명                               | 저자                        | 출판사     | 발행년도 | ISBN          | 세트 ISBN | 부가기호 | 권   | 주제분류번호 | 도서권수 | 대출건수 | 등록일자   |
| ---- | ---- | ------------------------------------ | --------------------------- | ---------- | -------- | ------------- | --------- | -------- | ---- | ------------ | -------- | -------- | ---------- |
| 0    | 1    | 인공지능과 흙                        | 김동훈 지음                 | 민음사     | 2021     | 9788937444319 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 1    | 2    | 가짜 행복 권하는 사회                | 김태형 지음                 | 갈매나무   | 2021     | 9791190123969 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 2    | 3    | 나도 한 문장 잘 쓰면 바랄 게 없겠네  | 김선영 지음                 | 블랙피쉬   | 2021     | 9788968332982 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 3    | 4    | 예루살렘 해변                        | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021     | 9788970759906 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 4    | 5    | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음                 | 김영사     | 2021     | 9788934990833 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |

```python
selected_columns = ns_df.columns != '부가기호'
ns_book = ns_df.loc[:, selected_columns]
ns_book.head()
```

|      | 번호 | 도서명                               | 저자                        | 출판사     | 발행년도 | ISBN          | 세트 ISBN | 권   | 주제분류번호 | 도서권수 | 대출건수 | 등록일자   | Unnamed: 13 |
| ---- | ---- | ------------------------------------ | --------------------------- | ---------- | -------- | ------------- | --------- | ---- | ------------ | -------- | -------- | ---------- | ----------- |
| 0    | 1    | 인공지능과 흙                        | 김동훈 지음                 | 민음사     | 2021     | 9788937444319 | NaN       | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 1    | 2    | 가짜 행복 권하는 사회                | 김태형 지음                 | 갈매나무   | 2021     | 9791190123969 | NaN       | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 2    | 3    | 나도 한 문장 잘 쓰면 바랄 게 없겠네  | 김선영 지음                 | 블랙피쉬   | 2021     | 9788968332982 | NaN       | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 3    | 4    | 예루살렘 해변                        | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021     | 9788970759906 | NaN       | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |
| 4    | 5    | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음                 | 김영사     | 2021     | 9788934990833 | NaN       | NaN  | NaN          | 1        | 0        | 2021-03-19 | NaN         |

```python
# axis = 1, 칼럼 기준으로 drop
ns_book = ns_df.drop('Unnamed: 13', axis=1)
ns_book.head()
```

|      | 번호 | 도서명                               | 저자                        | 출판사     | 발행년도 | ISBN          | 세트 ISBN | 부가기호 | 권   | 주제분류번호 | 도서권수 | 대출건수 | 등록일자   |
| ---- | ---- | ------------------------------------ | --------------------------- | ---------- | -------- | ------------- | --------- | -------- | ---- | ------------ | -------- | -------- | ---------- |
| 0    | 1    | 인공지능과 흙                        | 김동훈 지음                 | 민음사     | 2021     | 9788937444319 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 1    | 2    | 가짜 행복 권하는 사회                | 김태형 지음                 | 갈매나무   | 2021     | 9791190123969 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 2    | 3    | 나도 한 문장 잘 쓰면 바랄 게 없겠네  | 김선영 지음                 | 블랙피쉬   | 2021     | 9788968332982 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 3    | 4    | 예루살렘 해변                        | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021     | 9788970759906 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |
| 4    | 5    | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음                 | 김영사     | 2021     | 9788934990833 | NaN       | NaN      | NaN  | NaN          | 1        | 0        | 2021-03-19 |

```python
# inplace = True
# 주제분류번호를 칼럼 기준으로(1) drop하고, 반영(inplace)한다.
ns_book.drop('주제분류번호', axis=1, inplace=True)
ns_book.head()
```

|      | 번호 | 도서명                               | 저자                        | 출판사     | 발행년도 | ISBN          | 세트 ISBN | 권   | 도서권수 | 대출건수 | 등록일자   |
| ---- | ---- | ------------------------------------ | --------------------------- | ---------- | -------- | ------------- | --------- | ---- | -------- | -------- | ---------- |
| 0    | 1    | 인공지능과 흙                        | 김동훈 지음                 | 민음사     | 2021     | 9788937444319 | NaN       | NaN  | 1        | 0        | 2021-03-19 |
| 1    | 2    | 가짜 행복 권하는 사회                | 김태형 지음                 | 갈매나무   | 2021     | 9791190123969 | NaN       | NaN  | 1        | 0        | 2021-03-19 |
| 2    | 3    | 나도 한 문장 잘 쓰면 바랄 게 없겠네  | 김선영 지음                 | 블랙피쉬   | 2021     | 9788968332982 | NaN       | NaN  | 1        | 0        | 2021-03-19 |
| 3    | 4    | 예루살렘 해변                        | 이도 게펜 지음, 임재희 옮김 | 문학세계사 | 2021     | 9788970759906 | NaN       | NaN  | 1        | 0        | 2021-03-19 |
| 4    | 5    | 김성곤의 중국한시기행 : 장강·황하 편 | 김성곤 지음                 | 김영사     | 2021     | 9788934990833 | NaN       | NaN  | 1        | 0        | 2021-03-19 |

```python
# NaN이 들어있는 칼럼을 drop
ns_book = ns_df.dropna(axis=1)
ns_book.head()
```

|      | 번호 | ISBN          | 도서권수 | 대출건수 | 등록일자   |
| ---- | ---- | ------------- | -------- | -------- | ---------- |
| 0    | 1    | 9788937444319 | 1        | 0        | 2021-03-19 |
| 1    | 2    | 9791190123969 | 1        | 0        | 2021-03-19 |
| 2    | 3    | 9788968332982 | 1        | 0        | 2021-03-19 |
| 3    | 4    | 9788970759906 | 1        | 0        | 2021-03-19 |
| 4    | 5    | 9788934990833 | 1        | 0        | 2021-03-19 |

<br>



### (참고)파이썬 기초 AI 강의

[파이선으로 배우는 AI 기초](https://www.ebssw.kr/lrnng/alctcr/alctcrDetailView.do?alctcrSn=57835)