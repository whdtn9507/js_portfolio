# DevFolio 디자인 및 반응형 기준

분석일: 2026-11-03 (Asia/Seoul). 대상 프로젝트 a4DYM9E5gPhRx0PF4qQU / Devfolio Portfolio. Framer main을 읽기 전용으로 조사했다. 아래는 관찰값과 후속 제안을 구분한 기록이다. 이번 작업에서 Framer는 수정·Publish하지 않는다.

## 현재 구조

| 페이지 | 경로 | ID |
| --- | --- | --- |
| Home | / | augiA20Il |
| Works 목록 | /works | gx6GSPkGA |
| Works 상세 | /works/:QpBYV7CMX | aVdv6Io0a |
| Contact | /contact | M1T49So5B |
| 404 | /404 | b0wcJYK14 |

Home에는 Hero, Quote, Service, Skills, Works, Career, Education, Testimonials, FAQ, Price, Contact 및 Footer 관련 구조가 있다. 일부 표시 제목은 About Me, Working Principles, Collaboration으로 바뀌어 있다. 레이어 이름만으로 실제 콘텐츠나 삭제 의도를 판단하지 않는다.

Layout Template ID는 dKbMLxjO9이며 그 배경은 Deepest Dark다. 공통 컴포넌트 정의는 26개로 조회됐다. Home의 Template Setup 등 보조 프레임도 보존한다.

CMS는 Works 7개, Career 2개 항목이다. 홈 Works List cDEragUeR와 목록 페이지 List hSR3ljqgz에 limit 6이 적용돼 있다. Career Collection ID는 KUvhlIMQ_다. 기존 컬렉션·필드·항목·바인딩·상태는 유지한다.

## 다크 테마 관찰값

| 토큰 이름 | 관찰된 값 |
| --- | --- |
| Deepest Dark | #050507 |
| Main Background | #0A0A0F |
| Section Background | #12131A |
| Surface Background / Dark Surface | #1A1B23 |
| Surface Secondary | #2A2B35 |
| Brand Primary | #6366F1 |
| Whilte 100% | #FFFFFF |
| Whilte 80% / 60% | white alpha 0.8 / 0.6 |

토큰의 기존 오탈자도 임의로 이름을 변경하지 않는다. 각 페이지 프레임에 white 속성이 조회되지만 실제 화면과 Layout Template은 어둡다. 이 한 속성만으로 테마가 흰색이라고 판단하거나 배경을 일괄 재설정하지 않는다.

기존 Hero의 그래픽, 인디고 CTA, 프로젝트 카드의 테두리와 표면 계층을 유지한다. Career/Education의 밝은 카드는 현재 관찰된 디자인 요소이며 임의로 전체 색을 바꾸지 않는다.

## Typography

현재 영문 Heading preset은 Bricolage Grotesque, Body preset은 Manrope로 확인됐다.

| Preset | Desktop | Tablet | Phone | Line height |
| --- | --- | --- | --- | --- |
| Heading 1 | 120px | 96px | 60px | 1.1em |
| Heading 2 | 60px | 48px | 40px | 1.4em |
| Heading 3 | 40px | 32px | 24px | 1.4em |
| Body 2 | 24px | 20px | 16px | 1.6em |

이는 기존 preset 값이며 모든 화면 텍스트의 최종 렌더링 수치가 아니다. 한국어로 바꾸면서 원래 크기를 기계적으로 적용하지 않는다.

후속 제안: 한글 glyph를 지원하는 프로젝트 내 Pretendard를 한국어 본문에 검토한다. 실제로 해당 노드에 적용된 폰트라고 단정하지 않는다. 영어 제목의 기존 성격은 보존한다. 한글 줄바꿈과 글자 잘림이 있을 때만 범위를 정해 font size·line height·text wrap을 보정한다. 모바일 Hero의 긴 문장은 의미 단위로 줄을 나누며 고정 개행을 모든 breakpoint에 공유하지 않는다.

## Layout / Responsive

관찰된 기본 프레임 폭은 Desktop 1200px, Tablet 810px, Phone 390px다. 텍스트 preset의 최소 폭 기준은 1200 / 810 / 0px다. 기본 폭을 모든 실제 기기 범위의 검증 완료로 표현하지 않는다.

Home의 주요 섹션은 Desktop에서 가로 padding 40px, 세로 약 100–128px를 사용하고, Hero Wrapper는 maxWidth 1400px와 별도 padding을 갖는다. 기존 공간 비율과 구성은 보존하며 임의의 새 디자인 시스템으로 교체하지 않는다.

