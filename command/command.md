## 리눅스 기본 명령어

### ls (List)

- `ls`: 현재 디렉토리의 모든 파일 및 폴더를 기본 형식으로 보여준다.
- `ls -l`: 파일 및 폴더에 대한 자세한 정보와 함께 리스트업 한다.
- `ls -a`: 숨겨진 파일을 포함하여 모든 파일을 보여준다.

### cd (Change Directory)

- `cd`: 디렉토리를 변경한다.
- `cd Documents`: 현재 디렉토리에서 'Documents'라는 이름의 폴더로 이동한다.
- `cd ..`: 현재 디렉토리의 상위 폴더로 이동한다.

### pwd (Print Working Directory)

- `pwd`: 현재 작업 중인 디렉토리의 경로를 표시한다.

### mkdir (Make Directory)

- `mkdir`: 새로운 디렉토리(폴더)를 생성한다.
- `mkdir new_folder`: 현재 디렉토리에 'new_folder'라는 이름의 새 디렉토리를 만든다.
- `mkdir -p folder1/folder1`: 'folder1'내에 'folder1'를 생성한다. `-p`는 상위 디렉토리가 없는 경우, 그 상위 디렉토리를 생성하는 옵션이다.

### rmdir (Remove Directory)

- `rmdir`: 디렉토리를 삭제한다.
- `rmdir old_folder`: 'old_folder'라는 이름의 디렉토리를 삭제한다.
- `rmdir`은 디렉토리가 비어있을 때만 작동한다. **내부에 파일이나 다른 디렉토리가 있으면 오류가 발생한다.**
- 디렉토리 안의 파일과 함께 삭제하려면 `rm -r` 명령어를 사용해야 한다.

### rm (Remove)

- `rm`: 디렉토리나 파일을 삭제한다.
- `rm file.txt`: 'file.txt'라는 파일을 삭제한다.
- `rm -r folder`: 'folder'라는 디렉토리와 그 안의 모든 내용을 삭제한다.
- 삭제한 파일은 복구가 어렵기 때문에, 중요한 파일을 삭제하기 전에는 항상 확인하는 것이 좋다.

### touch

- `touch`: 새로운 빈 파일을 생성하거나, 기존 파일의 타임스탬프(날짜 및 시간 정보)를 현재 시간으로 갱신한다.
- `touch new_file.txt`: 'new_file.txt'라는 새 파일을 생성한다. 파일이 이미 존재한다면, 타임스탬프가 갱신된다.
- 매우 간단하고 빠르게 파일을 생성할 수 있으며, 스크립트나 로그 파일을 초기화할 때 유용하다.

### cp (Copy)

- `cp`: 파일이나 디렉토리를 복제한다.
- `cp source.txt destination.txt`: 'source.txt'를 'destination.txt'로 복사한다. 'destination.txt'가 이미 존재하면 덮어쓴다.
- `cp -r source_dir destination_dir`: 'source_dir' 디렉토리와 그 내용을 'destination_dir'로 복사한다.

### mv (Move)

- `mv`: 파일이나 디렉토르의 위치를 이동시키거나 이름을 변경한다.
- `mv old_name.txt new_name.txt`: 'old_name.txt의 이름을 'new_name.txt'로 변경한다.
- `mv file.txt /path/to/directory/`: 'file.txt'를 지정된 디렉토리로 이동한다.
- `mv`명령어는 파일을 이동시킬 때 복사 후 삭제하는 것이 아니라 파일의 위치정보만 변경하기 때문에 처리 속도가 빠르다.
- 이동하려는 대상 경로에 같은 이름의 파일이 이미 존재할 경우, 기존 파일은 덮어쓰여진다.

### cat (Concatenate)

- `cat`: 텍스트 파일의 내용을 화면에 출력하거나, 여러 파일의 내용을 연결하여 출력한다.
- `cat file.txt`: 'file.txt' 파일의 내용을 화면에 표시한다.
- `cat file1.txt file2.txt > combined.txt`: 'file1.txt'와 file2.txt'의 내용을 합쳐 'combined.txt'에 저장한다.

### chmod (Change Mode)

- `chmod`: 파일이나 디렉토리의 권한을 변경한다.
- `chmod 755 file.sh`: 'file.sh' 파일에 대해 소유자는 읽기, 쓰기, 실행 권한을 부여하고, 그룹과 기타 사용자에게는 읽기와 실행 권한만 부여한다.
- `chmod u+x file.sh`: 'file.sh' 파일에 대해 현재 사용자에게 실행 권한을 추가한다.
- 권한 변경은 보안에 영향을 줄 수 있으므로 신중히 사용해야 한다.

### grep (Global Reqular Experssion Print)

- 파일 내용 중에서 지정된 패턴이나 문자열을 검색하여 그 결과를 출력한다.
- `grep "text" file.txt`: 'file.txt'에서 "text"라는 문자열이 포함된 모든 줄을 표시한다.
- `grep -r "text" .`: 현재 디렉토리와 하위 디렉토리에서 "text" 문자열을 재귀적으로 검색한다.
- 정규 표현식을 사용하여 복잡한 검색 패턴을 지정할 수 있으며, 로그 파일 분석이나 특정 데이터 추출에 유용하다.

### echo

- 주어진 문자열을 터미널에 출력한다. 환경 변수의 값을 표시하거나, 파일에 텍스트를 쓰는 데에도 사용된다.
- `echo "Hello World"`: 터미널에 "Hello World"라는 문구를 출력한다.
- `echo $HOME`: 'HOME' 환경 변수의 값을 출력한다.
- `echo "some text" > file.txt`: "Some text"라는 문구를 'file.txt' 파일에 저장한다.
- 스크립트 작성 시 변수 값을 확인하거나, 파일에 내용을 빠르게 추가할 때 유용하다.

### man (Manual)

- 리눅스 명령어의 사용법, 옵션, 기능 등을 설명하는 매뉴얼 페이지를 제공한다.
- `man ls`: 'ls' 명령어에 대한 매뉴얼 패이지를 보여준다.

### sudo (SuperUser DO)

- 일반 사용자가 관리자(superuser) 권한을 가지고 명령어를 실행할 수 있게 한다. 시스템 설정 변경, 중요한 파일 수정, 관리자 권한을 필요로 하는 소프트웨어 설치 시 사용된다.
- `sudo apt-get update`: 패키지 리스트를 업데이트 한다.

### find

- 파일이나 디렉토리를 검색한다.
- `find . -name "file.txt"`: 현재 디렉토리에서 'file.txt' 파일을 찾는다.
- `find / -type d -name "config"`: 루트 디렉토리에서 'config'라는 이름의 디렉토리를 찾는다.
