# 한종수 DevFolio 작업 공간

이 저장소는 한종수의 기존 Framer DevFolio 포트폴리오를 위한 작업 지침, 콘텐츠 초안, 검증 기록을 관리한다. 화면과 CMS의 현재 상태는 Framer에서 확인한다. 이 저장소를 Framer 사이트 소스의 자동 동기화 또는 배포 설정으로 취급하지 않는다.

## 작업 대상

- GitHub: https://github.com/whdtn9507/js_portfolio
- Framer: https://framer.com/projects/a4DYM9E5gPhRx0PF4qQU
- 프로젝트: Devfolio - Software Engineer Portfolio and Agency template (copy)
- Workspace: 종수's Workspace
- 포트폴리오 소유자: 한종수
- 사용자 일정과 기록 기준: Asia/Seoul
- 연결 검증 근거: [docs/framer-connection.md](docs/framer-connection.md)

## 변경 경계

- 기존 README.md를 그대로 보존한다.
- GitHub main에는 직접 커밋하거나 push하지 않는다. 기본 작업 브랜치는 `work/devfolio-framer-setup`이며, 후속 작업도 별도 작업 브랜치를 사용한다. main 병합은 현재 범위 밖이다.
- 기존 CMS 컬렉션, 항목, 필드 및 연결을 삭제하지 않는다. 초기화를 위한 일괄 교체, 필드 재생성, 데이터 손실을 일으키는 타입 변경도 하지 않는다.
- Publish, 배포, 도메인 연결/변경을 실행하지 않는다.
- 현재 설정 작업은 저장소 문서 구성과 Framer 읽기 검증만 허용한다. 이 파일이나 실행 프롬프트 자체가 Framer 편집 권한을 부여하지 않는다. 후속 사용자 요청이 지정한 범위 안에서만 편집한다.
- 자격 증명, API 키, 세션 핸들을 저장소에 기록하지 않는다.
- 경력, 프로젝트 성과, 연락처, 학력, 고객 추천 등을 지어내지 않는다. 템플릿 예시를 한종수의 실제 이력으로 단정하지 않는다.

## 작업 방법

Framer DevFolio 작업에는 [.agents/skills/devfolio-framer/SKILL.md](.agents/skills/devfolio-framer/SKILL.md)를 읽고 적용한다. 시작용 요청문은 [prompts/devfolio-framer.md](prompts/devfolio-framer.md)에 있다.

Framer는 연결된 Framer 도구로 접근한다. 유효한 세션이 없을 때만 지정 프로젝트를 열고, 반환된 README와 context.md 및 작업에 맞는 문서를 읽는다. 연결이 실패하면 오류와 미검증 범위를 보고하고 프로젝트를 새로 만들거나 다른 프로젝트로 대체하지 않는다.

GitHub 브랜치는 Framer 편집 상태를 격리하거나 자동으로 동기화하지 않는다. Framer의 실제 활성 프로젝트와 브랜치를 매번 확인하고, 사용자 수동 변경을 다시 읽은 뒤 최소 범위만 수정한다. 실패한 쓰기는 부분 반영될 수 있으므로 상태 확인 없이 재실행하지 않는다.

완료 보고에는 변경 파일/화면, 검증한 내용, 미확인 사항, 남은 입력을 구분한다. 연결 확인을 편집·CMS 검증·게시 성공으로 표현하지 않는다.
