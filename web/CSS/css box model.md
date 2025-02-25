# CSS Box Model
웹 페이지의 모든 HTML 요소를 감싸는 사각형 상자 모델로 내용(content), 안쪽 여백(padding), 테두리(border), 외부 간격(padding)으로 구성되어 요소의 크기와 배치를 결정한다.

- Margin : 박스와 다른 요소 사이의 공백, 가장 바깥쪽 영역
- Border : 콘텐츠와 패딩을 감싸는 테두리 영역
- Padding : 콘텐츠 주위의 위치하는 공백 영역
- Content : 콘텐츠가 표시되는 영역

 ## Box 구성 요소
- Content box : 실제 콘텐츠가 표시되는 영역 크기로, `width` 와 `height` 속성을 사용하여 크기를 조정한다.
- Padding box : 콘텐츠 주위의 공백으로, `padding` 관련 속성을 사용하여 크기를 조정한다.
- Border box : 콘텐츠와 패딩을 래핑하며, `border` 관련 속성을 사용하여 크기를 조정한다.
- Margin Box : 콘텐츠와 패딩 그리고 테두리를 래핑하며, 박스와 다른 요소 사이의 공백을 결정하고, `margin` 관련 속성을 사용하여 크기를 조정한다.

### Box 구성의 방향 별 속성 값
- top
- bottom
- left
- right

## shorthand 속성
- `borde`r : `border-width`, `border-style`, `border-color`를 한 번에 설정하기 위한 속성
- `margin` & `padding` : 4방향의 속성을 각각 지정하지 않고 한 번에 지정할 수 있는 속성
	- 4개 : 상/우/하/좌
	- 3개 : 상/좌우/하
	- 2개 : 상하/좌우
	- 1개 : 공통

## Box-Sizing 속성

### The standard CSS box model
- 표준 상자 모델에서 `width`와 `height` 속성 값을 설정하면 이 값은 content box의 크기를 조정하게 된다.
- CSS는 border box가 아닌 content box의 크기를 `wdith`값으로 지정한다.

### The alternative CSS box model
```css
* {
      box-sizing: border-box;
    }
```
- 대체 상자 모델에서 모든 `width`와 `height`는 실제 상자의 너비로 실제 박스 크기를 정하기 위해 테두리와 패딩을 조정할 필요가 없다.

## 기타 display 속성

### `inline-block`
- `inline`과 `block` 요소 사이의 중간 지점을 제공하는 display 값이다.
- `width` 및 `height` 속성 사용 가능하다.
- `padding`, `margin` 및 `border`로 인해 다른 요소가 상자에서 밀려난다.
- 새로운 행으로 넘어가지 않는다.
- 결국, 요소가 줄 바꿈 되는 것을 원하지 않으면서 너비와 높이를 적용하고 싶은 경우에 사용한다.

### `none`
- 요소를 화면에 표시하지 않고, 공간조차 부여되지 않는다.