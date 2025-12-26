# Pandoc 사용 매뉴얼 (Windows 환경)

Pandoc은 다양한 문서 형식을 변환해주는 강력한 커맨드라인 도구입니다. 이 매뉴얼은 Windows 환경에서 Pandoc을 설치하고 사용하는 기본적인 방법을 다룹니다.

## 1. 설치 (Installation)

[Pandoc 공식 다운로드 페이지](https://github.com/jgm/pandoc/releases)에서 `.msi` 설치 파일을 다운로드하여 실행합니다.

설치가 완료되면 터미널을 새로 열고 다음 명령어로 설치를 확인합니다.
```bash
pandoc --version
```

## 2. 기본 사용법 (Basic Usage)

기본적인 명령어 구조는 다음과 같습니다.
```bash
pandoc [입력파일] -o [출력파일]
```

- `-o`: Output(출력) 파일을 지정하는 옵션입니다.

## 3. 자주 사용하는 변환 예시

### Markdown을 Word(.docx)로 변환
가장 많이 사용하는 기능 중 하나입니다.
```bash
pandoc input.md -o output.docx
```

### Markdown을 HTML로 변환
```bash
pandoc input.md -o output.html
```

### Markdown을 PDF로 변환
PDF 변환은 추가적인 설정이 필요할 수 있습니다. 가장 간단한 방법은 다음과 같습니다.
```bash
pandoc input.md -o output.pdf
```
*참고: PDF 변환을 위해서는 LaTeX 엔진(MiKTeX 등)이나 wkhtmltopdf 같은 도구가 추가로 필요할 수 있습니다.*

## 4. 한글 폰트 문제 해결 (PDF 변환 시)

Windows에서 PDF 변환 시 한글이 깨지는 경우가 많습니다. 이를 해결하기 위해 `xelatex` 엔진을 사용하고 한글 폰트를 지정해주어야 합니다.

```bash
pandoc input.md -o output.pdf --pdf-engine=xelatex -V mainfont="Malgun Gothic"
```

- `--pdf-engine=xelatex`: PDF 변환 엔진으로 xelatex를 사용합니다.
- `-V mainfont="Malgun Gothic"`: 메인 폰트를 윈도우 기본 폰트인 '맑은 고딕'으로 지정합니다.

## 5. 팁 (Tips)

- 파일 경로에 공백이 있다면 따옴표(`"`)로 감싸주어야 합니다. 예: `"My Document.md"`
- 변환 시 스타일을 지정하고 싶다면 `--reference-doc` 옵션을 사용하여 기준이 되는 docx 파일을 지정할 수 있습니다.
