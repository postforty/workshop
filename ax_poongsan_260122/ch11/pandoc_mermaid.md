# Pandoc Mermaid 변환 가이드 (Windows)

Pandoc을 사용하여 Markdown 문서를 변환할 때, 내부에 포함된 Mermaid 차트를 실제 이미지로 렌더링하여 포함시키는 방법을 설명합니다.

## 1. 선행 환경 설정 (Prerequisites)

Mermaid 차트를 렌더링하기 위해서는 **Node.js**와 **필터(Filter)** 프로그램 설치가 필수적입니다.

### 1.1 Node.js 설치
`npm` 명령어를 사용하기 위해 먼저 Node.js가 필요합니다.
- [Node.js 공식 홈페이지](https://nodejs.org/)에서 **LTS 버전**을 다운로드하여 설치합니다.
- 설치 후 터미널(CMD/PowerShell)에서 `node -v`와 `npm -v`를 입력하여 설치를 확인합니다.

### 1.2 mermaid-filter 설치
터미널을 **관리자 권한**으로 열고 다음 명령어를 입력합니다.
```bash
npm install -g mermaid-filter
```
*참고: 권한 오류가 발생할 경우 터미널을 마우스 우클릭 - '관리자 권한으로 실행' 후 다시 시도하세요.*

---

## 2. 사용 방법 (Usage)

Pandoc 명령어의 옵션에 `-F mermaid-filter` (또는 `--filter mermaid-filter`)를 추가하면 됩니다.

### 2.1 예제 명령어

#### Word(.docx)로 변환
```bash
pandoc input.md -F mermaid-filter -s -o output.docx
```

#### HTML로 변환
```bash
pandoc input.md -F mermaid-filter -s -o output.html
```

#### PDF로 변환 (한글 폰트 설정 포함)
```bash
pandoc input.md -F mermaid-filter -s -o output.pdf --pdf-engine=xelatex -V mainfont="Malgun Gothic"
```

---

## 3. 주요 팁 (Tips)

### 3.1 첫 실행 시 소요 시간
명령어를 처음 실행할 때, 내부적으로 차트를 웹으로 렌더링하기 위한 엔진(Puppeteer/Chromium)을 자동으로 내려받습니다. 이 과정에서 **수 분 정도 시간이 걸릴 수 있으므로** 터미널이 멈춘 것처럼 보이더라도 잠시 기다려주세요.

### 3.2 작동 원리
1. Pandoc이 Markdown 파일을 읽습니다.
2. `mermaid` 코드 블록을 발견하면 `mermaid-filter`로 보냅니다.
3. 필터가 해당 코드를 내부적으로 이미지 파일(PNG/SVG 등)로 변환합니다.
4. 변환된 이미지를 최종 문서(Word/HTML/PDF)에 삽입합니다.

### 3.3 경로 문제
이미지 파일이 생성될 때 임시 폴더 권한 문제로 실패하는 경우가 있다면, 작업 중인 폴더로 이동(`cd`)한 뒤 명령어를 실행하는 것이 가장 안전합니다.
