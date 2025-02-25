# CSS Position

## CSS Layout
각 요소의 **위치**와 **크기를 조정**하여 웹 페이지의 디자인을 결정하는 것이다.
- `display`
- `position`
- `flexbox`

## CSS Position
- 요소를 Normal Flow에서 제거하여 다른 위치로 배치하는 것이다.
- 다른 요소 위에 올리기, 화면의 특정 위치에 고정시키기 등

### Position 이동 방향
- top
- right
- bottom
- left
- Z Axis

## Position 유형

### 1 .`static`
- 요소를 Normal Flow에 따라 배치한다.
- `top`, `right`, `bottom`, `left` 속성이 적용되지 않는다.
- 기본 값이다.

### 2. `relative`
- 요소를 Normal Flow에 따라 배치한다.
- 자신의 원래 위치(`static`)을 기준으로 이동한다.
- `top`, `right`, `bottom`, `left` 속성으로 위치를 조정한다.
- 다른 요소와 레이아웃에 영향을 주지 않는다.
- 요소가 차지하는 공간은 `static`일 때와 같다.

### 3. `absolute`
- 요소를 Normal Flow에서 제거한다.
- 가장 가까운 `relative` 부모 요소를 기준으로 이동한다.
	- 만족하는 부모 요소가 없다면 `body`태그를 기준으로 한다.
- `top`, `right`, `bottom`, `left` 속성으로 위치를 조정한다.
- 문서에서 요소가 차지하는 공간이 없어진다.

### 4. `fixed`
- 요소를 Normal Flow에서 제거한다.
- 현재 화면 영역(viewport)을 기준으로 이동한다.
- 스크롤을 해도 항상 같은 위치에 유지된다.
- `top`, `right`, `bottom`, `left` 속성으로 위치를 조정한다.
- 문서에서 요소가 차지하는 공간이 없어진다.

### 5. `sticky`
- `relative`와 `fixed`의 특성을 결합한 속성이다.
- 스크롤 위치가 임계점이 도달하기 전에는 `relative`처럼 동작한다.
- 스크롤이 특정 임계점에 도달하면 `fixed`처럼 동작하여 화면에 고정된다. 
- 만약 다음 `sticky` 요소가 나오면 다음 `sticky` 요소가 이전 `sticky` 요소의 자리를 대체한다.
- 이전 `sticky` 요소가 고정되어 있던 위치와 다음 `sticky`요소가 고정되어야할 위치가 겹치게 되기 때문이다.

### 6. `z-index`
- 요소의 쌓임 순서(stack order)를 정의하는 속성이다.
- 정수 값을 사용해 Z축 순서를 지정한다.
- 값이 클수록 요소가 위에 쌓이게 된다.
- `static`이 아닌 요소에만 적용된다.
- 기본값은 `auto`이다.
- 부모 요소의 `z-index` 값에 영향을 받는다.
- 같은 부모 내에서만 `z-index` 값을 비교한다.
- 부모의 `z-index`가 낮으면 자식의 `z-index`가 아무리 높아도 부모보다 위로 올라갈 수 없다.
- `z-index` 값이 같으면 HTML 문서 순서대로 쌓인다.

## Position의 목적
: 전체 페이지에 대한 레이아웃을 구성하는 것보다는 **페이지 특정 항목의 위치를 조정하는 것**이다.
