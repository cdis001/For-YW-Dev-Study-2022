# 3. 인터넷 기초

## 1. 인터넷 동작 원리
> https://developer.mozilla.org/docs/Learn/Common_questions/How_does_the_Internet_work
- 인터넷은 컴퓨터끼리 연결하고 연결 상태를 유지할 수있는 방법을 찾는 방법
- 웹을 가능하게 하는 기술 인프라인 웹의 중추
- 함께 통신하는 거대한 컴퓨터 네트워크

### 네트워크
- 두 개의 컴퓨터가 통신이 필요할 때, 우리는 다른 컴퓨터와 물리적으로 (보통 케이블) 또는 무선으로 (WiFi or Bluetooth) 연결되어야 함. 
- 이렇게 연결할 수록 매우 복잡해짐. 
   - 10대의 컴퓨터를 연결하려는 경우 컴퓨터 당 9개의 플러그가 달린 45개의 케이블이 필요
- 네트워크의 각 컴퓨터는 라우터라고하는 특수한 소형 컴퓨터에 연결
   - 라우터는 컴퓨터에서 보낸 메시지가 올바른 대상 컴퓨터에 도착하는지 확인하는 단순한 기능만 있음
   - 컴퓨터 B에게 메시지를 보내려면 컴퓨터 A가 메시지를 라우터로 보내야하며, 라우터는 메시지를 컴퓨터 B로 전달하고 메시지가 컴퓨터 C로 배달되지 않도록 해야 함
- 라우터를 시스템에 추가하면 10대의 컴퓨터 네트워크에는 10개의 케이블만 필요함. 
   - 각 컴퓨터마다 단일 플러그와 10개의 플러그가 있는 하나의 라우터가 필요
- 수백, 수천, 수십억 대의 컴퓨터를 연결하기 위해 두 대의 라우터를 연결하여 무한히 확장함
- 개인 네트워크를 가질 수는 있으나, 아주 먼 곳에 케이블이 연결되어 있지 않으므로 먼 곳과는 통신하기 힘듦
- 전화기 기반의 시설은 이미 세계 어느 곳과도 연결되어 있어, 네트워크를 연결하기에 최적화 되어있음
- 네트워크를 전화 시설과 연결하기 위해선, 모뎀이라는 특수 장비가 필요
- 모뎀은 우리 네트워크의 정보를 전화 시설에서 처리 할 수있는 정보로 바꾸며, 그 반대의 경우도 마찬가지
- 다음은 우리의 네트워크에서 도달하려는 네트워크로 메시지를 보내야하므로 네트워크를 인터넷 서비스 제공 업체 (Internet Service Provider, ISP)에 연결
   - ISP는 모두 함께 연결되는 몇몇 특수한 라우터를 관리하고 다른 ISP의 라우터에도 액세스 할 수 있는 회사
- 우리 네트워크의 메시지는 ISP 네트워크를 통해 대상 네트워크로 전달
- 인터넷은 이러한 전체 네트워크 인프라로 구성

### IP(Internet Protocol)
- 네트워크에 연결된 컴퓨터의 고유한 주소
- 컴퓨터에 메시지를 보내려면 메시지를 받을 특정 컴퓨터를 지정해야 하므로, IP를 이용해 주소를 찾음
- 점으로 구분 된 네 개의 숫자로 구성된 주소
- IP주소를 기억하기 어렵기 때문에 그래서 우리는 '도메인 이름(DNS)' 이라는 사람이 읽을 수 있도록 IP 주소의 이름을 지정할 수 있음

## 2. DNS
- 호스트의 도메인 이름을 호스트의 네트워크 주소로 바꾸거나 그 반대의 변환을 수행할 수 있도록 하기 위해 개발
- 도메인 네임 시스템은 흔히 "전화번호부"에 비유
- 인터넷은 2개의 주요 이름공간을 관리하는데, 하나는 도메인 이름 계층, 다른 하나는 인터넷 프로토콜(IP) 주소 공간
- 도메인 네임 시스템은 도메인 네임 계층을 관리하며 해당 네임 계층과 주소 공간 간의 변환 서비스를 제공
- 인터넷 네임 서버와 통신 프로토콜로 도메인 네임 시스템을 구현
- DNS 네임 서버는 도메인을 위한 DNS 레코드를 저장하는 서버
- DNS 네임 서버는 데이터베이스에 대한 쿼리의 응답 정보와 함께 응답

