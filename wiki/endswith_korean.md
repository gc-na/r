<!--
Meta Description: # R의 endsWith 함수: 문자열 끝 비교하기 ## 개요 `endsWith` 함수는 R에서 문자열이 특정 접미사로 끝나는지를 확인하는 데 사용됩니다. 이 함수는 데이터 처리 및 텍스트 분석 작업에서 유용하게 활용됩니다. ## 문서화 `endsWith` 함수는 주어...
Meta Keywords: 문자열, endswith, true, 함수는, false
-->

# R의 endsWith 함수: 문자열 끝 비교하기

## 개요
`endsWith` 함수는 R에서 문자열이 특정 접미사로 끝나는지를 확인하는 데 사용됩니다. 이 함수는 데이터 처리 및 텍스트 분석 작업에서 유용하게 활용됩니다.

## 문서화
`endsWith` 함수는 주어진 문자열 벡터 내의 각 문자열이 지정된 접미사로 끝나는지를 논리값(TRUE 또는 FALSE)의 배열로 반환합니다. 이 함수는 주로 데이터 필터링 및 조건부 검사에 사용됩니다.

### 사용법
```R
endsWith(x, suffix)
```

#### 매개변수
- `x`: 문자열 벡터
- `suffix`: 확인할 접미사 문자열 (단일 문자열 또는 문자열 벡터)

#### 반환값
- 논리값 벡터: 각 문자열이 지정된 접미사로 끝나는 경우 TRUE, 그렇지 않으면 FALSE를 반환합니다.

### 예제
```R
# 예제 문자열 벡터
strings <- c("apple", "banana", "cherry", "date")

# 'e'로 끝나는 문자열 확인
result <- endsWith(strings, "e")
print(result)  # [1] TRUE FALSE FALSE TRUE

# 'a'로 끝나는 문자열 확인
result2 <- endsWith(strings, "a")
print(result2)  # [1] FALSE TRUE FALSE TRUE
```

## 설명
`endsWith` 함수를 사용할 때 주의할 점은 접미사는 반드시 문자열 형식이어야 하며, 벡터로 전달할 경우 각 문자열에 대해 개별적으로 검사됩니다. 또한, 대소문자를 구분하기 때문에 정확한 접미사를 입력해야 합니다. 예를 들어, "apple"과 "Apple"은 서로 다르게 인식됩니다. 다른 문자열 처리 함수와 함께 사용하여 보다 복잡한 문자열 처리가 가능합니다.

## 한 줄 요약
`endsWith` 함수는 R에서 주어진 문자열이 특정 접미사로 끝나는지를 확인하는 유용한 함수입니다.