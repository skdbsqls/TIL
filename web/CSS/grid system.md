# Bootstrap Grid system
> 웹 페이지의 레이아웃을 조정하는 데 사용되는 12개의 컬럼으로 구성된 시스템

## Grid system 목적
반응형 디자인을 지원해 웹 페이지를 모바일, 태블릿, 데스크탑 등 다양한 기기에서 적절하게 표시할 수 있도록 돕는다.

## Grid system 구성
1. Container : Column들을 담고 있는 공간

2. Column : 실제 컨텐츠를 포함하는 부분

3. Gutter : 컬럼과 컬럼 사이의 여백 영역(상하좌우)

- 1개의 row안에 12개의 column 영역이 구성
- 각 요소는 12개 중 몇 개를 차지할 것인지 지정

## Grid System 실습

### Basic
```html
  <div class="container">
    <div class="row">
      <div class="col-4"></div>
      <div class="col-4"></div>
      <div class="col-4"></div>
    </div>
  </div>
```
- `<div class="container">` : 좌우에 적당한 여백을 주면서 콘텐츠를 가운데 정렬
- `<div class="row">` : column을 담을 공간 설정
- `<div class="col">` : `col`만 작성하면 12개의 영역을 알아서 분배, 기본적으로 gutter도 설정되어 있음, `col-num` 칸수를 표현하는 것이 권장됨
- column이 12개 보다 적으면 적은 칸 수 만큼 차지하지만, 12개 보다 크면 해당 row를 벗어나 아래로 내려감

### Nesting(중첩)
```html
  <div class="container">
    <div class="row">
      <div class="col-4 box">
        <div>col-4</div>
      </div>
      <div class="col-8 box">
        <div class="row">
          <div class="col-6">
            <div class="box">col-6</div>
          </div>
          <div class="col-6">
            <div class="box">col-6</div>
          </div>
          <div class="col-6">
            <div class="box">col-6</div>
          </div>
          <div class="col-6">
            <div class="box">col-6</div>
          </div>
        </div>
      </div>
    </div>
  </div>
```

### Offset(상쇄)
```html
  <div class="container">
    <div class="row">
      <div class="col-4">
        <div class="box">col-4</div>
      </div>
      <div class="col-4 offset-4">
        <div class="box">col-4 offset-4</div>
      </div>
    </div>
    <div class="row">
      <div class="col-3 offset-3">
        <div class="box">col-3 offset-3</div>
      </div>
      <div class="col-3 offset-3">
        <div class="box">col-3 offset-3</div>
      </div>
    </div>
    <div class="row">
      <div class="col-6 offset-3">
        <div class="box">col-6 offset-3</div>
      </div>
    </div>
  </div>
```
- 특정한 column을 상쇄하고 다음 column을 등장시킴
- 상쇄 시킬 column 다음에 오는 column에 `offset-num`을 통해 앞에 상쇄 시킬 column의 개수를 지정

## Gutters
> Gird system에서 column 사이에 여백 영역
- x축은 `padding`, y축은 `margin`으로 여백을 생성한다.
- 실제 컬럼 간에 좌우 간격(x축)은 변하지 않으며, `padding`으로 인해 컬럼 안데 contents의 너비가 변하는 것이다.

```html
  <div class="container">
    <div class="row gx-0">
      <div class="col-6">
        <div class="box">col</div>
      </div>
      <div class="col-6">
        <div class="box">col</div>
      </div>
    </div>
  </div>
```
- x축 기준 gutter는 column를 감싸는 row에서 `gx-num`으로 설정(padding)
- y축 기준 gutter는 column를 감싸는 row에서 `gy-num`으로 설정(margin)
- `g-num`로 설정하면 x, y축 모두 gutter 설정 가능
