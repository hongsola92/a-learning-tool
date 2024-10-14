## 파일 처리 코드

### 📅 24.10.14.

### 파일 처리 기본 개념
- **파일 읽기 (Read File)**: 파일 경로를 입력받아 파일의 내용을 읽어오는 기능.
- **파일 쓰기 (Write File)**: 데이터를 파일에 기록하는 기능.
- **파일 복사 (Copy File)**: 파일을 다른 위치로 복사하는 기능.
- **파일 이동 (Move File)**: 파일을 지정된 경로로 이동하는 기능.
- **파일 삭제 (Delete File)**: 파일을 삭제하는 기능.

### 파일 처리 기능
- **파일 읽기**:
    - 지정된 파일 경로에서 파일을 읽어오며, 파일이 존재하지 않으면 오류를 발생시킴.
    - 예제 코드:
    ```python
    def read_file(file_path):
        with open(file_path, 'r') as file:
            return file.read()
    ```

- **파일 쓰기**:
    - 데이터를 지정된 파일 경로에 저장하며, 파일이 존재하지 않으면 새로 생성함.
    - 예제 코드:
    ```python
    def write_file(file_path, data):
        with open(file_path, 'w') as file:
            file.write(data)
    ```

- **파일 복사**:
    - 파일을 다른 위치로 복사하는 기능.
    - 예제 코드:
    ```python
    import shutil

    def copy_file(src, dest):
        shutil.copy(src, dest)
    ```

- **파일 이동**:
    - 파일을 지정된 경로로 이동시키는 기능.
    - 예제 코드:
    ```python
    import shutil

    def move_file(src, dest):
        shutil.move(src, dest)
    ```

- **파일 삭제**:
    - 파일을 삭제하는 기능.
    - 예제 코드:
    ```python
    import os

    def delete_file(file_path):
        if os.path.exists(file_path):
            os.remove(file_path)
        else:
            print(f"File {file_path} does not exist")
    ```