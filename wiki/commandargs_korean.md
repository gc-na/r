<!--
Meta Description: # R의 commandArgs 함수: 커맨드 라인 인자 처리하기 ## 개요 `commandArgs` 함수는 R에서 커맨드 라인 인자를 가져오는 데 사용됩니다. 이 함수는 스크립트 실행 시 외부에서 전달된 인자를 효과적으로 처리할 수 있게 해줍니다. ## 문서화 ### ...
Meta Keywords: commandargs, 스크립트, 커맨드, 인자를, 있습니다
-->

# R의 commandArgs 함수: 커맨드 라인 인자 처리하기

## 개요
`commandArgs` 함수는 R에서 커맨드 라인 인자를 가져오는 데 사용됩니다. 이 함수는 스크립트 실행 시 외부에서 전달된 인자를 효과적으로 처리할 수 있게 해줍니다.

## 문서화
### 목적
`commandArgs` 함수는 R 스크립트가 실행될 때 외부에서 전달된 인수를 접근할 수 있도록 해줍니다. 이를 통해 사용자나 다른 프로그램이 스크립트에 인자를 전달하여 동적으로 실행할 수 있습니다.

### 사용법
```R
commandArgs(trailingOnly = FALSE)
```

- **trailingOnly**: 논리값으로, `TRUE`일 경우 스크립트 이름 이후의 인자만 반환합니다. 기본값은 `FALSE`입니다.

### 세부 사항
- `commandArgs`는 커맨드 라인에서 실행된 R 스크립트의 인자를 문자열 벡터 형식으로 반환합니다.
- 반환되는 첫 번째 요소는 스크립트의 경로이며, 나머지 요소는 사용자가 입력한 인자입니다.
- 주로 스크립트를 자동화하거나 배치 처리할 때 유용하게 사용됩니다.

## 예제
### 기본 사용 예
```R
# 스크립트 파일명: example.R
args <- commandArgs(trailingOnly = TRUE)
print(args)
```
위 스크립트를 커맨드 라인에서 다음과 같이 실행하면:
```bash
Rscript example.R arg1 arg2
```
출력은 다음과 같습니다:
```
[1] "arg1" "arg2"
```

### 스크립트 이름 포함 예
```R
# 스크립트 파일명: example_with_name.R
args <- commandArgs(trailingOnly = FALSE)
print(args)
```
커맨드 라인에서 실행 시:
```bash
Rscript example_with_name.R arg1 arg2
```
출력은 다음과 같습니다:
```
[1] "example_with_name.R" "arg1" "arg2"
```

## 설명
- **커맨드 라인 인자 처리**: `commandArgs`를 사용할 때, `trailingOnly` 인자의 설정에 따라 반환되는 인자의 수가 달라질 수 있습니다. `TRUE`로 설정하면 스크립트 이름을 제외한 인자만 가져오고, `FALSE`로 설정하면 모든 인자를 포함합니다.
- **스크립트 자동화**: 이 함수를 이용하면, 다양한 입력 인자를 통해 스크립트를 유연하게 조정할 수 있습니다. 예를 들어, 데이터 파일 경로를 인자로 전달하여 처리할 수 있습니다.
- **에러 처리**: 입력된 인자가 예상과 다를 경우, 스크립트 실행 중 에러가 발생할 수 있습니다. 따라서 인자 수와 형식을 사전 확인하는 것이 중요합니다.

## 한 줄 요약
`commandArgs` 함수는 R 스크립트에서 커맨드 라인 인자를 효과적으로 처리하는 기능을 제공합니다.