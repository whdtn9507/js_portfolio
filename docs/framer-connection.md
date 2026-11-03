# Framer 연결 검증 기록

검증일: 2026-11-03 (Asia/Seoul)

## 대상과 확인 결과

| 항목 | 확인 값 |
| --- | --- |
| 소유자 | 한종수 |
| GitHub 저장소 | https://github.com/whdtn9507/js_portfolio |
| Framer Workspace | 종수's Workspace |
| 프로젝트 이름 | Devfolio - Software Engineer Portfolio and Agency template (copy) |
| 프로젝트 ID | a4DYM9E5gPhRx0PF4qQU |
| 프로젝트 URL | https://framer.com/projects/a4DYM9E5gPhRx0PF4qQU |
| 조회 당시 Framer 활성 브랜치 | main |
| GitHub 설정 브랜치 | work/devfolio-framer-setup |

연결된 Framer 도구의 list_projects에서 해당 프로젝트를 확인했고, open_project로 세션을 연 뒤 read_docs로 context.md를 읽었다. context.md에서 사용자 이름 한종수와 활성 브랜치 main을 확인했다. 따라서 해당 프로젝트에 접근하고 프로젝트 문서를 읽는 연결은 검증됐다.

프로젝트 트리·페이지·CMS 데이터는 이번 설정에서 조회하거나 수정하지 않았다. 편집 권한, CMS 구조, 미리보기, Publish 가능 여부는 테스트하지 않았다. Framer에 쓰기나 Publish를 실행하지 않았다.

이 기록은 검증 당시의 증거이며 영구 연결이나 GitHub–Framer 자동 동기화를 구성했다는 의미가 아니다. 이후 실행에서는 현재 도구 연결과 프로젝트 상태를 다시 확인해야 한다. 세션 핸들이나 자격 증명은 저장하지 않는다.

## GitHub 보존 기준

- 설정 시작 main 커밋: `c496ca5e94ea312762a9208a4f513c12baa95983`
- 기존 README.md blob SHA: `6e9b81333edd3fe9f090382189ca2e1589ca16c9`
- README.md 내용: `# js_portfolio`
- 설정은 위 커밋에서 분기한 작업 브랜치에 새 문서만 추가한다. README.md blob을 그대로 유지한다.

## 사용

루트 AGENTS.md를 따르고 [실행 프롬프트](../prompts/devfolio-framer.md)로 현황 조사부터 시작한다. 기존 CMS 삭제, GitHub main 직접 수정, Publish는 금지한다.
