# Quarto 활용 가이드 (고퀄리티 자동 보고서 생성)

Quarto는 Pandoc을 기반으로 한 차세대 오픈 소스 과학기술 출판 시스템입니다. Markdown 문서 안에 데이터 분석 코드(Python, R 등)와 다이어그램을 삽입하여, 가장 현대적이고 세련된 디자인의 보고서(Word, PDF, HTML)를 자동으로 생성할 수 있습니다.

## 1. 선행 환경 설정 (Windows)

Quarto는 자체적으로 문서 변환을 수행하며, 고퀄리티 통계 차트를 위해 Python 환경을 주로 사용합니다.

### 1.1 Quarto CLI 설치
터미널(CMD/PowerShell)에서 다음 명령어로 설치하거나, [Quarto 홈페이지](https://quarto.org/docs/get-started/)에서 설치 파일을 다운로드합니다.
```bash
# winget을 이용한 설치
winget install quarto.quarto
```

### 1.2 시각화 도구 설치 (Python)
세련된 통계 차트를 그리려면 파이썬과 관련 라이브러리가 필요합니다.
```bash
# 필수 라이브러리 설치
pip install pandas plotly jupyter
```

---

## 2. 기본 사용 방법

Quarto는 `.qmd` 확장자를 기본으로 사용하지만, 일반 `.md` 파일도 처리할 수 있습니다.

### 2.1 문서 작성 (`report.qmd`)
문서 상단에 설정(YAML)을 넣고, 그 아래에 본문과 코드 블록을 작성합니다.

````markdown
---
title: "2025 분기 경영 보고서"
author: "작성자 이름"
format:
  docx:
    reference-doc: custom-reference.docx # (선택) 워드 스타일 템플릿
---

## 1. 실적 요약
이번 분기 실적은 전년 대비 15% 성장하였습니다.

## 2. 분기별 매출 통계
```{python}
import plotly.express as px
import pandas as pd

# 데이터 로드 (Excel/CSV 등 연동 가능)
df = pd.DataFrame({
    "Quarter": ["1Q", "2Q", "3Q", "4Q"],
    "Sales": [1200, 1500, 1800, 2100]
})

# Plotly를 이용한 세련된 막대 그래프
fig = px.bar(df, x="Quarter", y="Sales", 
             text_auto='.2s', title="매출 성장 추이",
             color_discrete_sequence=['#45B3E7']) # 현대적인 색상

fig.show()
```

## 3. 시스템 아키텍처 (D2 활용)
D2 문법도 별도 설치 없이 바로 지원합니다.

```d2
User -> Web Server -> Database: 데이터 조회
```
````

### 2.2 문서 생성(Render)
터미널에서 다음 명령어를 입력하면 `report.docx` 파일이 생성됩니다.
```bash
quarto render report.qmd --to docx
```

---

## 3. 고퀄리티 보고서를 위한 핵심 팁

### 3.1 세련된 차트 디자인 (Plotly)
- **테마 지정**: `fig.update_layout(template="plotly_white")`를 사용하면 배경이 흰색인 깔끔한 비즈니스용 차트가 생성됩니다.
- **색상 팔레트**: 원색 대신 `#5DADE2`, `#48C9B0` 같은 파스텔/현대적인 헥사 코드를 사용하세요.

### 3.2 데이터 자동화
- 코드 블록에서 `pd.read_excel("data.xlsx")`를 사용하면, 엑셀 파일만 업데이트하고 실행해도 보고서 내의 모든 그래프가 자동으로 최신화됩니다.

### 3.3 Word 스타일 지정
- `reference-doc` 옵션을 사용하여 미리 디자인된 워드 문서를 지정하면, 제목 크기나 폰트, 표 스타일 등이 해당 디자인에 맞춰서 생성됩니다.

---

## 4. 요약: 왜 Quarto인가?

| 기능 | Pandoc (기본) | Quarto |
| :--- | :--- | :--- |
| **통계 차트** | 별도 생성 후 이미지 삽입 | 코드에서 직접 생성 (자동 삽입) |
| **디자인** | 필터 설정이 복잡함 | 현대적인 스타일 기본 내장 |
| **데이터 연동** | 수동 작업 필요 | 파이썬 연동으로 완전 자동화 |
| **다이어그램** | 필터 개별 설치 | Mermaid, D2 등 통합 지원 |
