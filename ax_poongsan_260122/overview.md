# 🤖 AI활용 업무 자동화 교육

## 📋 교육 개요

- 🏢 **대상 기업**: 풍산
- 📅 **일정**: 2026년 01월 26일, 27일 (월, 화)
- ⏰ **시간**: 09:00 ~ 18:00
- 🎯 **학습 목표**: 
  1. 프롬프트 엔지니어링: 데이터 보안 및 비식별화 원칙을 준수하며, 논리적 구조를 갖춘 프롬프트를 설계하여 AI로부터 최적의 업무 결과를 도출한다.
  2. 텍스트·언어 생성: 마크다운 기반으로 지식을 체계화하고, 사용자의 문서를 참조하는 AI를 활용하여 목적에 맞는 2차 콘텐츠를 생성한다.
  3. 이미지 생성: 생성형 AI를 활용하여 텍스트를 시각화하고, 업무 보고 및 마케팅 등에 즉시 활용 가능한 비주얼 에셋을 직접 제작한다.
  4. 문서 자동화(기초): 코딩 없이 다이어그램을 생성하고 보고서 서식을 자동화하며, 이종 파일 간 포맷 변환을 통해 문서 작업 시간을 획기적으로 단축한다.
  5. 문서 자동화(심화): 표준 템플릿으로 업무 양식을 통일하고, 작성한 메모에 꼬리표(속성)를 붙여 필요한 정보만 자동으로 뽑아내어 팀 공용 폴더와 연동된 실시간 업무 현황판을 구축한다.
- 🧰 **활용툴**: Gemini, ChatGPT, n8n, Obsidian, NotebookLM, Google AI Studio 등 교육 커리큘럼에 명시된 주요 AI 솔루션 및 자동화 도구

## 📚 참고 자료

