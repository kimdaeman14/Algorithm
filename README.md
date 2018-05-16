# Algorithm 

# 1강. 컴퓨터 알고리즘의 정의

## `문제`를 `효율적`이게 `단계적`으로 `해결`하는 방법

- 컴퓨터 언어
	- 컴퓨터와 대화하기 위해서 사용하는 언어
	- C, C++, C#, Jaca, Python
- 컴퓨터 알고리즘
	- 컴퓨터를 이용하여 주어진 문제를 풀기 위한 방법이나 절차
	- 정렬알고리즘, 해시알고리즘, 최단거리알고리즘 등 
- 컴퓨터 프로그램
	- 컴퓨터가 특정 작업을 수행하기 위해 짜여진 명령의 순서 ~~

*컴퓨터는 ~~바보~~ 아니 ``저장&&계산의 천재``다. 
**어떻게 하면 돈을 벌 수 있나요?**
**오래 살려면 어떻게 해야 하나요?** 
아무리 물어봐도 컴퓨터는 대답을 하지 못합니다. 대답을 얻기 위해서는 그에 맞는 방법을 
단계별로 구현을 해준 뒤에 물어봐야 답을얻을 수 있습니다.*


#### 우리집에서 학원까지 가는 알고리즘

````
1. 집을 나선다
2. 대로변으로 이동한다
3. ``빈차``라고 표시된 택시를 확인한다
4. 택시기사에게 택시를 타겠다는 의사를 전달한다 
5. 목적지를 말한다 
6. 목적지까지 이동한다
7. 요금을 지불하고 내린다
8. 학원까지 걸어간다 
````


택시, 지하철, 버스, 자전거, 걸어서 등 다양한 방법이 존재하는데, 여기서 가장 빠른방법은 
무엇이고 가장 비용이 적게 드는 방법은 무엇인가 ? 

- 컴퓨터 알고리즘을 설명하기 위한 4단계
	- 문제 정의 problem definition
		- 해결하고자 하는 문제는 무엇인가를 명확하게 설명하는 것 
		- 입력과 출력의 형태로 정의하는 것
		- 컴퓨터가 수행할 수 있는 형태로 전환이 가능하는지의 여부 
	- 알고리즘 설명 algorithm description
		- 컴퓨터가 수행해야 할 내용을 하나씩 차례대로 정의한 과정
		
		````
		1. 라면끓이기
		2. 냄비에 물 500ml를 넣고, 가스레인지에 올려라
		3. 물이 끓을 때까지 기다려라
		4. 준비된 라면과 재료를 넣고 3분을 기다려라 
		5. 맛있게 먹어라
		````
		
	- 정확성 증명 correctness proof
		- 과정대로 수행하면 항상 올바른 답을 내보내는가 ? 
		- 잘못된 답을 내보내는 경우는 없는가 ? 
		- 올바른 출력을 내보내고 정상적으로 종료되는가 ? 
	- 성능 분석 performance analysis
		- 수행시간 running time
		- 사용공간 space consumption
	

# 2강. 컴퓨터 알고리즘의 개요

#### 컴퓨터 알고리즘을 설명하기 위한 4단계
	- 문제정의 : 어떤 자료를 입력으로 넣어주고 어떤 자료를 출력으로 넣어줄건지 명확하게 설정할 것
	- 알고리즘 설명 : 과정을 단계적으로 설명(ex:요리) 
	- 정확성 증명 : 이 알고리즘을 쓰면 정확한 성능을 내준다는 것을 확인
	- 성능 분석 : 문제를 어떻게하면 좀더 효율적으로 해결할 수 있을 것인가

**성능 분석**
- 특정 기계에서 수행시간을 측정하는 것은 공정하지 않다. 
- 조건이 동일한 특정기계에서 측정해야하는데 사실상 불가능하다. 
- 따라서, `수행연산 횟수`를 비교하는 방식으로 성능을 분석한다.

