https://ftpserver.ksecole.kr

ID : webapp
PW : webapp2026

**vs code code snippet에 대해 설명해줘**
VS Code: 코드 스니펫 (Code Snippet)
📌 정의 및 목적
코드 스니펫은 반복적으로 사용되는 코드 패턴을 줄임말(Trigger) 하나로 즉시 불러오는 자동 완성 기능입니다.

"단순한 타이핑 도구를 넘어, 개발의 생산성과 일관성을 높이는 필수 기능입니다."

🔹 주요 장점
생산성 극대화: 수십 줄의 보일러플레이트(Boilerplate) 코드를 단 몇 글자로 입력하여 개발 시간을 단축합니다.

오류 방지: 복잡한 문법 구조를 미리 템플릿화하여 오타로 인한 런타임 에러를 방지합니다.

표준화: 팀 단위 프로젝트에서 공통된 코드 스타일(컨벤션)을 유지하기 용이합니다.

🛠️ 사용자 정의 스니펫 예시 (JSON)
사용자가 직접 sout이라는 줄임말을 설정하여 자바의 출력문을 자동 완성하는 예시입니다.

JSON
{
  "Java System Out": {
    "prefix": "sout",
    "body": [
      "System.out.println($1);"
    ],
    "description": "콘솔 출력을 위한 System.out.println() 스니펫"
  }
}
prefix: 스니펫을 실행할 키워드 (입력창에 sout 입력)

body: 실제 삽입될 코드 내용 ($1은 자동 완성 후 커서가 위치할 지점)

description: 해당 스니펫에 대한 설명
-제미나이
