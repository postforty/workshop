# 구조화된 데이터 예시

동일한 데이터를 구조화된 형식으로 변환한 예시입니다.

## text

```text
=== 사용자 프로필 (User Profile) ===

[기본 정보]
이름: 김일남 (Kim Il-nam)
아이디: gildong.hong
이메일: gildong@example.com
가입일: 2023-10-25

[역할 및 권한]
직책: Senior Developer
권한:
  - 프로젝트 생성: ✓
  - 팀원 관리: ✓
  - 시스템 설정: ✗

[기술 스택]
Frontend: React, TypeScript, TailwindCSS
Backend: Node.js, Python (FastAPI)
DevOps: Docker, AWS, GitHub Actions

[최근 활동 로그]
2023-11-01 | Login          | Connected from Busan (KR) IP
2023-10-30 | Code Review    | Approved PR #1024
2023-10-28 | Documentation  | Updated API Specification

[자기소개]
안녕하세요! 효율적인 코드와 깔끔한 아키텍처를 사랑하는 개발자입니다. 
새로운 기술을 배우고 공유하는 것을 좋아합니다.
```

## markdown

```markdown
# 사용자 프로필 (User Profile)

## 기본 정보
- 이름: 김일남 (Kim Il-nam)
- 아이디: `gildong.hong`
- 이메일: gildong@example.com
- 가입일: 2023-10-25

## 역할 및 권한
- 직책: 시니어 개발자 (Senior Developer)
- 권한:
  - [x] 프로젝트 생성
  - [x] 팀원 관리
  - [ ] 시스템 설정

## 기술 스택
1. Frontend: React, TypeScript, TailwindCSS
2. Backend: Node.js, Python (FastAPI)
3. DevOps: Docker, AWS, GitHub Actions

## 최근 활동 로그
| 날짜 | 활동 유형 | 설명 |
| :--- | :---: | :--- |
| 2023-11-01 | 로그인 | 부산(KR) IP에서 접속 |
| 2023-10-30 | 코드 리뷰 | PR #1024 승인 |
| 2023-10-28 | 문서 작성 | API 명세서 업데이트 |

## 자기소개
> "안녕하세요! 효율적인 코드와 깔끔한 아키텍처를 사랑하는 개발자입니다. 
> 새로운 기술을 배우고 공유하는 것을 좋아합니다."
```

## json

```json
{
  "user_profile": {
    "basic_info": {
      "name": "김일남 (Kim Il-nam)",
      "id": "gildong.hong",
      "email": "gildong@example.com",
      "join_date": "2023-10-25"
    },
    "role_and_permissions": {
      "position": "Senior Developer",
      "permissions": {
        "create_project": true,
        "manage_team": true,
        "system_settings": false
      }
    },
    "tech_stack": {
      "frontend": ["React", "TypeScript", "TailwindCSS"],
      "backend": ["Node.js", "Python (FastAPI)"],
      "devops": ["Docker", "AWS", "GitHub Actions"]
    },
    "recent_activity_log": [
      {
        "date": "2023-11-01",
        "type": "Login",
        "description": "Connected from Busan (KR) IP"
      },
      {
        "date": "2023-10-30",
        "type": "Code Review",
        "description": "Approved PR #1024"
      },
      {
        "date": "2023-10-28",
        "type": "Documentation",
        "description": "Updated API Specification"
      }
    ],
    "bio": "안녕하세요! 효율적인 코드와 깔끔한 아키텍처를 사랑하는 개발자입니다. 새로운 기술을 배우고 공유하는 것을 좋아합니다."
  }
}
```

## xml

```xml
<user_profile>
  <basic_info>
    <name>김일남 (Kim Il-nam)</name>
    <id>gildong.hong</id>
    <email>gildong@example.com</email>
    <join_date>2023-10-25</join_date>
  </basic_info>
  <role_and_permissions>
    <position>Senior Developer</position>
    <permissions>
      <create_project>true</create_project>
      <manage_team>true</manage_team>
      <system_settings>false</system_settings>
    </permissions>
  </role_and_permissions>
  <tech_stack>
    <frontend>
      <item>React</item>
      <item>TypeScript</item>
      <item>TailwindCSS</item>
    </frontend>
    <backend>
      <item>Node.js</item>
      <item>Python (FastAPI)</item>
    </backend>
    <devops>
      <item>Docker</item>
      <item>AWS</item>
      <item>GitHub Actions</item>
    </devops>
  </tech_stack>
  <recent_activity_log>
    <activity>
      <date>2023-11-01</date>
      <type>Login</type>
      <description>Connected from Busan (KR) IP</description>
    </activity>
    <activity>
      <date>2023-10-30</date>
      <type>Code Review</type>
      <description>Approved PR #1024</description>
    </activity>
    <activity>
      <date>2023-10-28</date>
      <type>Documentation</type>
      <description>Updated API Specification</description>
    </activity>
  </recent_activity_log>
  <bio>안녕하세요! 효율적인 코드와 깔끔한 아키텍처를 사랑하는 개발자입니다. 새로운 기술을 배우고 공유하는 것을 좋아합니다.</bio>
</user_profile>
```

## yaml

```yaml
user_profile:
  basic_info:
    name: "김일남 (Kim Il-nam)"
    id: gildong.hong
    email: gildong@example.com
    join_date: "2023-10-25"
  role_and_permissions:
    position: Senior Developer
    permissions:
      create_project: true
      manage_team: true
      system_settings: false
  tech_stack:
    frontend:
      - React
      - TypeScript
      - TailwindCSS
    backend:
      - Node.js
      - Python (FastAPI)
    devops:
      - Docker
      - AWS
      - GitHub Actions
  recent_activity_log:
    - date: "2023-11-01"
      type: Login
      description: Connected from Busan (KR) IP
    - date: "2023-10-30"
      type: Code Review
      description: "Approved PR #1024"
    - date: "2023-10-28"
      type: Documentation
      description: Updated API Specification
  bio: "안녕하세요! 효율적인 코드와 깔끔한 아키텍처를 사랑하는 개발자입니다. 새로운 기술을 배우고 공유하는 것을 좋아합니다."
```

## csv

```csv
section,field,value
basic_info,name,"김일남 (Kim Il-nam)"
basic_info,id,gildong.hong
basic_info,email,gildong@example.com
basic_info,join_date,2023-10-25
role_and_permissions,position,Senior Developer
permissions,create_project,true
permissions,manage_team,true
permissions,system_settings,false
tech_stack,frontend,"React, TypeScript, TailwindCSS"
tech_stack,backend,"Node.js, Python (FastAPI)"
tech_stack,devops,"Docker, AWS, GitHub Actions"
activity_log,2023-11-01,"Login: Connected from Busan (KR) IP"
activity_log,2023-10-30,"Code Review: Approved PR #1024"
activity_log,2023-10-28,"Documentation: Updated API Specification"
bio,description,"안녕하세요! 효율적인 코드와 깔끔한 아키텍처를 사랑하는 개발자입니다. 새로운 기술을 배우고 공유하는 것을 좋아합니다."
```
