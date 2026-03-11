# 📚 웹 프로그래밍 요약: HTML/CSS 및 React 기초

## 1. HTML & CSS 및 웹 기초

### 마크업 언어 vs 메타데이터
* [cite_start]**마크업 언어**: 문서나 데이터를 구조화하고 서식을 지정하는 언어입니다 (예: HTML, XML, Markdown)[cite: 7, 11]. [cite_start]주로 콘텐츠의 표현에 초점을 맞춥니다[cite: 12].
* [cite_start]**메타데이터**: 데이터 자체가 아닌, 데이터를 설명하는 정보입니다 (예: HTML의 `<meta>` 태그, JSON-LD)[cite: 7, 11]. [cite_start]마크업 언어는 문서 내에 메타데이터를 포함할 수 있습니다[cite: 14].

### HTML 표준 기관
* [cite_start]**W3C**: 웹 표준 제정 기관으로 HTML의 공식 명세를 제공합니다[cite: 18, 20].
* [cite_start]**MDN Web Docs**: 태그 목록과 사용법을 상세히 설명하며, 최신 표준을 쉽게 이해할 수 있습니다[cite: 21, 23, 24].
* [cite_start]**WHATWG**: 최신 HTML Living Standard(HTML LS)를 유지보수하는 단체입니다[cite: 25, 27].

### MPA vs SPA

* [cite_start]**MPA (Multi-Page App)**: 매 요청마다 서버에서 새로운 HTML을 받아 페이지 전체를 새로고침합니다 [cite: 60, 62, 63, 66-70].
* [cite_start]**SPA (Single-Page App)**: 초기 요청에만 HTML을 받고, 이후에는 AJAX를 통해 JSON 데이터만 받아 화면의 필요한 부분만 갱신합니다 [cite: 61, 71, 72-77].

### Node.js
* [cite_start]서버 측에서 자바스크립트를 실행할 수 있게 해주는 런타임 환경(Environment)입니다[cite: 243, 245, 254].
* [cite_start]OS나 웹 프레임워크가 아니며, 특정 운영체제에 종속되지 않고 실행 환경만을 제공합니다[cite: 257, 264, 276, 277].

### 개발 도구
* [cite_start]**IDE**: 코드 편집, 디버깅, 빌드 등을 하나로 통합한 도구입니다 (예: Visual Studio, IntelliJ IDEA) [cite: 306, 307, 310-313, 321, 322].
* [cite_start]**코드 편집기**: 가볍고 빠른 성능을 제공하며, 특히 **VS Code**는 크로스 플랫폼과 풍부한 확장 기능을 지원하여 널리 쓰입니다[cite: 323, 326, 327, 332, 334, 336].

---

## 2. React와 CRA (Create React App)

### npm vs npx
* [cite_start]**npm**: Node.js 패키지를 설치하고 의존성을 관리하는 패키지 매니저입니다[cite: 350, 352, 357].
* [cite_start]**npx**: 패키지를 로컬에 설치하지 않고 일회성으로 바로 실행하는 도구입니다[cite: 353, 355, 357].

### Vite vs Webpack
| 구분 | Vite | Webpack |
| :--- | :--- | :--- |
| **개발 서버 속도** | [cite_start]빠름 (ESM 기반) [cite: 369] | [cite_start]느림 (번들링 필요) [cite: 369] |
| **HMR 지원** | [cite_start]즉각적 반영 [cite: 369] | [cite_start]상대적으로 느림 [cite: 369] |
| **번들링 방식** | [cite_start]필요할 때만 빌드 [cite: 369] | [cite_start]전체 파일 번들링 [cite: 369] |

### 리액트 프로젝트 생성 명령어
* [cite_start]**Vite 사용 (권장)**: `npm create vite@latest 프로젝트명 --template react` 후 `npm install` 및 `npm run dev` 실행[cite: 380].
* [cite_start]**CRA 사용**: `npx create-react-app 프로젝트명` 후 `npm start` 실행[cite: 380].

---

## 3. JSX (JavaScript XML)

* [cite_start]JavaScript 코드 안에서 HTML과 유사한 마크업을 사용할 수 있게 해주는 문법 확장입니다 [cite: 383-385].
* [cite_start]Babel을 이용해 `React.createElement()` 형태의 JavaScript로 변환됩니다[cite: 390, 397, 399].
* [cite_start]**장점**: 코드가 직관적이고 가독성이 좋으며, 조건부 렌더링 및 이벤트 핸들링 구현이 쉽습니다[cite: 413, 421, 455, 469].

### JSX 주요 문법 및 사용법
* [cite_start]**기본 구조**: 반드시 하나의 부모 요소(예: `<div>` 또는 `<>`)로 감싸야 합니다[cite: 488, 500, 508].
* [cite_start]**표현식**: 자바스크립트 변수나 표현식은 `{}`로 감싸서 사용합니다[cite: 518, 521, 524].
* [cite_start]**속성(Props)**: HTML의 `class` 대신 `className`을 사용하고, 인라인 스타일은 `style={{ 속성: "값" }}` 형태의 객체로 전달합니다[cite: 392, 536, 544, 547].
* [cite_start]**조건부 렌더링**: 삼항 연산자(`조건 ? 참 : 거짓`) 또는 `&&` 연산자를 활용합니다[cite: 555, 558, 560, 565].
* [cite_start]**반복문**: 배열의 `map()` 메서드를 사용하며, 최상위 반복 요소에는 고유한 `key` 속성이 필수입니다 [cite: 572-574, 578-580, 584].
* [cite_start]**이벤트 처리**: `onClick`, `onChange` 등 카멜 케이스(CamelCase)로 작성합니다[cite: 588, 590, 596].
