# claudelab — Claude for Executives 실습 가이드

임원 Claude 실습 과정(4~6회차) 따라 하기 가이드 사이트. https://skilleat-labs.github.io/claudelab/

- 회차별 페이지(`docs/day4~6/`)는 직접 고치지 않는다. 원본은 과정 폴더의 `02_실습가이드/build_guides.js`이고, `node build_mkdocs.js`로 다시 만든다 (Word 가이드와 같은 원본).
- 직접 쓰는 페이지: `docs/index.md`, `docs/install.md`, `docs/downloads.md`
- 로컬 확인: `mkdocs serve` → http://127.0.0.1:8000/claudelab/
- 배포: `main`에 push하면 GitHub Actions가 Pages로 배포한다 (`.github/workflows/pages.yml`, `mkdocs build --strict`).
- 예시 회사 (주)한빛정밀과 모든 수치는 교육용 가상 자료다.