## 3. 웹
> https://developer.mozilla.org/ko/docs/Learn/Getting_started_with_the_web/How_the_Web_works

### 구조
- 클라이언트
   1. 일반적인 웹 사용자의 인터넷이 연결된 장치
      - 컴퓨터는 WI-FI에 연결되어 있고, 또는 휴대폰은 모바일 네트워크에 연결되어 있음
   2. 위 장치들에서 이용가능한 웹에 접근하는 소프트웨어 
      - 파이어폭스 또는 크롬 과 같은 웹 브라우저
- 서버
   - 웹페이지, 사이트, 또는 앱을 저장하는 컴퓨터
   - 클라이언트의 장비가 웹페이지에 접근하길 원할 때, 서버로부터 클라이언트의 장치로 사용자의 웹 브라우저에서 보여지기 위한 웹페이지의 사본이 다운로드 됨

   - 웹 애플리케이션 서버(WAS)
      - 브라우저와 DBMS(데이터 베이스 관리 시스템) 사이에서 동작하는 미들웨어
         - 미들웨어: 클라이언트와 DBMS 사이에서 중개 역할을 하는 소프트웨어
      - 역할
         - 프로그램 실행 환경과 데이터 베이스 접속 기능 제공
         - 여러 개의 트랙잭션을 관리
         - 업무를 처리하는 비즈니스 로직을 수행
         - 동적인 컨텐츠(asp, php, jsp)를 웹 브라우저에게 제공하는 역할
            - 웹 서버는 정적인 컨텐츠(html, css, js)를 웹 브라우저에게 제공
         - 정적인 콘텐츠를 처리할 수도 있음


### 동작 순서
1. 사용자가 웹 브라우저의 검색창에 특정 사이트의 주소를 입력한다.
2. 웹 브라우저가 DNS에게 특정 사이트의 (도메인)주소를 요청한다.
3. DNS가 웹 브라우저에게 사이트의 IP주소를 응답한다.
4. 웹 브라우저가 웹 서버에게 IP 주소를 이용하여 html 문서를 요청한다.
5. 웹 서버는 바로 웹 페이지를 공급하지 못하고, 웹 애플리케이션 서버와 데이터 베이스에서 웹 페이지 작업을 처리한다.
6. 작업 처리 결과를 웹 서버로 보낸다.
7. 웹 서버는 웹 브라우저에게 html 문서 결과를 응답한다.
8. 웹 브라우저는 화면에 웹 페이지를 출력한다.

## 4. HTTP
> https://developer.mozilla.org/ko/docs/Web/HTTP/Overview
- HTML 문서와 같은 리소스들을 가져올 수 있도록 해주는 프로토콜
   - 프로토콜은 컴퓨터 내부에서, 또는 컴퓨터 사이에서 데이터의 교환 방식을 정의하는 규칙 체계
- 웹에서 이루어지는 모든 데이터 교환의 기초이며, 클라이언트-서버 프로토콜이기도 함
- 클라이언트와 서버들은 (데이터 스트림과 대조적으로) 개별적인 메시지 교환에 의해 통신
- 클라이언트에 의해 전송되는 메시지를 요청(requests)이라고 부르며, 그에 대해 서버에서 응답으로 전송되는 메시지를 응답(responses)이라고 부름
- 오늘날 하이퍼텍스트 문서 뿐만 아니라 이미지와 비디오 혹은 HTML 폼 결과와 같은 내용을 서버로 포스트(POST/ 전달)하기 위해서도 사용

