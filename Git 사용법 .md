# Git 사용법

### **1. Git 초기화**

- **git init**: 현재 디렉토리를 Git 저장소로 초기화. `.git` 폴더 생성.
    
    ```bash
    bash
    코드 복사
    $ git init
    
    ```
    
- **초기 설정**:
    
    ```bash
    bash
    코드 복사
    $ git config --global user.name "깃닉네임"
    $ git config --global user.email "깃이메일"
    
    ```
    

---

### **2. Git 스테이징**

- **파일 스테이징**:
    
    ```bash
    bash
    코드 복사
    $ git add 파일명
    $ git add --all    # 모든 변경사항 추가
    $ git add .        # 현재 디렉토리의 모든 변경사항 추가
    $ git add *        # 현재 디렉토리와 하위 디렉토리 파일 추가
    
    ```
    
- **스테이징 확인**:
    
    ```bash
    bash
    코드 복사
    $ git status         # 상태 확인
    $ git status -s      # 요약된 상태 확인
    
    ```
    
- **스테이징 취소**:
    
    ```bash
    bash
    코드 복사
    $ git rm --cached 파일명
    
    ```
    

---

### **3. GitIgnore**

- **`.gitignore` 생성**: Git이 추적하지 않을 파일이나 폴더를 지정.
    
    ```
    plaintext
    코드 복사
    # 예시: .gitignore 내용
    /node_modules
    .env
    *.log
    
    ```
    

---

### **4. Git 커밋**

- **커밋하기**:
    
    ```bash
    bash
    코드 복사
    $ git commit         # 메시지 작성 에디터 열림
    $ git commit -m "메시지"  # 메시지를 바로 입력하여 커밋
    
    ```
    
- **add와 commit 동시에**:
    
    ```bash
    bash
    코드 복사
    $ git commit -am "메시지"  # 수정된 파일 add 후 커밋 (새 파일 제외)
    
    ```
    

---

### **5. Git 로그 확인**

- **커밋 내역 보기**:
    
    ```bash
    bash
    코드 복사
    $ git log                          # 자세한 커밋 내역
    $ git log --oneline                # 요약된 내역
    $ git log --pretty=oneline         # 간단한 형식
    $ git log --graph                  # 커밋 그래프
    $ git log --oneline -n7            # 최근 7개 커밋
    
    ```
    

---

### **6. Git Diff (변경사항 비교)**

- **변경사항 확인**:
    
    ```bash
    bash
    코드 복사
    $ git diff               # 커밋된 파일과 수정 파일 비교
    $ git diff --staged      # 커밋된 파일과 스테이징된 파일 비교
    
    ```
    
- **커밋 간 비교**:
    
    ```bash
    bash
    코드 복사
    $ git diff <커밋해시1> <커밋해시2>
    $ git diff HEAD HEAD^    # 가장 최근 커밋과 이전 커밋 비교
    
    ```
    
- **브랜치 간 비교**:
    
    ```bash
    bash
    코드 복사
    $ git diff 브랜치1 브랜치2
    
    ```
    

---

### **추가 Tip**

1. **.git 폴더는 절대 삭제하지 말 것!**
2. **새 파일은 `git add` 후 커밋 가능.**
3. **.gitignore은 초기 설정 후 적용 필요.**