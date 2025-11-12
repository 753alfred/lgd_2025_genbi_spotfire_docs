# lgd_2025_genbi_spotfire_docs

LG Display GenBI Spotfire Copilot 프로젝트 문서

## 📚 프로젝트 개요

Spotfire Copilot 외부 API 연동 및 Intent 확장 프로젝트의 모든 기술 문서를 제공합니다.

- **프로젝트명**: Spotfire Copilot 외부 API 연동
- **시작일**: 2025년 11월 12일
- **목적**: Hi-D Search(Data) API 연동

## 🌐 문서 사이트

이 문서는 **MkDocs Material**로 관리되며, GitHub Pages에 자동 배포됩니다.

**배포된 사이트**: `https://yourusername.github.io/lgd_2025_genbi_spotfire_docs/`

## 🚀 로컬에서 문서 보기

### 1. 의존성 설치

```bash
pip install -r requirements.txt
```

또는 개별 설치:

```bash
pip install mkdocs-material
pip install mkdocs-git-revision-date-localized-plugin
```

### 2. 로컬 서버 실행

```bash
mkdocs serve
```

브라우저에서 `http://127.0.0.1:8000` 접속

### 3. 문서 빌드

```bash
mkdocs build
```

빌드된 사이트는 `site/` 디렉토리에 생성됩니다.

## 📖 문서 구조

```
lgd_2025_genbi_spotfire_docs/
├── docs/                           # 문서 소스 파일
│   ├── index.md                    # 홈페이지
│   ├── kickoff_report.md           # 착수 보고서
│   ├── code_review_for_developers.md   # 개발 가이드
│   ├── customer_business_questions.md  # 비즈니스 요구사항
│   └── README.md                   # README
├── mkdocs.yml                      # MkDocs 설정 파일
├── requirements.txt                # Python 의존성
├── .github/
│   └── workflows/
│       └── deploy.yml              # GitHub Pages 자동 배포
└── README.md                       # 이 파일
```

## 🔧 GitHub Pages 설정

### 1. GitHub 저장소 설정

1. GitHub에서 새 저장소 생성
2. 저장소 Settings → Pages로 이동
3. Source를 **"Deploy from a branch"** 선택
4. Branch를 **"gh-pages"** 선택

### 2. 코드 푸시

```bash
git add .
git commit -m "Add MkDocs documentation"
git push origin main
```

### 3. 자동 배포

`main` 브랜치에 푸시하면 GitHub Actions가 자동으로:
1. MkDocs 빌드
2. `gh-pages` 브랜치에 배포
3. GitHub Pages에 자동 반영

## 📝 문서 작성 가이드

### 새 문서 추가

1. `docs/` 디렉토리에 `.md` 파일 생성
2. `mkdocs.yml`의 `nav` 섹션에 추가:

```yaml
nav:
  - 홈: index.md
  - 새 문서: new_document.md
```

### Mermaid 다이어그램 사용

````markdown
```mermaid
graph TD
    A[시작] --> B[끝]
```
````

### 경고 박스 사용

```markdown
!!! info "제목"
    내용

!!! warning "경고"
    주의할 내용

!!! tip "팁"
    유용한 정보
```

## 🛠️ 유용한 명령어

```bash
# 로컬 서버 실행
mkdocs serve

# 빌드만 실행
mkdocs build

# GitHub Pages에 수동 배포 (권장하지 않음, GitHub Actions 사용)
mkdocs gh-deploy

# 설정 파일 검증
mkdocs build --strict
```

## 📂 주요 문서

- **[착수 보고서](docs/kickoff_report.md)**: 프로젝트 배경, 목표, 추진 전략
- **[개발자 가이드](docs/code_review_for_developers.md)**: Intent 추가 및 API 연동 방법
- **[비즈니스 요구사항](docs/customer_business_questions.md)**: API 연동 전 확인사항

## 🤝 기여 방법

1. 문서 수정: `docs/` 디렉토리의 마크다운 파일 편집
2. 로컬 테스트: `mkdocs serve`로 확인
3. 커밋 및 푸시: `git push origin main`
4. 자동 배포 확인

## 📞 문의

프로젝트 관련 문의사항은 프로젝트 담당자에게 연락해주세요.

---

*최종 업데이트: 2025년 11월 12일*