- 🔗 [Learn Prompting](https://learnprompting.org/docs/introduction)
- 🔗 [프롬프트 엔지니어링: 개요 및 가이드](https://cloud.google.com/discover/what-is-prompt-engineering)
- 🔗 [마크다운 가이드](https://www.markdownguide.org)
- 🔗 [AI TOP 100](https://challenge.aitop100.org/)

## 🛠️ 사용 기술

| 기술명           | 하위 기술   | 용도                     | 비고                 | URL                                                                |
| ---------------- | ----------- | ------------------------ | -------------------- | ------------------------------------------------------------------ |
| ChatGPT          |             | 대화형 AI 챗봇           |                      | <https://chatgpt.com/>                                             |
| Gemini           |             | 멀티모달 AI 챗봇         |                      | <https://gemini.google.com>                                        |
|                  | Gem         | 맞춤형 AI 챗봇           | Gemini 하위 도구     |                                                                    |
| Presidio         |             | 개인정보(PII) 비식별화   | Microsoft 오픈소스   | <https://microsoft.github.io/presidio>                             |
| NotebookLM       |             | 문서 기반 AI 노트        |                      | <https://notebooklm.google.com>                                    |
| Markdown         |             | 텍스트 서식 언어         | Markdown 공식 가이드 | <https://www.markdownguide.org>                                    |
| Live Preview     |             | Markdown 실시간 미리보기 |                      | <https://markdownlivepreview.com>                                  |
| markmap          |             | 마인드맵 시각화          |                      | <https://markmap.js.org>                                           |
| Obsidian          |             | Markdown 형식의 텍스트 파일을 기반으로 작동하는 개인 지식 관리 및 노트 필기 |                      | <https://obsidian.md>                                           |
| Mermaid          |             | 텍스트 기반 다이어그램 및 차트 생성 |                      | <https://www.mermaidchart.com/play>                                           |
| Pandoc           |             | 문서 포맷 변환           |                      | <https://pandoc.org>                                               |
| Google AI Studio |             | 생성형 AI 프로토타이핑   |                      | <https://aistudio.google.com>                                      |
|                  | Nano Banana | 이미지 생성 모델         | AI Studio 하위 도구  |                                                                    |
| 몰입형 번역      |             | 웹페이지 실시간 번역     | 크롬 브라우저 확장 | <https://immersivetranslate.com/ko>                                |
| Web to PDF      |             | 웹페이지 PDF 변환     | 크롬 브라우저 확장 | <https://webtopdf.space/>                                |


## 📝 교육 커리큘럼 (16교시)

| 일차 | 주제 | 차수 | 시간 | 세부 주제 | 세부 내용 | 사용기술 |
| :--- | :--- | :---: | :---: | :--- | :--- | :--- |
| **1일차** | **프롬프트<br>엔지니어링** | 1교시 | 50분 | AI 업무자동화 개요 | - AI 업무자동화 개념 및 필요성<br>- ChatGPT, Gemini 환경 구축 | ChatGPT, Gemini |
| | | 2교시 | 50분 | 프롬프트 기초 | - 효과적인 지시를 위한 프롬프트 구조(Persona, Context 등) | Gemini |
| | | 3교시 | 50분 | 프롬프트 심화 | - 업무용 템플릿 제작 및 프롬프트 최적화 기법 | Gemini |
| | | 4교시 | 50분 | AI 데이터 보안 | - 개인정보(PII) 비식별화 및 보안의 중요성<br/> - 기밀 정보 유출 없는 Gemini + Excel 활용법 | Presidio, Gemini |
| | **텍스트·언어<br>생성** | 5교시 | 50분 | 문서 구조화 기초 | - Markdown 이해 및 구조화된 문서 작성 기법 | Markdown, Live Preview, markmap |
| | | 6교시 | 50분 | 지식 관리 자동화 | - Markdown 기반 로컬 지식 관리 시스템 구축<br />- LLM API를 활용한 문서 기반 답변 생성 | Obsidian, Google AI Studio |
| | | 7교시 | 50분 | 맞춤형 AI Gem 제작 | - 특정 업무 전용 AI 챗봇 제작 | Gem |
| | | 8교시 | 50분 | 콘텐츠 기반 답변 및 생성 | - 내가 가진 정보(1차 콘텐츠)로 채팅하기<br/>- 내 목적에 맞는 결과물(2차 콘텐츠) 생성하기 | NotebookLM |
| **2일차** | **이미지 생성** | 9교시 | 50분 | 비주얼 콘텐츠 생성 | - AI 이미지 생성 및 업무 활용 | Nano Banana |
| | **문서 자동화(기초)** | 10교시 | 50분 | 보고서 생성 | - Word, HWP 보고서 생성하기 | Gemini |
| | | 11교시 | 50분 | 다이어그램 시각화<br />문서 포맷 변환 자동화 | - (직접 코딩하지 않는) 코딩 기반 플로우차트 및 마인드맵 자동 생성<br />- 파일 간 포맷 변환 및 웹 PDF 일괄 저장 | Mermaid, Pandoc, Web to PDF |
| | **문서 자동화(심화)** | 12교시 | 50분 | AI 친화적 데이터 규격화 | - AI가 즉시 이해할 수 있는 구조적 텍스트 작성법과 정보 연결 기술 습득(Markdown 및 Linking 학습)<br/>"지금 작성하는 방식이 미래 사내 AI 비서의 성능을 결정합니다." | Obsidian, Markdown |
| | | 13교시 | 50분 | 지식의 정형화와 시각화 | - 비정형 노트를 '데이터베이스'로 변환하고 복잡한 업무 로직을 시각화<br/>"노트에 속성을 부여하는 순간, 단순한 메모는 검색 가능한 데이터베이스가 됩니다." | Obsidian: Properties, Canvas |
| | | 14교시 | 50분 | 업무 자동화 | - 표준 템플릿으로 양식을 통일하고, 공유 환경에서 실시간 업무 현황판 구축.<br/>"취합과 보고 업무를 옵시디언에 맡기고, 여러분은 의사결정에만 집중하십시오." | Obsidian: Templates, Dataview |
| | **실습** | 15교시 | 50분 | 실무 종합 실습 | - 업무 시나리오 기반 자동화 솔루션 기획 및 구현 | 종합 기술 활용 |
| | | 16교시 | 50분 | 결과 공유 및 피드백 | - 프로젝트 발표, Q&A 및 교육 총평 | |
