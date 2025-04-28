<!--
Meta Description: # R의 mapply: 다중 인자 함수 적용하기 ## 개요 R의 `mapply` 함수는 여러 개의 벡터 또는 리스트를 동시에 입력으로 받아 사용자 정의 함수를 적용하는 데 사용됩니다. 이는 반복적인 작업을 간결하게 처리할 수 있도록 도와줍니다. ## 문서화 ### 목적...
Meta Keywords: mapply, result, 인자를, simplify, true
-->

# R의 mapply: 다중 인자 함수 적용하기

## 개요
R의 `mapply` 함수는 여러 개의 벡터 또는 리스트를 동시에 입력으로 받아 사용자 정의 함수를 적용하는 데 사용됩니다. 이는 반복적인 작업을 간결하게 처리할 수 있도록 도와줍니다.

## 문서화
### 목적
`mapply`는 다중 인자를 가진 함수에 대해 벡터화된 방식으로 여러 개의 인자를 동시에 적용할 수 있도록 설계된 함수입니다. 이는 주로 데이터 변환이나 계산을 효율적으로 수행하는 데 유용합니다.

### 사용법
```R
mapply(FUN, ..., MoreArgs = NULL, SIMPLIFY = TRUE, USE.NAMES = TRUE)
```

- **FUN**: 적용할 함수
- **...**: 함수에 전달할 벡터 또는 리스트
- **MoreArgs**: FUN에 추가로 전달할 인자
- **SIMPLIFY**: 결과를 간단한 형태로 반환할지 여부 (기본값: TRUE)
- **USE.NAMES**: 결과에 이름을 사용할지 여부 (기본값: TRUE)

### 세부사항
- `mapply`는 기본적으로 `lapply`와 유사하지만, 다중 인자를 처리할 수 있다는 점에서 차별화됩니다.
- 결과 형식은 `SIMPLIFY` 인자에 따라 달라지며, 기본값이 TRUE일 경우 결과는 가능한 한 간단한 형태로 반환됩니다.

## 예제
### 예제 1: 두 벡터의 합
```R
x <- c(1, 2, 3)
y <- c(4, 5, 6)
result <- mapply(sum, x, y)
print(result)  # 출력: 5 7 9
```

### 예제 2: 사용자 정의 함수 사용
```R
multiply <- function(a, b) {
  return(a * b)
}

x <- c(1, 2, 3)
y <- c(4, 5, 6)
result <- mapply(multiply, x, y)
print(result)  # 출력: 4 10 18
```

### 예제 3: 추가 인자 사용
```R
power <- function(base, exponent) {
  return(base ^ exponent)
}

x <- c(2, 3, 4)
y <- c(3, 2, 1)
result <- mapply(power, x, y)
print(result)  # 출력: 8 9 4
```

## 설명
`mapply`를 사용할 때 몇 가지 주의할 점이 있습니다. 
- 입력된 벡터의 길이가 다를 경우, 가장 긴 벡터의 길이에 맞춰 반복되므로 예상치 못한 결과가 나올 수 있습니다.
- `SIMPLIFY` 인자를 FALSE로 설정하면 결과가 리스트 형태로 반환되어, 다음 단계에서의 데이터 처리에 유용할 수 있습니다.

## 한 줄 요약
R의 `mapply` 함수는 여러 벡터나 리스트에 대해 사용자 정의 함수를 동시에 적용할 수 있는 효율적인 방법입니다.