# CSS Flexbox
요소를 행과 열 형태로 배치하는 1차원 레이아웃 방식으로 공간을 배열하거나 정렬한다.

## Flexbox 구성 요소
- Flex Container : `display: flex;` 혹은 `displayL inline-flex;`가 설정된 부모 요소로 이 컨테이너의 1차 자식 요소들이 Flex item이 된다. 
    - 즉, flexbox 속성 값들을 사용하여 자식 요소, Flex item들을 배치하는 주체이다.
- Flex item
- main axis(주 축) : flex item들이 배치되는 기본 축으로 main start에서 시작하여 main end 방향으로 배치한다. (기본 값)
- cross axis(교차 축) : main axis에 수직인 축으로 cross start에서 시작하여 cross end 방향으로 배치한다. (기본 값)

## Flexbox 속성 목록
- Flex Container 관련 속성 : `display`, `flex-direction`, `flex-wrap`, -`justify-content`, `align-items`, `align-content`
- Flex Item 관련 속성 : `align-self`, `flex-grow`, `flex-basis`, `order`

### 1. Flex Container 지정
- flex item은 기본적응로 행(주 축의 기본값인 가로 방향)으로 나열된다.
- flex item은 주 축의 시작 선에서 시작한다.
- flex item은 교차 축의 크기를 채우기 위해 늘어난다.

### 2. `flex-direction`
- flex item이 나열되는 방향을 지정한다.
- column으로 지정할 경우 주 축이 변경된다.
- `-reverse`로 지정하면 flex item 배치의 시작 선과 끝 선이 서로 바뀐다.

### 3. `flex-wrap`
- flex item 목록이 flex container의 한 행에 들어가지 않을 경우 다른 행에 배치할 지 여부를 설정한다.

### 4. `justify-content`
- 주 축을 따라 flex item과 주위에 공간을 분배한다.

### 5. `align-content`
- 교차 축을 따라 flex item과 주위에 공간을 분배한다.
- `flex-wrap`이 `wrap` 또는 `wrap-reverse`로 설정된 여러 행에만 적용된다.
- 한 줄짜리 행에는 효과가 없다.

### 6. `align-items`
- 교차 축을 따라 flex item 행을 정렬한다.

### 7. `align-self`
- 교차 축을 따라 개별 flex item을 정렬한다.

## 목적에 따른 속성 분류
- 배치 : `flex-direction`, `flex-wrap`
- 공간 분배 : `justify-content`, `align-content`
- 정렬 : `align-items`, `align-self`

속성명 Tip : justify(주 축), align(교차 축)

`justify-items` 및 `justify-self` 속성이 없는 이유? `margin auto`를 통해 정렬 및 배치가 가능하기 때문이다.

### 8. `flex-grow`
- 남는 행 여백을 비율에 따라 각 flex item에 분재한다.
- 아이템이 컨테이너 내에서 확장하는 비율을 지정한다.
- `flex-grow`의 반대는 `flex-shrink`이다.

### 9. `flex-basis`
- flex item의 초기 크기 값을 지정한다.
- `flex-basis`와 `width` 값을 동시에 적용한 경우 `flex- basis`가 우선이다.

## `flex-wrap` 응용

### 반응형 레이아웃
다양한 디바이스와 화면 크기에 자동으로 적응하여 콘텐츠를 최적으로 표시하는 웹 레이아웃 방식이다.
- `flex-wrap`을 사용해 반응형 레이아웃을 작성한다. (`flex-grow` & `flex-basis` 활용)
