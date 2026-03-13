# Git 기본 명령어

## 개요

자주 쓰는 Git 명령어를 정리합니다.

## 저장소 초기화 및 복제

```bash
# 새 저장소 초기화
git init

# 원격 저장소 복제
git clone <URL>
```

## 변경 사항 스테이징 및 커밋

```bash
# 변경된 파일 확인
git status

# 특정 파일 스테이징
git add <파일명>

# 전체 변경 사항 스테이징
git add .

# 커밋
git commit -m "커밋 메시지"
```

## 브랜치

```bash
# 브랜치 목록 확인
git branch

# 새 브랜치 생성 후 이동
git checkout -b <브랜치명>

# 브랜치 병합
git merge <브랜치명>
```

## 원격 저장소

```bash
# 원격 저장소에 푸시
git push origin <브랜치명>

# 원격 저장소에서 가져오기
git pull origin <브랜치명>
```

## 참고
- [공식 Git 문서](https://git-scm.com/doc)
