# 🚀 GitHub Pages 배포 빠른 시작 가이드

## ✅ 완료된 작업

MkDocs와 GitHub Pages 배포를 위한 모든 설정이 완료되었습니다!

### 생성된 파일

```
lgd_2025_genbi_spotfire_docs/
├── 📄 mkdocs.yml                   # MkDocs 설정 파일
├── 📄 requirements.txt             # Python 의존성
├── 📄 .gitignore                   # Git 무시 파일
├── 📁 .github/
│   └── 📁 workflows/
│       └── 📄 deploy.yml           # GitHub Actions 자동 배포
└── 📁 docs/                        # 문서 소스
    ├── 📄 index.md                 # 홈페이지 (새로 생성)
    ├── 📄 kickoff_report.md        # 착수 보고서
    ├── 📄 code_review_for_developers.md   # 개발 가이드
    ├── 📄 customer_business_questions.md  # 비즈니스 요구사항
    └── 📄 README.md                # README
```

---

## 🎯 다음 단계 (3단계)

### 1단계: GitHub 저장소에 푸시

```bash
# 현재 디렉토리에서 실행
git add .
git commit -m "Add MkDocs documentation with GitHub Pages deployment"
git push origin main
```

### 2단계: GitHub Pages 활성화

1. GitHub 저장소 페이지로 이동
2. **Settings** 탭 클릭
3. 왼쪽 메뉴에서 **Pages** 클릭
4. Source 섹션에서:
   - **Deploy from a branch** 선택
   - Branch: **gh-pages** 선택
   - Folder: **/ (root)** 선택
5. **Save** 클릭

### 3단계: 배포 확인

1. **Actions** 탭에서 워크플로우 실행 확인
2. 완료되면 (약 2-3분 소요):
   - 배포 URL: `https://yourusername.github.io/lgd_2025_genbi_spotfire_docs/`

---

## 🧪 로컬 테스트 (옵션)

배포 전 로컬에서 확인하려면:

```bash
# 의존성 설치
pip install -r requirements.txt

# 로컬 서버 실행
mkdocs serve
```

브라우저에서 `http://127.0.0.1:8000` 접속

---

## 🎨 주요 기능

### ✨ Material 테마
- 아름다운 UI/UX
- 다크/라이트 모드 전환
- 반응형 디자인

### 🔍 검색 기능
- 전체 문서 검색
- 한국어 검색 지원

### 📊 Mermaid 다이어그램
- 플로우차트, 시퀀스 다이어그램 지원
- 자동 렌더링

### 📱 네비게이션
- 탭 기반 메뉴
- 사이드바 목차
- 상단 네비게이션

---

## 📝 문서 수정 방법

### 기존 문서 수정
1. `docs/` 디렉토리의 `.md` 파일 편집
2. `git push` → 자동 배포

### 새 문서 추가
1. `docs/new_page.md` 파일 생성
2. `mkdocs.yml`의 `nav` 섹션에 추가:
   ```yaml
   nav:
     - 홈: index.md
     - 새 페이지: new_page.md
   ```
3. `git push` → 자동 배포

---

## 🔧 설정 커스터마이징

### 사이트 정보 변경
`mkdocs.yml` 파일 수정:

```yaml
site_name: 원하는 사이트 이름
site_description: 원하는 설명
repo_url: https://github.com/yourusername/your-repo
```

### 테마 색상 변경
`mkdocs.yml`의 `theme.palette` 섹션:

```yaml
theme:
  palette:
    primary: blue  # red, pink, purple, deep-purple, indigo, blue, etc.
    accent: amber
```

### 네비게이션 구조 변경
`mkdocs.yml`의 `nav` 섹션:

```yaml
nav:
  - 홈: index.md
  - 가이드:
      - 시작하기: getting-started.md
      - 고급: advanced.md
  - API: api.md
```

---

## 🐛 트러블슈팅

### 문제: GitHub Actions 실패

**원인**: Python 의존성 설치 실패

**해결**:
1. `requirements.txt` 확인
2. `.github/workflows/deploy.yml`의 설치 명령어 확인

### 문제: 페이지가 404 에러

**원인**: GitHub Pages 설정 오류

**해결**:
1. Settings → Pages에서 **gh-pages** 브랜치 선택
2. Actions 탭에서 워크플로우 성공 확인

### 문제: 로컬에서 Mermaid 안 보임

**원인**: 브라우저 캐시

**해결**:
1. 하드 리프레시 (Ctrl+Shift+R 또는 Cmd+Shift+R)
2. `mkdocs serve` 재시작

---

## 📚 추가 리소스

- [MkDocs 공식 문서](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [Mermaid 다이어그램 문법](https://mermaid.js.org/)

---

## ✅ 체크리스트

배포 전 확인사항:

- [ ] `mkdocs.yml`에서 `repo_url` 수정
- [ ] 로컬 테스트 완료 (`mkdocs serve`)
- [ ] Git 커밋 및 푸시
- [ ] GitHub Actions 워크플로우 성공 확인
- [ ] GitHub Pages 설정 (gh-pages 브랜치)
- [ ] 배포된 사이트 접속 확인

---

## 🎉 완료!

모든 설정이 완료되었습니다. 이제 `git push`만 하면 자동으로 배포됩니다!

**축하합니다! 🎊**