### 구성요소
- 요청은 하나의 개체, 사용자 에이전트(또는 그것을 대신하는 프록시)에 의해 전송
- 대부분의 경우, 사용자 에이전트는 브라우저지만, 무엇이든 될 수 있음
- 서버는 요청을 처리하고 response라고 불리는 응답을 제공
- 이 요청과 응답 사이에는 여러 개체들이 있는데, 예를 들면 다양한 작업을 수행하는 게이트웨이 또는 캐시 역할을 하는 프록시 등이 있음
- [Client] <--> [Proxy] <--> [Proxy] <--> [Server]
- 실제로는 브라우저와 요청을 처리하는 서버 사이에는 좀 더 많은 컴퓨터들이 존재(라우터, 모뎀 등)
- HTTP은 애플리케이션 계층의 최상위에 있음

1. 클라이언트(Client)
   - 사용자를 대신하여 동작하는 모든 도구
   - 주로 사용자가 사용하는 브라우저
   - 브라우저는 항상 요청을 보내는 개체이며, 서버가 될 수 없음
   - 웹 페이지 표시 과정
      1. 브라우저는 페이지의 HTML 문서를 가져오기 위한 요청을 전송
      2. 파일을 구문 분석하여 실행해야 할 스크립트 + 페이지 내 포함된 하위 리소스들(보통 이미지와 비디오)을 잘 표시하기 위한 레이아웃 정보(CSS) + 추가적인 요청들을 가져옴 
      3. 브라우저는 완전한 문서인 웹 페이지를 표시하기 위해 그런 리소스들을 혼합
   - 브라우저에 의해 실행된 스크립트는 이후 단계에서 좀 더 많은 리소스들을 가져올 수 있으며 브라우저는 그에 따라 웹 페이지를 갱신
   - 브라우저는 HTTP 요청 내에서 이런 지시 사항들을 변환하고 HTTP 응답을 해석하여 사용자에게 명확한 응답을 표시

2. 서버(Server)
   - 클라이언트에 의한 요청에 대한 문서를 제공해주는 개체
   - 서버는 논리적으로는 단일 기계(복잡한 프로세스를 하는 서버 역할을 하는 것들의 집합일 수도 있기 때문)
   - 반드시 단일 머신일 필요는 없으며, 여러 개의 서버를 동일한 머신 위에서 호스팅 할 수 있음

3. 프록시(Proxy)
   - 웹 브라우저와 서버 사이에서는 수많은 컴퓨터와 머신이 HTTP 메시지를 이어 받고 전달
   - 여러 계층으로 이루어진 웹 스택 구조에서 이러한 컴퓨터/머신들은 대부분은 전송, 네트워크 혹은 물리 계층에서 동작하나, HTTP 계층에서는 이들이 어떻게 동작하는지 눈에 보이지 않음
   - 이러한 컴퓨터/머신 중에서도 애플리케이션 계층에서 동작하는 것들을 일반적으로 프록시라고 함
   - 프록시를 통해 요청이 변경될 수도, 변경되지 않을 수도 있음
   - 기능
      - 캐싱  (캐시는 공개 또는 비공개가 될 수 있음 (예: 브라우저 캐시))
      - 필터링 (바이러스 백신 스캔, 유해 컨텐츠 차단(자녀 보호) 기능)
      - 로드 밸런싱 (여러 서버들이 서로 다른 요청을 처리하도록 허용)
      - 인증 (다양한 리소스에 대한 접근 제어)
      - 로깅 (이력 정보를 저장)

### 기본적인 특성
1. 간단함
   - 사람이 읽을 수 있으며 간단하게 고안
   - HTTP 메세지를 프레임별로 캡슐화하여 간결함을 유지
   
2. 확장 가능함
   - 클라이언트와 서버가 새로운 헤더의 시맨틱에 대해 간단한 합의만 한다면, 언제든지 새로운 기능을 추가할 수 있음

3. 상태가 없지만, 세션은 있음
   - 상태를 저장하지 않음(Stateless)
   - 동일한 연결 상에서 연속하여 전달된 두 개의 요청 사이에는 연결고리가 없음
   - HTTP 쿠키는 상태가 있는 세션을 만들도록 해줌.(페이지와 상호작용할 떄 사용)
   - 헤더 확장성을 사용하여, 동일한 컨텍스트 또는 동일한 상태를 공유하기 위해 각각의 요청들에 세션을 만들도록 HTTP 쿠키가 추가

