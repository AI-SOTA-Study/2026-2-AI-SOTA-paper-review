# 2026-2 AI SOTA Paper Review

AI SOTA 논문 리뷰 스터디 저장소입니다.

## 스터디 개요

- 인원: 3명
- 발제: 매주 월요일 11:00
- 진행 방식: 발제자의 발표 후 Q&A 및 논문 정리 공유
- 시험 기간: 시험 2주 전부터 스터디를 진행하지 않습니다. 해당 기간의 일정은 시험 종료 후 다시 조정합니다.

## 진행 일정

| 요일 | 시간 | 내용 | 대상 |
| --- | --- | --- | --- |
| 월요일 | 11:00~11:30 | 논문 발제 | 전체 |
| 월요일 | 11:30~12:00 | Q&A | 전체 |
| 화요일 | ~23:59 | 다음 논문 주제 정하기 | 발제자 |
| 일요일 | ~23:59 | 발표 자료를 `weekN` 폴더에 push | 발제자 |
| 일요일 | ~23:59 | 논문 정리 파일 제출 (`.md`, `.ipynb` 등) | 발제자 및 참여자 |

## 발제 순서

| 순서 | 발제자 |
| --- | --- |
| 1 | 정재훈 |
| 2 | 허예린 |
| 3 | 이도현 |

2번째와 3번째 발제자는 추후 정한 뒤 이 표를 업데이트합니다. 3명이 한 번씩 발제한 뒤 같은 순서를 반복합니다.

## 폴더 및 파일 규칙

발제자는 발표 자료를 해당 주차 폴더에 업로드합니다.

```text
week N_<paper-id>/
├── 발표자료 파일 (예: 발표자료.pdf, 발표자료.pptx)
├── 정리 파일 (예: 이름.md 또는 이름.ipynb)
└── 기타 논문 리뷰 자료
```

- 폴더 이름은 `weekN_<논문 식별자>` 형식을 권장합니다.
- 발표 자료는 발제자가 일요일 23:59까지 업로드합니다.
- 모든 참여자는 본인이 작성한 논문 정리 파일을 일요일 23:59까지 업로드합니다.
- 정리 파일의 확장자는 자유입니다. 예: `.md`, `.ipynb`, `.pdf`
- 논문 원문은 저작권 문제가 있을 수 있으므로 저장소에 직접 업로드하지 않고 링크로 공유합니다.

## Fork 및 Pull Request 제출 방법

각 참여자는 자신의 fork에서 작업한 뒤 원본 저장소로 Pull Request(PR)를 보냅니다.

### 1. 저장소 Fork

1. GitHub에서 원본 저장소에 접속합니다.
2. 오른쪽 위의 **Fork**를 클릭합니다.
3. 본인 계정을 Owner로 선택하고 fork를 생성합니다.

### 2. Fork 저장소 Clone

fork한 저장소의 **Code** 버튼에서 HTTPS 주소를 복사한 뒤 터미널에서 실행합니다.

```bash
git clone https://github.com/<내-아이디>/2026-2-AI-SOTA-paper-review.git
cd 2026-2-AI-SOTA-paper-review
```

### 3. 원본 저장소 등록

원본 저장소를 `upstream`으로 등록하면 최신 내용을 받아올 수 있습니다.

```bash
git remote add upstream https://github.com/AI-SOTA-Study/2026-2-AI-SOTA-paper-review.git
git remote -v
```

### 4. 작업 브랜치 생성 및 최신 내용 반영

`main` 브랜치에서 직접 작업하지 않고, 주차와 이름을 포함한 작업 브랜치를 만듭니다.

```bash
git fetch upstream
git switch main
git pull upstream main
git switch -c weekN-<이름>
```

예시:

```bash
git switch -c week1-jeongjaehoon
```

### 5. 파일 작성 및 commit

해당 주차 폴더에 발표 자료 또는 논문 정리 파일을 추가한 뒤 변경 사항을 확인하고 commit합니다.

```bash
git status
git add "week N_<paper-id>/"
git commit -m "Add week N paper review"
```

### 6. fork에 push

```bash
git push -u origin weekN-<이름>
```

### 7. Pull Request 생성

1. GitHub의 본인 fork 페이지로 이동합니다.
2. 방금 push한 브랜치 옆의 **Compare & pull request**를 클릭합니다.
3. PR의 base repository가 `AI-SOTA-Study/2026-2-AI-SOTA-paper-review`인지 확인합니다.
4. base branch는 `main`, compare branch는 본인의 작업 브랜치인지 확인합니다.
5. 제목과 본문을 작성한 뒤 **Create pull request**를 클릭합니다.

PR 본문에는 다음 내용을 포함합니다.

```markdown
## 논문
- 논문 제목:
- 논문 링크:

## 변경 내용
- 발표 자료 추가 또는 수정
- 논문 정리 파일 추가

## 확인 사항
- [ ] 해당 주차 폴더에 파일을 추가했습니다.
- [ ] 일요일 23:59 전 제출했습니다.
- [ ] 원본 저장소를 base repository로 설정했습니다.
```

### 8. 리뷰 반영 및 완료

리뷰 의견이 있으면 같은 작업 브랜치에서 파일을 수정하고 다시 push합니다. 기존 PR에 자동으로 반영됩니다. 리뷰가 끝나면 원본 저장소에 merge합니다.

```bash
git add .
git commit -m "Apply review feedback"
git push
```

## 제출 전 확인

- [ ] 이번 주 논문 주제를 수요일 23:59까지 정했습니다.
- [ ] 발제자는 발표 자료를 일요일 23:59까지 `weekN` 폴더에 push했습니다.
- [ ] 발제자와 참여자 모두 논문 정리 파일을 일요일 23:59까지 제출했습니다.
- [ ] fork에서 작업하고 원본 저장소로 PR을 생성했습니다.
