# greet-ci

인사말 프로그램의 GitHub Actions CI 구성 실습

## 요구사항

- Python >= 3.11
- uv

## 설치 및 동기화

```bash
uv sync --locked
```

## 실행

```bash
uv run --locked python greet.py Hee
uv run --locked python greet.py
```

## 테스트 및 품질 검사

```bash
uv run --locked pytest -q greet.py
uv run --locked black --check greet.py
uv run --locked flake8 greet.py
uv run --locked mypy greet.py
```

## 패키지 빌드

```bash
uv build
```