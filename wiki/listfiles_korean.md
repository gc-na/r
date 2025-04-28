<!--
Meta Description: # R의 list.files 함수: 파일 목록 가져오기 ## 개요 R의 `list.files` 함수는 특정 디렉토리 내의 파일 목록을 가져오는 데 사용됩니다. 이 함수는 데이터 분석 작업에서 데이터 파일을 로드하거나 관리할 때 유용합니다. ## 문서 `list.file...
Meta Keywords: files, list, 디렉토리, true로, 설정하면
-->

# R의 list.files 함수: 파일 목록 가져오기

## 개요
R의 `list.files` 함수는 특정 디렉토리 내의 파일 목록을 가져오는 데 사용됩니다. 이 함수는 데이터 분석 작업에서 데이터 파일을 로드하거나 관리할 때 유용합니다.

## 문서
`list.files` 함수는 주어진 디렉토리의 파일 및 디렉토리 이름을 벡터 형태로 반환합니다. 이 함수는 다양한 인자를 통해 결과를 필터링하고 정렬할 수 있습니다.

### 목적
- 특정 디렉토리 내의 파일 목록을 쉽게 가져올 수 있도록 합니다.

### 사용법
```R
list.files(path = ".", pattern = NULL, all.files = FALSE, full.names = FALSE, recursive = FALSE, ignore.case = FALSE, include.dirs = FALSE, no.. = FALSE)
```

### 매개변수
- **path**: 파일 목록을 가져올 디렉토리 경로. 기본값은 현재 작업 디렉토리입니다.
- **pattern**: 정규 표현식으로, 반환할 파일 이름을 필터링합니다.
- **all.files**: TRUE로 설정하면 숨김 파일도 포함하여 반환합니다.
- **full.names**: TRUE로 설정하면 전체 경로를 포함하여 반환합니다.
- **recursive**: TRUE로 설정하면 하위 디렉토리 내의 파일도 검색합니다.
- **ignore.case**: TRUE로 설정하면 대소문자를 무시하고 검색합니다.
- **include.dirs**: TRUE로 설정하면 디렉토리 이름도 반환합니다.
- **no..**: TRUE로 설정하면 상위 디렉토리(`..`)를 제외합니다.

## 예제
1. 현재 디렉토리의 모든 파일 목록 가져오기:
   ```R
   files <- list.files()
   print(files)
   ```

2. 특정 디렉토리의 파일 목록 가져오기:
   ```R
   files <- list.files(path = "data/")
   print(files)
   ```

3. 특정 패턴으로 필터링된 파일 목록 가져오기:
   ```R
   txt_files <- list.files(pattern = "\\.txt$")
   print(txt_files)
   ```

4. 전체 경로 포함하여 파일 목록 가져오기:
   ```R
   full_files <- list.files(full.names = TRUE)
   print(full_files)
   ```

5. 하위 디렉토리의 파일도 포함하여 가져오기:
   ```R
   all_files <- list.files(recursive = TRUE)
   print(all_files)
   ```

## 설명
`list.files` 함수는 매우 유용하지만, 다음과 같은 주의사항이 있습니다:
- **경로 오류**: 잘못된 경로를 입력하면 빈 벡터가 반환됩니다. 경로를 정확히 확인하세요.
- **정규 표현식**: `pattern` 매개변수를 사용할 때 올바른 정규 표현식을 사용해야 합니다. 잘못된 패턴은 예기치 않은 결과를 초래할 수 있습니다.
- **숨김 파일 포함**: `all.files`를 TRUE로 설정하면 숨김 파일도 포함되므로, 필요에 따라 설정을 조정해야 합니다.
- **대소문자 구분**: `ignore.case`를 TRUE로 설정하지 않으면 대소문자가 구분됩니다.

## 한 줄 요약
`list.files` 함수는 특정 디렉토리 내의 파일 목록을 가져오는 유용한 R 함수입니다.