4. 연결
   - 연결은 전송 계층에서 제어되므로 근본적으로 HTTP 영역 밖
   - HTTP는 연결될 수 있도록 하는 근본적인 전송 프로토콜을 요구하지 않음
   - 신뢰할 수 있거나 메시지 손실이 없는(최소한의 오류는 표시) 연결을 요구
   - 인터넷 상의 가장 일반적인 두 개의 전송 프로토콜 중에서 TCP는 신뢰할 수 있으며 UDP는 그렇지 않음
      - TCP: 연결 프로토콜의 한 종류, 양쪽이 연결 된 뒤에 데이터 전송
      - UDP: 연결 프로토콜의 한 종류, 연결되지 않더라도 우선 데이터 전송

   - HTTP는 연결이 필수는 아니지만 연결 기반인 TCP 표준에 의존
   - 클라이언트와 서버가 HTTP를 요청/응답으로 교환하기 전에 여러 왕복이 필요한 프로세스인 TCP 연결을 설정해야 함
   - HTTP/1.0의 기본 동작은 각 요청/응답에 대해 별도의 TCP 연결을 여는 것이나, 여러 요청을 연속해서 보내는 경우 단일 TCP 연결을 공유하는 것이 더 효율적
   - HTTP에 더 알맞은 좀 더 나은 전송 프로토콜을 설계하는 실험이 진행 중(구글은 UDP 기반의 QUIC를 실험중)

### HTTP 흐름
1. TCP 연결을 열어줌(새 연결을 열거나, 기존 연결을 재사용하거나, 서버에 대한 여러 TCP 연결을 열 수 있음)
2. HTTP 메시지를 전송
3. 서버에 의해 전송된 응답을 읽음
4. 연결을 닫거나 다른 요청들을 위해 재사용

### HTTP 메세지
- HTTP 메시지의 두 가지 타입인 요청(requests)과 응답(responses)은 각자의 특성있는 형식을 가지고 있음
1. 요청
   1. HTTP 메서드
      - 보통 클라이언트가 수행하고자 하는 동작을 정의한 GET, POST 같은 동사나 OPTIONS나 HEAD와 같은 명사
      - 대표적인 메서드
         - GET: 데이터를 받아올 때 사용
         - POST: 특정 리소스를 제출할 때 사용(파일 업로드 등)
         - PATCH: 수정할 때 사용
         - DELETE: 삭제할 때 사용
   2. 리소스의 경로
      - 리소스의 URL
   
   3. HTTP 프로토콜의 버전

   4. 서버에 대한 추가 정보를 전달하는 헤더들

   5. POST와 같은 몇 가지 메서드를 위한, 전송된 리소스를 포함하는 응답의 본문과 유사한 본문

2. 응답
   1. HTTP 프로토콜의 버전
   2. 요청의 성공 여부와, 그 이유를 나타내는 상태 코드
   3. 아무런 영향력이 없는, 상태 코드의 짧은 설명을 나타내는 상태 메시지
   4. 요청 헤더와 비슷한, HTTP 헤더들
   5. 리소스가 포함되는 본문(필수는 아님)

### HTTP 파라미터 전송
```javascript
const login = (email, password) => {
   ... //로그인 로직
}
```
1. GET
  ```
  [GET]
  www.test.com/login?email=user01@test.com&password=123456
  ```
  - http 메소드 뒤에 '?'를 붙여 파라미터를 전달
  - 파라미터 이름, 값을 URL 뒤에 작성
  - 필요한 파라미터가 2개 이상일 경우, '&'를 이용해 구별
  - 데이터 길이에 제한이 있음
  - 단순 조회에 주로 사용

2. POST
  ```javascript
   const userInfo = {
      email: "user01@test.com",
      password: "123456"
   }

  const loginResult = fetch("www.test.com/login", {
     method: "POST",
     body: JSON.stringify(data),
  })
  ```
  - URL에 직접적으로 표기하지 않고 body에 데이터가 담김 
  - 사용자에게 데이터가 노출되지 않아 보안에 강함
  - GET을 제외한 요청(PUT, DELETE...)은 이런 방식으로 데이터 전달
  