![image](https://user-images.githubusercontent.com/34432988/40132627-4979d4e8-5978-11e8-9724-0d0742b93169.png)

- 컴퓨터 알고리즘의 수행시간 분석 
	- 수행시간은 입력으로 크기가 커지면 커질수록 시간이 많이 걸린다.
	- 따라서 수행시간은 입력크기 n에 대한 함수로 표현한다. 
		
1. 성능 분석의 비교 대상
	- 산술연산 : add, multiply, exponent, modular, ...
	- 데이터입출력 : copy, move, save, load, ...
	- 제어 연산 : if, while, register, ...
	
2. 점근적 표기법 
	- 빅오 표기 : n이라는 값에 대해서 y축인 시간이 얼마나 걸린다를 표시하고 있는 것이고, 아무리 느려져도 상한선인 cg(n)보다 높아질 수 없다.
	
	![image](https://user-images.githubusercontent.com/34432988/40133143-db16789c-5979-11e8-93b3-d9ebc2294c21.png)

	![image](https://user-images.githubusercontent.com/34432988/40133355-6ed482b8-597a-11e8-88ca-72813704309b.png)

	- 오메가 표기 : 반대로 f(n)이 n이 어떻게 변한다고 하더라도 하한선인 cg(n)보다 내려갈 수 없다. 
	  	
		     `3n^2-4n+1=오메가(n)`
	
	![image](https://user-images.githubusercontent.com/34432988/40133530-08e34c72-597b-11e8-81f6-9c658332b224.png)
	
	- 쎄타 표기 : 빅오와 오메가표기를 같이 쓰는 것. 
		
	![image](https://user-images.githubusercontent.com/34432988/40133497-f147c89a-597a-11e8-8cb1-f92628628f86.png)


# 3강. 정렬 문제 

1. 정렬문제의 정의 
	- 정렬문제 sorting problem : n 개의 숫자들을 입력받아서 그것들이 점점 커지는,작아지는 순서를 다시 나열받아서 출력으로 내보내는 것.
		-입력 input : n 개의 숫자들의 배열 
		-출력 output : 입력된 숫자들의 배열이 어떤 조건을 만족하도록 다시 나열한 결과
		
		` 인풋 5, 2, 4, 6, 1, 3 으로 들어왔으면 `
		` 아웃풋으로 1, 2, 3, 4, 5, 6 으로 출력 ` 
		
		위와같이 됐다면 정렬문제가 해결됐다 라고 할 수 있을 것.
		
2. 선택정렬 알고리즘 
	- 선택정렬 selection sort
		- 선택하여 정렬하는 알고리즘
		1. 선택할 때 뭐를 선택하는지가 가장 중요하다.
		2. 최소값 선택(오름차순) 또는 최대값 선택(내림차순)
			- 최소값 선택 정렬
			1. 정렬되지 않은 숫자 중에 가장 작은 숫자 선택
			2. 선택된 숫자를 정렬되지 않은 숫자들 중 첫번째 숫자와 자리를 바꾸면 선택된 숫자는 정렬된 것이다.
			3. 모든 숫자를 옮길 때까지 1-2번 과정을 반복한다. 
			
			
![image](https://user-images.githubusercontent.com/34432988/40134389-3a72ba28-597d-11e8-8f6d-dc1026a5d331.png)


	- 정확성 증명
	1. 수학적 귀납법을 이용
	2. i번째 선택한 숫자가 i번째로작은(혹은큰) 숫자인지를 증명
	
	- 성능분석
	1. 하나를찝고 다른거랑 비교를 몇번하는지를 보면 해당 함수의 성능이 된다.
			
			






*기울이기*

**찐하게**

`단어강조`

[링크](http://naver.com)

![이미지삽입](https://a.disquscdn.com/1525719473/images/noavatar92.png)

~~썼다지우기~~

- 리스트1
- 리스트2
- 리스트3

1. 리스트1
2. 리스트2
3. 리스트3

- [ ] 체크박스
- [ ] 체크박스
- [x] 체크박스 선택
  
 > 주석사용
 >> 주석응용
 > *주석안에단어**강조**도 된다*.


	코드는 띄어쓰기 4번 앞뒤로 
	또는 백쿼드 앞뒤로 3개
	또는 ~~~물결표 앞뒤로 3개
	입니다. 아 그리고 이런식으로 
	위아래에 입력하고 줄바꿔서 
	코드 넣는게 보기 좋아요.
	띄어쓰기를 한건지 안한건지 
	모르니까 다른걸로도 다시한번
		
```
