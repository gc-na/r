# [리눅스] C Shell (csh) jobs 사용법: 작업 목록 확인하기

## Overview
`jobs` 명령은 현재 셸 세션에서 실행 중인 작업의 목록을 보여줍니다. 이 명령은 백그라운드에서 실행 중인 프로세스와 포그라운드에서 실행 중인 프로세스를 확인하는 데 유용합니다.

## Usage
기본 구문은 다음과 같습니다:
```
jobs [options] [arguments]
```

## Common Options
- `-l`: 각 작업의 프로세스 ID(PID)를 포함하여 출력합니다.
- `-n`: 최근에 상태가 변경된 작업만 표시합니다.
- `-p`: 작업의 프로세스 ID만 출력합니다.

## Common Examples
- 현재 실행 중인 작업 목록 보기:
    ```csh
    jobs
    ```

- 각 작업의 프로세스 ID와 함께 목록 보기:
    ```csh
    jobs -l
    ```

- 최근에 상태가 변경된 작업만 보기:
    ```csh
    jobs -n
    ```

- 작업의 프로세스 ID만 출력하기:
    ```csh
    jobs -p
    ```

## Tips
- `jobs` 명령은 백그라운드에서 실행 중인 작업을 관리할 때 유용합니다. 예를 들어, `bg` 또는 `fg` 명령과 함께 사용하여 작업을 재개할 수 있습니다.
- 작업 목록을 확인한 후, 필요에 따라 특정 작업을 종료할 수 있습니다. 이를 위해 `kill` 명령을 사용하여 프로세스 ID를 지정할 수 있습니다.
- 작업이 많을 경우, `jobs -l` 옵션을 사용하여 각 작업의 PID를 확인하면 더 쉽게 관리할 수 있습니다.