## 5. Hosting
- 대형 서버의 기능을 빌려쓰는 것
- PC 서버로 웹사이트를 제공하기 위해서는 24시간동안 컴퓨터를 켜놔야 하는데, 개인 컴퓨터에서는 현실적으로 힘드므로 호스팅 업체가 여러대의 서버 중 일부 공간을 나누어 준 뒤 그 대가를 받는 서비스

### 종류
1. 웹 호스팅
   - 여러 대의 웹사이트를 한 서버에 운영하는 방식
   - 트래픽양이 증가해서 혼자 너무 많은 트래픽을 발생시킨다면 서버가 다운 될 수 있음

2. 서버 호스팅
   - 서버 컴퓨터의 부분, 혹은 전체를 임대하는 서비스

## 6. 기타 사이트
> https://d2.naver.com/helloworld/59361

## 7. REST API
1. 개념
  - REST란, REpresentational State Transfer 의 약자
    - 자원을 이름(자원의 표현)으로 구분하여 해당 자원의 상태(정보)를 주고 받는 모든 것을 의미

  - API(Application Programming Interface)란
    - 데이터와 기능의 집합을 제공하여 컴퓨터 프로그램간 상호작용을 촉진하며, 서로 정보를 교환가능 하도록 하는 것

  - 월드와이드웹과 같은 분산 하이퍼 미디어 시스템에서 운영되는 소프트웨어 아키텍처 스타일
    - 하이퍼 미디어?
      - 텍스트·음성·도형·애니메이션 및 비디오 화상 등 복수의 정보를 노드(node)와 링크(link)로 유기적으로 연결한 네트워크(그물망)구조

  - REST API란 REST 기반으로 API를 구현한 것

2. 특징
  - Uniform (유니폼 인터페이스)
    - Uniform Interface는 URI로 지정한 리소스에 대한 조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일.

  - Stateless (무상태성)
    - REST는 무상태성 성격을 가짐, 
    - 다시 말해 작업을 위한 상태정보를 따로 저장하고 관리하지 않음. 
    - 세션 정보나 쿠키정보를 별도로 저장하고 관리하지 않기 때문에 API 서버는 들어오는 요청만을 단순히 처리하면 됨. 
    - 때문에 서비스의 자유도가 높아지고 서버에서 불필요한 정보를 관리하지 않음으로써 구현이 단순해짐.

  - Cacheable (캐시 가능)
    - REST의 가장 큰 특징 중 하나는 HTTP라는 기존 웹표준을 그대로 사용하기 때문에, 웹에서 사용하는 기존 인프라를 그대로 활용이 가능. 
    - HTTP가 가진 캐싱 기능이 적용 가능 
    - HTTP 프로토콜 표준에서 사용하는 Last-Modified 태그나 E-Tag를 이용하면 캐싱 구현이 가능합니다.

  - Self-descriptiveness (자체 표현 구조)
    - REST의 또 다른 큰 특징 중 하나는 REST API 메시지만 보고도 이를 쉽게 이해 할 수 있는 자체 표현 구조로 되어 있음.

  - Client - Server 구조
    - REST 서버는 API 제공, 클라이언트는 사용자 인증이나 컨텍스트(세션, 로그인 정보)등을 직접 관리하는 구조
    - 각각의 역할이 확실히 구분되기 때문에 클라이언트와 서버에서 개발해야 할 내용이 명확해지고 서로간 의존성이 줄어들게 됨.

  - 계층형 구조
    - REST 서버는 다중 계층으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있음
    - PROXY, 게이트웨이 같은 네트워크 기반의 중간매체를 사용할 수 있게 합니다.

3. 구성
  - 자원(Resource) - URL
    - 모든 자원에 고유한 ID가 존재하고, 이 자원은 Server에 존재한다.
    - 자원을 구별하는 ID는 /orders/order_id/1 와 같은 HTTP URI 이다.

  - 행위(Verb) - Http Method
    - HTTP 프로토콜의 Method를 사용한다.
    - HTTP 프로토콜은 GET, POST, PUT, DELETE와 같은 메서드를 제공한다.

  - 표현(Representations)
    - Client가 자원의 상태 (정보)에 대한 조작을 요청하면 Server는 이에 적절한 응답 (Representation)을 보낸다
    - REST에서 하나의 자원은 JSON, XML, TEXT, RSS 등 여러 형태의 Representation으로 나타낼 수 있다.
    - 현재는 JSON으로 주고 받는 것이 대부분이다.
      - JSON?
        - JavaScript Object Notation
        - 자바스크립트 객체 표기


