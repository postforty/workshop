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