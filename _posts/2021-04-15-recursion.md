---
layout: post
title: Recursion
subititle: 재귀 방법, 대충 이해는 되는데 구현이 어렵다면?
categories: Algorithm
tags: [Algorithm]
---
구글링을 통해 이해했다고 생각했는데 막상 코딩테스트에 가면 구현이 어렵더라구요.  
그래서 오늘도 **Hello Coding 그림으로 개념을 이해하는 알고리즘(아디트야 바르가바, 한빛미디어)** 책과 **정보처리기사 필기(길벗)** 책을 통해 좀 더 깊이 공부했습니다.  

## 필요성
생각하는대로 손코딩을 하다보면 어느새 같은 기능을 반복해서 적는 구간이 생깁니다.  
저는 이럴때마다 recursion(재귀)을 떠올리면서 def recursion을 정의하고 코드를 간결하게 만들려고 합니다.  
하지만 재귀 방법 구현 경험이 전무하다보니 자주 error가 생기면서 당황했습니다.  
이번 기회에 완벽히 이해해서 앞으로 복잡한 데이터 분석 코드를 작성할 때도 재귀를 멋지게 적용하려 합니다!  

## 정의
Recursion 함수는 결과를 return하기 전에 자기 자신을 호출하는 방법입니다.  

## 구성
재귀 함수를 작성할 때는 무한 반복을 막기위한 **기본 단계**와 **재귀 단계**를 넣어주면 됩니다.  
### 예시
새해를 기다리는 카운트다운을 하는 재귀함수를 다음과 같이 나타낼 수 있습니다.  

```python
def countdown(i):
   if i<2:
      return i   #기본 단계
   else:
      countdown(i-1)   #재귀 단계 
```
## 호출 순서 이해하기
재귀 함수는 컴퓨터에서 어떤 방식으로 이해되고 있는 걸까요?  
이 질문에 답하기 위해서는 data structure(자료 구조) linear structure(선형 구조)에 속하는 [stack][1] (스택)에 대한 이해가 필요합니다.  

  [1]: https://dasolu.github.io/basic/2021/04/15/data-structure-stack.html 