4. 설계 규칙
  - URI는 정보의 자원을 표현해야 함
    - resource는 동사보다는 명사를, 대문자보다는 소문자를 사용한다.
    - resource의 도큐먼트 이름으로는 단수 명사를 사용해야 한다.
    - resource의 컬렉션 이름으로는 복수 명사를 사용해야 한다.
    - resource의 스토어 이름으로는 복수 명사를 사용해야 한다.
      - Ex) GET /Member/1 -> GET /members/1

  - 자원에 대한 행위는 HTTP Method(GET, POST, PUT, DELETE 등)으로 표현
    - URI에 HTTP Method가 들어가면 안됨
      - Ex) GET /members/delete/1 -> DELETE /members/1
    - URI에 행위에 대한 동사 표현이 들어가면 안된다.(즉, CRUD 기능을 나타내는 것은 URI에 사용하지 않는다.)
      - Ex) GET /members/show/1 -> GET /members/1
      - Ex) GET /members/insert/2 -> POST /members/2
    - 경로 부분 중 변하는 부분은 유일한 값으로 대체한다.(즉, :id는 하나의 특정 resource를 나타내는 고유값이다.)
      - Ex) student를 생성하는 route: POST /students
      - Ex) id=12인 student를 삭제하는 route: DELETE /students/12

  - 슬래시 구분자(/ )는 계층 관계를 나타내는데 사용한다.
      - Ex) http://restapi.example.com/houses/apartments
  - URI 마지막 문자로 슬래시(/ )를 포함하지 않는다.
  - URI에 포함되는 모든 글자는 리소스의 유일한 식별자로 사용되어야 하며 URI가 다르다는 것은 리소스가 다르다는 것이고, 역으로 리소스가 다르면 URI도 달라져야 한다.
  - REST API는 분명한 URI를 만들어 통신을 해야 하기 때문에 혼동을 주지 않도록 URI 경로의 마지막에는 슬래시(/)를 사용하지 않는다.
      - Ex) http://restapi.example.com/houses/apartments/ (X)
  - 하이픈(- )은 URI 가독성을 높이는데 사용
  - 불가피하게 긴 URI경로를 사용하게 된다면 하이픈을 사용해 가독성을 높인다.
  - 밑줄(_ )은 URI에 사용하지 않는다.
  - 밑줄은 보기 어렵거나 밑줄 때문에 문자가 가려지기도 하므로 가독성을 위해 밑줄은 사용하지 않는다.
  - URI 경로에는 소문자가 적합하다.
  - URI 경로에 대문자 사용은 피하도록 한다.
  - RFC 3986(URI 문법 형식)은 URI 스키마와 호스트를 제외하고는 대소문자를 구별하도록 규정하기 때문
  - 파일확장자는 URI에 포함하지 않는다.
  - REST API에서는 메시지 바디 내용의 포맷을 나타내기 위한 파일 확장자를 URI 안에 포함시키지 않는다.
  - Accept header를 사용한다.
      - Ex) http://restapi.example.com/members/soccer/345/photo.jpg (X)
      - Ex) GET / members/soccer/345/photo HTTP/1.1 Host: restapi.example.com Accept: image/jpg (O)
  - 리소스 간에는 연관 관계가 있는 경우
  - /리소스명/리소스 ID/관계가 있는 다른 리소스명
      - Ex) GET : /users/{userid}/devices (일반적으로 소유 ‘has’의 관계를 표현할 때)

5. 실습!
  ### 네이버 영화 오픈 API와 HTML table을 사용하여 영화 정보 페이지 만들어보기!
  - 네이버 영화 OPEN API
     > https://developers.naver.com/docs/search/movie/

  - fetch()로 API 호출

  1. HTML table의 구조
     1. 제목
     2. 이미지
     3. 평점

   