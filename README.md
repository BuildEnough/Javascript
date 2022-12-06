# 2022년 12월 4일
프로그래머의 역할은 요구사항을 기반으로 문제를 해결하기 위한 방안을 고안하고 이를 코드로 구현하는 것  
구현된 코드는 의도한 대로 정확히 동작해서 문제를 해결해야 함  
자신이 구현한 코드가 컴퓨터 내부에서 어떻게 동작할 것인지 예측 가능해야하며, 이를 명확히 설명할 수 있어야 한다
> 빨리 가는 유일한 방법은 제대로 가는 것

<br>

### 크로스 브라우징 이슈  
**브라우저에 따라 웹페이지가 정상적으로 동작하지 않는 이슈**  
브라우저 종류가 다양함  
자사 브라우저에서만 동작하는 기능을 경쟁적으로 추가하면서 발생(시장 점유율을 높이기 위해서 등등...)  

<br>

### 렌더링  
HTML, CSS, 자바스크립트로 작성된 문서를 해석해서 브라우저에 시각적으로 출력하는 것  
서버에서 데이터를 HTML로 변환해서 브라우저에게 전달하는 과정(SSR: Server Side Rendering)

<br>

### Ajax  
자바스크립트를 이용해 서버와 브라우저가 비동기(`asynchronous`)방식으로 데이터를 교환할 수 있는 통신기능  
Ajax 등장 전: 웹페이지 전체 렌더링하는 방식, 화면이 전환되면 서버로부터 새로운 HTML을 전송받아 웹페이지 전체를 처음부터 렌더링  
Ajax 등장 후: 웹페이지에서 변경할 필요가 없는 부분은 다시 렌더링하지 않고, 서버로부터 필요한 데이터만 전송받아 변경해야 하는 부분만 한정적으로 렌더링하는 방식

<br>

### jQuery
DOM(Document Object Model)은 다소 번거롭고 논란이 있었지만 jQuery의 등장으로 DOM을 더욱 쉽게 제어할 수 있게 되었고 크로스 브라우징 이슈도 어느정도 해결됨
**솔직히 뭐라는지 잘 모름**

<br>

### V8 자바스크립트 엔진  
자바스크립트로 웹 애플리케이션을 구축하려는 시도가 늘어나면서 더욱 빠르게 동작하는 자바스크립트 엔진이 필요하게 되었고 `V8 자바스크립트 엔진`은 이러한 요구에 부합하는 빠른 성능을 보여줌

<br>

### Node.js 
V8 자바스크립트 엔진으로 빌드된 자바스크립트 런타임 환경
브라우저의 자바스크립트 엔진에서만 동작하던 자바스크립트를 브라우저 이외의 환경에도 동작할 수 있도록  
자바스크립트 엔진을 브라우저에서 독립시킨 자바스크립트 실행 환경  
다양한 플랫폼에 적용할 수 있지만 서버 사이드 애플리케이션 개발에 주로 사용됨

<br>

### 자바스크립트의 특징
HTML, CSS와 함께 웹을 구성하는 요소 중 하나로 웹 브라우저에서 동작하는 유일한 프로그래밍 언어  
개발자가 별도의 컴파일 작업을 수행하지 않는 `인터프리터 언어`  
인터프리터와 컴파일러의 장점을 결합해 비교적 처리 속도가 느린 인터프리터의 단점을 해결함

<br>

|컴파일러 언어|인터프리터 언어|
|---|---|
|코드가 실행되기 전 단계인 컴파일 타임에 소스코드 전체를 한번에 머신코드로 변환후 실행|코드가 실행되는 단계인 런타임에 문 단위로 한줄씩 중간코드인 바이트코드로 변환 후 실행|
|실행 파일 생성|실행 파일 생성하지 않음|
|컴파일 단계와 실행 단계가 분리되어 있음, 명시적인 컴파일 단계를 거치고, 명시적으로 실행 파일을 실행함|인터프리트 단계와 실행 단계가 분리되어 있지 않다, 한 줄씩 바이트코드로 변환하고 즉시 실행|
|실행에 앞서 컴파일은 단 한번 수행됨|코드가 실행될 때마다 인터프리트 과정이 반복 수행됨|
|컴파일과 실행 단계가 분리되어 있으므로 코드 실행속도 빠름|인터프리트 단계와 실행 단계가 분리되어 있지않고 반복수행되므로 코드 실행속도가 비교적 느림|

<br>

---
# 2022년 12월 6일
자스크립트는 명령형, 함수형, 프로토타입 기반 객체지향 프로그래밍을 지원하는 **멀티 패러다임 프로그래밍 언어**  
클래스 기반 객체지향 언어보다 효율적이면서 강력한 프로토타입 기반의 객체지향 언어  

<br>

### 자바 스크립트 실행환경
모든 브라우저는 자바스크립트를 해석하고 실행할 수 있는 자바스크립트 엔진을 내장하고 있다  
브라우저는 HTML, CSS, 자바스크립트를 실행해 웹페이지를 브라우저 화면에 렌더링하는 것이 주된 목적  

Node.js는 브라우저 외부에서 자바스크립트 실행 환경을 제공하는 것이 주된 목적  
따라서 Node.js는 DOM API를 제공하지 않는다(브라우저 외부 환경에서는 HTML 요소를 파싱해서 객체화한 DOM을 직접 다룰 필요가 없기 때문)  
반대로 Node.js에서는 파일을 생성하고 수정할 수 있는 파일 시스템을 기본 제공하지만 브라우저는 이를 지원하지 않는다  

웹 어플리케이켠의 자바스크립트는 사용자 컴퓨터의 브라우저에서 동작  
만약 브라우저를 통해 다운로드되어 실행되는 자바스크립트가 사용자 컴퓨터의 로컬 파일을 삭제하거나 수정하고 생성할 수 있다면 컴퓨터가 악성코드에 그대로 노출된 것과 마찬가지 이기 때문에 보안상의 이유로 브라우저 환경의 자바스크립트는 파일 시스템을 제공하지 않는다

<br>

### 개발자 도구
