# Pandoc D2 변환 가이드 (고퀄리티 차트)

D2(Declarative Diagramming)는 텍스트를 기반으로 세련되고 현대적인 다이어그램을 생성하는 도구입니다. Mermaid보다 전문적인 디자인과 강력한 기능을 제공하며, 오픈 소스로서 누구나 무료로 사용할 수 있습니다.

## 1. D2의 특징 및 장점

- **현대적인 디자인**: 기본 테마가 매우 세련되어 보고서용으로 적합합니다.
- **아이콘 지원**: AWS, Google Cloud, Docker 등 수천 개의 IT 아이콘을 내장하고 있습니다.
- **스케치 모드**: 딱딱한 차트가 아닌, 손으로 그린 듯한 감성적인 스타일을 지원합니다.
- **가볍고 빠름**: Go 언어로 작성된 단독 실행 파일로, 별도의 런타임(Python, Node.js 등)이 필요 없습니다.

## 2. 설치 및 환경 설정 (Windows)

### 2.1 D2 엔진 설치
Windows 터미널(CMD/PowerShell)에서 다음 명령어로 간편하게 설치할 수 있습니다.
```bash
winget install terastruct.d2
```
*설치 후 새 터미널 창을 열어 `d2 --version`을 입력하여 설치를 확인하세요.*

### 2.2 Pandoc Lua 필터 준비
Pandoc에서 D2 문법을 인식하려면 **Lua 필터**가 필요합니다.
1. [pandoc-ext/diagram](https://github.com/pandoc-ext/diagram/blob/main/diagram.lua) 페이지에서 `diagram.lua` 파일을 다운로드합니다.
2. 변환할 Markdown 파일이 있는 폴더에 `diagram.lua` 파일을 넣습니다.

---

## 3. 사용 방법

### 3.1 Markdown 작성 예시
Markdown 파일(`input.md`) 내에 다음과 같이 `d2` 코드 블록을 작성합니다.

```d2
x -> y: Hello D2 {
  style: {
    stroke: "#5d6d7e"
    fill: "#ebedef"
  }
}
```

### 3.2 변환 명령어 (Word/PDF/HTML)
변환 시 `--lua-filter` 옵션을 사용하여 방금 준비한 필터 파일을 지정합니다.

```bash
# Word로 변환 (고퀄리티 차트 포함)
pandoc input.md --lua-filter=diagram.lua -s -o output.docx

# PDF로 변환
pandoc input.md --lua-filter=diagram.lua -s -o output.pdf --pdf-engine=xelatex
```

---

## 4. 디자인 업그레이드 팁

### 4.1 테마(Theme) 적용
D2는 200번 테마(세련된 푸른색 계열)를 포함하여 다양한 테마를 지원합니다.
- 명령어 뒤에 환경 변수를 붙여 테마를 변경할 수 있습니다.
- 예: `SET D2_THEME=200 && pandoc ...`

### 4.2 스케치 모드 (Sketch Mode)
회의 시 화이트보드에 그린 느낌을 주려면 다음 설정을 코드 블록 상단에 추가합니다.
```d2
direction: right
vars: {
  d2-config: {
    layout-engine: elk
    theme: 200
    sketch: true
  }
}
x -> y: 손글씨 스타일 차트
```

### 3.3 아이콘 활용
노드 이름 뒤에 아이콘 이름을 지정하여 손쉽게 클라우드 아키텍처를 그릴 수 있습니다.
```d2
Cloud: {
  icon: aws
}
Database: {
  icon: postgresql
}
Cloud -> Database: 연결
```