후속 변경 기준:

- 기존 Stack/Grid와 컴포넌트 상속을 재사용한다. Layout Template이 breakpoint 구조를 소유하면 그 구조와 높이를 무작정 바꾸지 않는다.
- 한국어 콘텐츠 증가에 맞게 카드와 본문의 높이가 늘어나도록 하고 고정 높이로 잘라내지 않는다.
- 모바일 Skills 카드가 화면 밖으로 벗어나지 않도록 열 수·최소 폭·텍스트 wrap·부모 padding을 점검한다.
- 좁은 폭에서 프로젝트는 읽을 수 있는 단일 열로 유지하고 이미지 비율을 보존한다.
- 320, 375, 390, 810, 1200, 1440px 및 경계 809/810, 1199/1200px를 검증 폭으로 제안한다. 지금 모두 테스트한 것은 아니다.
- 텍스트가 있는 가시적 컨테이너에는 가로 여백을 유지한다. full-bleed 배경과 내부 콘텐츠 max-width를 구분한다.
- 긴 영문 기술명과 한국어 제목이 CTA·카드·폼을 밀어내지 않는지 확인한다.

## 읽기 전용 시각 점검 결과

Desktop 1200px와 Phone 390px의 Home 캡처를 열어 확인했다. 내보내기나 공개 사이트 기능 테스트는 수행하지 않았다. 캡처 파일이나 이미지 자산을 저장소에 첨부하지 않는다.

| 관찰 | 후속 검토 방향 |
| --- | --- |
| Hero와 일부 메뉴·FAQ에 템플릿 인물/이름이 남아 있음 | 실제 소유자 정보와 무관한 텍스트를 구분하고 편집 요청 범위에서 대체 |
| 서비스 설명에 Mobile App, Cloud, Blockchain 등의 템플릿 문구가 남아 있음 | PORTFOLIO_CONTENT.md의 근거 있는 경험과 맞춰 재작성. 해당 기술 경력 생성 금지 |
| Working Principles 제목 아래 고객 추천사·별점이 남아 있음 | 실제 추천으로 취급하지 않음. 후속 콘텐츠 정비 때 명시적으로 처리 범위 지정 |
| Collaboration 아래 템플릿 가격표가 남아 있음 | 실제 요금으로 노출하지 않도록 후속 검토. 가격 창작 금지 |
| Quote 뒤 큰 빈 공간 | 애니메이션·스크롤 동작과 컨테이너 높이를 구분해 확인. 캡처만으로 원인 확정 금지 |
| Phone Skills 2열 카드 일부가 잘림 | overflow·최소 폭·열 수를 우선 검증 |
| Phone Hero의 한글 제목 줄바꿈이 불안정함 | 한글 폰트와 wrap, 크기 및 콘텐츠 폭 점검 |
| PC/Phone에 영문 템플릿 카피가 혼재함 | 실제 변경할 문구를 지정하고 한국어 본문으로 통일 |

트리에서 ErrorNode 42개가 조회됐으나 상세 진단·심각도·발생 원인은 분류하지 않았다. 이를 새로 발생한 오류, 빌드 실패 또는 해결 완료로 보고하지 않는다. 읽기 프로그램의 changedNodeCount는 0이었다.

## 접근성 및 동작 검증 기준

후속 실제 UI 편집 시에만 결과를 확인해 기록한다.

- 제목 위계, 읽기 순서, 키보드 포커스와 메뉴 조작
- 링크·CTA 목적지 및 현재 CMS 목록→상세 연결, 기존 slug 보존
- 이미지의 맥락에 맞는 대체 텍스트, 장식 요소의 구분
- 텍스트와 배경의 대비를 실제 사용 색 조합에서 측정
- 버튼의 터치 영역과 카드 링크 구분, 긴 제목·Empty State
- 폼 label·필수값·오류 안내·제출 목적지. 실제 전송은 별도 권한 없이 테스트하지 않음
- 모션이 캡처나 내용 가독성을 방해하는지, reduced motion 대응

## 자료와 검증 한계

기존 사이트를 관찰해 문서로 정리한 것이며 새 UI의 구현 명세나 검증 통과 보고서가 아니다. 프로젝트 상세 전체 richtext, 모든 컴포넌트 variant, 실제 메뉴/폼/링크 동작 및 게시된 사이트는 이번 범위에서 검증하지 않았다. 사내 화면·타인 사진·개인 연락처를 저장소에 복제하지 않는다.
