# Bootstrap
> CSS 프론트엔드 프레임워크(Toolkit)
- 미리 만들어진 다양한 디자인 요소들을 제공하여 웹 사이트를 빠르고 쉽게 개바할 수 있도록 한다.

# CDN(Content Delivery Network)
> 지리적 제약 없이 빠르고 안전하게 콘텐츠를 전송할 수 있는 전송 기술
- 서버와 사용자 사이의 물리적인 거리를 줄여 콘텐츠 로딩에 소요되는 시간을 최소화한다. (웹 페이지 로드 속도를 높인다.)
- 지리적으로 사용자가와 가까운 CDN 서버에 콘텐츠를 저장해서 사용자에게 전달한다.

## Bootstrap CDN
1. Bootstrap 홈페이지 - Download - "Compiled CSS and JS" 다운로드
2. CDN을 통해 가져오는 bootstrap css와 js 파일을 확인
3. bootstrap.css, bootstrap.js 파일 참고
- 온라인 CDN 서버에 업로드 된 css 및 js 파일을 불러와서 사용하는 것

## Bootstrap 기본 사용법
```html
<p class="mt-5">Hello, world!</p>
```

### Bootstrap에서 클래스 이름으로 Spacing을 표현하는 방법
> {`property}{sides}-{size}`
- Bootstrap에는 특정한 규칙이 있는 클래스 이름으로 스타일 및 레이아웃이 미리 작성되어 있다.

### [참고] rem 단위
> `rem`은 "root em"의 약자로, HTML 문서의 **루트 요소(`html`)의 폰트 크기를 기준**으로 하는 상대적 단위이다.
- 대부분의 브라우저가 루트 폰트 크기를 **16px**로 기본 설정
- `1rem = html` 요소의 폰트 크기 (대부분 16px)
- 예시: 루트 폰트 크기가 16px일 때
  - `2rem == 32px`
  - `0.5rem == 8px`
  - `1.5rem == 24px`

## Bootstrap에서의 Reset CSS
- bootstrap은 `bootstrap-reboot.css`라는 파일명으로 `normalize.css`를 자체적으로 커스텀해서 사용하고 있다.

# Bootstrap 활용

## Typography
> 제목, 본문 텍스트, 목록 등
- Display headings : 기존 Heading보다 더 눈에 띄는 제목이 필요한 경우
- Inline text elements : HTML inline 요소에 대한 스타일
- Lists : HTML Lists 요소에 대한 스타일

## Colors
> Text, Border, Background 및 다양한 요소에 사용하는 Bootstrap의 색상 키워드
- Text colors : `class="text-color"`
- Background colors : `class="bg-color"`

## Component
> Bootstrap에서 제공하는 UI 관련 요소(버튼, 네비게이션 바, 카드, 폼, 드롭다운 등)
- 일관된 디자인을 제공하여 웹 사이트의 구성 요소를 구축하는 데 유용하게 활용할 수 있다.

### 대표 Component 사용해보기
- Alerts
- Badges
- Buttons
- Cards
- Navbar

### Bootstrap을 사용하는 이유
- 가장 많이 사용되는 CSS 프레임워크이기 때문이다.
- 사전에 디자인된 다양한 컴포넌트 및 기능을 사용할 수 있는데, 이는 빠른 개발과 유지보수를 용이하게 한다.
- 손쉬운 반응형 웹 디자인을 구현할 수 있다.
- 커스터마이징이 용이하다.
- 크로스 브라우징을 지원한다. 즉, 모든 주요 브라우저에서 작동하도록 설계되어 있다.