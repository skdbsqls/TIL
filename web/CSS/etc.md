## [참고]

### Margin collapsing(마진 상쇄)
- 두 block 타입 요소의 `margin top`과 `bottom`이 만나 더 큰 `margin`으로 결합되는 현상이다.
- 왜? 복잡한 레이아웃에서 요소 간 간격을 일관되게 유지하기 위해서.
- 요소 간 간격을 더 예측 가능하고 관리하기 쉽게 만든다.
- 즉, 일관성과 단수화를 위함이다.

### 박스 타입 별 수평 정렬
- Block 요소의 수평 정렬 : `margin: auto;`를 사용하여 블록 요소의 너비를 지정하고 좌우 마진을 `auto`로 설정한다.
- Inline 요소의 수평 정렬 : `text-align`을 사용하여 부모 요소에 적용한다.

### Flexbox Shorthand 속성
- `flex-flow` : flex-direction flex-wrap