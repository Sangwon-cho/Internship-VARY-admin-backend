## Sprint1 : TypeScript & PostgreSQL

### 👉 TypeScript

- TypeScript는 2012년에 발표된 오픈 소스 프로그래밍 언어로, 대규모 JavaScript 애플리케이션 개발을 목적으로 Microsoft에 의해 개발
- TypeScript는 웹브라우저에서 바로 해석될 수 없고 JavaScript로 변환되어야 웹 브라우저가 해석할 수 있다 → TS를 transpiler라고 부르고 이러한 언어를 Meta Language라고 부른다
- 장점
  - `정적 타입을 지원` → 컴파일 단계에서 오류를 포착할 수 있다 → 코드의 가독성을 높이고 디버깅을 용이하게 한다.
  - `ES6 / ES NEXT 지원` - 호환성을 위해 babel을 사용할 필요없고 ES6/ES NEXT문법을 사용해도 tsconfig.js에 지정된 자바스크립트 버전으로 자동으로 변환해주기 때문에 최신 JS기능들을 호환 걱정없이 사용할 수 있다.
  - `객체지향 프로그래밍 지원` - ES NEXT부터 class,interface, abstract class등 객체지향언어의 문법들이 추가 되었다.
  - `강력한 생태계` - 대부분의 라이브러리들이 ts를 지원하며 각종 에디터가 다양한 플러그인을 지원한다
- 단점

  - `상대적으로 낮은 가독성과 코드 작성에 많은 시간 소요` - 하나하나 타입을 모두 설정해주어야하므로 시간이 오래걸리고 코드가 길어지면서 가독성도 떨어지게된다.
  - `컴파일 언어` - TS는 JS로 컴파일 되는 언어이므로 브라우저나 대중적으로 사용되는 런타임에서는 바로 사용할 수 없다
  - `복잡한 초기 설정` - tsconfig.json 파일을 통해 여러가지 설정을 해야한다.

    </br>

  <span style="font-weight:bold">Why TypeScript?</span>

  VARY는 다른 서비스들에 비해 특히 클라이언트 각각의 input에 따른 output을 나타내기에 그만큼 error를 발생시킬 경우의 수도 많다. 하지만 타입스크립트를 사용함으로 컴파일 과정에서 에러를 확인할 수 있게되어 개발단계에서 인지하지 못한 실수나 예상밖에 상황으로부터 오는 에러들 또한 미연에 방지할 수 있게 된다. 따라서 VARY는 사용자가 겪는 불편을 줄이고 프로그램의 높은 안정성을 가져올 수 있을 것이다.

### <span style="font-weight:bold">👉 PostgreSQL</span>

- `오픈소스로 무료로 사용 가능` → 비용 절감
- `ORDMBS(개체 관계형 데이터베이스)` → 개체 및 테이블 상속을 등을 정의할 수 있음
- `빠르고 유연한 개발` → 강력한 오픈소스 커뮤니티로 인해 발전 속도가 빠르다
- `다양한 데이터 유형을 지원한다` → 숫자, 문자열, 날짜와 시간 타입 이외에 기하학적인 도형, 네트워크 주소, JSON 항목등
- 복잡한 대량의 데이터 작업을 수행하는데 적합, 단순히 읽기 전용 작업이 아닌 복잡한 읽기-쓰기 작업을 수행하는데 적합, OLTP / OLAP에 적합

  - **OLTP (Online Transaction Processing)**
    - 네트워크 상의 온라인 사용자들의 Database에 대한 일괄 트랜잭션 처리를 의미
    - Transaction 의 과정에서 INSERT/UPDATE 를 중점적으로 수행
  - **OLAP (Online Analytical Processing)**

    - 시스템과 연관되어 Data 를 분석하고 의미있는 정보로 치환하거나, 복잡한 모델링을 가능하게끔 하는 분석 방법
    - SELECT Query 를 통한 데이터 스캔 Operation)

  <span style="font-weight:bold">Why PostgreSQL?</span>

  VARY에서는 이메일과 웹페이지를 만들어주는 mobile builder의 역할 뿐만 아니라 그 데이터들을 분석하여 각각의 서비스들에 대한 통계 또한 제공해야한다. 또한 VARY의 서비스는 Online Transaction Processing(OLTP)이 매우 중요하기에 PostgreSQL을 사용함으로 그 이점을 사용할 수 있을 것이다.(무엇보다도 오픈소스이기에 무료로 사용가능하다는 점이 아주 매력적!)

### _용어정리_

`정적타입언어`( TypeScript, Java, C++)

- 자바스크립트(동적타입언어)의 모든 기능을 포함하면서 정적타입을 지원
- 정적 타입 언어(JS,Python,PHP)는 변수의 타입이 컴파일 타임에 결정된다!(동적 타입 언어는 런타임에 결정된다)
