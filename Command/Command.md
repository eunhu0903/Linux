## 리눅스 기본 명령어

### ls (List)

- `ls`: 현재 디렉토리의 모든 파일 및 폴더를 기본 형식으로 보여준다.
- `ls -l`: 파일 및 폴더에 대한 자세한 정보와 함께 리스트업 해준다.
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

### rmdir (Remove Directory)

- `rmdir`: 디렉토리를 삭제한다.
- `rmdir old_folder`: 'old_folder'라는 이름의 디렉토리를 삭제한다.
- `rmdir`은 디렉토리가 비어있을 때만 작동하며, **내부에 파일이나 다른 디렉토리가 있으면 오류가 발생한다.**
- 디렉토리 안의 파일과 함께 삭제하려면 `rm -r` 명령어를 사용해야 한다.

### rm (Remove)

- `rm`: 파일이나 디렉토리를 삭제한다.
- `rm file.txt`: 'file.txt'라는 파일을 삭제한다.
- `rm -r folder`: 'folder'라는 디렉토리와 그 안의 모든 내용을 삭제한다.

### touch

- `touch`: 새로운 빈 파일을 생성하거나, 기존 파일의 타임스탬프를 현재 시간으로 갱신한다.
- `touch new_file.txt`: 'new_file.txt'라는 새 파일을 생성한다. 이미 존재한다면, 타임스탬프가 갱신된다.

### cp (Copy)

- `cp`: 파일이나 디렉토리를 복사한다.
- `cp a.txt b.txt`: 'a.txt'를 'b.txt'로 복사한다.
- `cp -r a.txt b.txt`: 'a.txt' 디렉토리와 그 내용을 'b.txt'로 복사한다.

### mv (Move)

- `mv`는 파일이나 디렉토리의 위치를 이동시키거나 이름을 변경한다.
- `mv a.txt b.txt`: 'a.txt'의 이름을 'b.txt'로 변경한다.
- `mv a.txt /Desktop/directory/`: 'a.txt'를 지정된 디렉토리로 이동한다.

### cat (Concatenate)

- `cat`: 텍스트 파일의 내용을 화면에 출력하거나, 여러 파일의 내용을 연결하여 출력한다.
- `cat a.txt`: 'a.txt' 파일의 내용을 화면에 표시한다.

  