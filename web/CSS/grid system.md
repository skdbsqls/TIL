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

# 반응형 웹 디자인(Responsive Web Design)
> 디바이스 종류나 화면 크기에 상관없이, 어디서든 일관된 레이아웃 및 사용자 경험을 제공하는 디자인 기술

## Grid system breakpoints
> 웹 페이지를 다양한 화면 크기에서 적잘하게 배치하기 위한 분기점
```html
  <div class="container">
    <div class="row">
      <div class="col-12 col-sm-6 col-md-2 col-lg-3 col-xl-4">
        <div class="box">col</div>
      </div>
      <div class="col-12 col-sm-6 col-md-8 col-lg-3 col-xl-4">
        <div class="box">col</div>
      </div>
      <div class="col-12 col-sm-6 col-md-2 col-lg-3 col-xl-4">
        <div class="box">col</div>
      </div>
      <div class="col-12 col-sm-6 col-md-12 col-lg-3 col-xl-12">
        <div class="box">col</div>
      </div>
    </div>
  </div>
```
- Bootstrap grid system에서는 12개 column과 6개 breakpoints를 사용하여 반응형 웹 디자인을 구현한다.
- 화면 너비에 따라 6개의 분기점을 제공한다.
- `xs`, `sm`, `md`, `lg`, `xl`, `xxl`
- `col-size-num`, `xs`은 기본값으로 size를 작성하지 않으면 `xs`이다.
- 각 breakpoints 마다 설정된 최대 너비 값 **이상으로** 화면이 커지면 grid system 동작이 변경된다.

### CSS Layout 종합 정리
- CSS 레이아웃 기술들은 각각 고유한 특성과 장단점을 가지고 있다.
- 이들은 상호 보완적이며, 특정 상황에 따라 적합한 도구가 달라진다.
- 최적의 기술을 선택하고 효과적으로 활용하기 위해서는 다양한 실제 개발 경험이 필수적이다.