# Internet-Of-Things
23-1 Prof.Song

각 예제들에 대한 요점입니다.

예제 1-1 : 기본적인 변수 선언식, 가변 데이터 생성. 가변 데이터의 식별자 = a

예제 1-2 : 변수 선언과 더불어 데이터를 할당하는 과정, 변수영역과 데이터영역을 분리하면 중복 데이터에 대한 처리 효율 상승

예제 1-3 : 불변성; 문자열 값과 숫자 값 모두 한 번 만들었다면 다른 값으로 바꿀 수 없고, 새로 만드는 동작을 통해서만 이루어짐.

예제 1-4 : 참조한 데이터를 할당하는 과정; 가변형 데이터와는 달리 객체의 변수 영역이 별도로 존재 & 데이터 영역에 저장된 값은 모두 불변값

예제 1-5 : 참조형 데이터의 프로퍼티를 재할당하는 과정; 새로운 객체가 만들어진 것이 아니라 기존의 객체 내부의 값만 바뀐 것 = 중첩객체

예제 1-6 : 중첩된 참조형 데이터객체의 프로퍼티 할당; 재할당 명령을 내리게 될 시 참조 카운트가 0이 되어 가비지컬렉터의 수거 대상이 됨

예제 1-7 : 변수 복사; 기본형 데이터와 참조형 데이터의 차이 - 복사과정은 동일하지만 데이터 할당 과정에서 차이 발생

예제 1-8 : 변수 복사 이후 값 변경 결과 비교(1) - 객체의 프로퍼티 변경 시; 자바스크립트의 모든 데이터 타입은 참조형 데이터일 수밖에 없음.

예제 1-9 : 변수 복사 이후 값 변경 결과 비교(2) - 자체를 변경했을 때; 객체에 대한 변경임에도 불구하고 값이 달라짐.

예제 1-10 : 객체의 가변성에 따른 문제점 - 정보가 바뀐 시점, 바뀌기 전&후의 정보차이를 보여줘야하는 기능 구현은 불가능

예제 1-11 : 객체의 가변성에 따른 문제점의 해결 방법 - changeName 함수로 새로운 객체를 반환하도록 수정; 서로 다른 객체라 변경 전&후 비교 가능

예제 1-12 : 기존 정보를 복사해서 새로운 객체를 반환하는 함수(얕은 복사); 체이닝 모든 프로퍼티 복사, getter/setter 복사 X는 등의 아쉬운 점 존재

예제 1-13 : copyObject를 이용한 객체 복사 - 협업 개발자끼리 앞선 함수 사용을 한다는 전제하에 user 객체 = 불변 객체

예제 1-14 : 중첩된 객체 대한 얕은 복사 : user 객체에 직접 속하지 않은 내부 프로퍼티에 대해서는 기존 데이터를 그대로 참조하는 현상 발생

예제 1-15 : 중첩된 객체에 대한 깊은 복사 : 객체의 프로퍼티 값이 참조형 데이터인 경우 다시 그 내부의 프로퍼티들을 복사해야함.

예제 1-16 : 객체의 깊은 복사를 수행하는 범용 함수 : copyObjectDeep 함수를 사용하여 객체 복사 후 원본과 사본 어느 프로퍼티를 변경하더라도 다른쪽에는 영향을 주지 않게끔 만듬.

예제 1-17 : 깊은 복사 결과 확인 : hasOwnProperty 방법을 활용하여 프로타입 체이닝을 통해 상속된 프로퍼티를 복사하지 않게끔 가능

예제 1-18 : JSON을 활용한 간단한 깊은 복사 : 객체를 JSON 문법으로 표현된 문자열로 전환했다가 다시 JSON 객체로 바꾸는 방법

예제 1-19 : 자동으로 undefined를 부여하는 경우 : 값을 대입하지 않는 경우 특이한 동작이 발생

예제 1-20 : undefined와 배열 : 각 3개의 빈 요소에는 문자 그대로 어떤 값도 할당돼 있지 않음을 의미

예제 1-21 : 반 요소와 배열의 순회 : 존재하지 안흔 프로퍼티에 대해 순회 불가능한 것은 당연. 배열은 length 프로퍼티의 개수만큼 빈 공간을 확보하고 각 공간에 인덱스를 이름으로 지정할 것이라 생각하기 쉽지만, 실제로는 객체와 마찬가지로 특정 인덱스에 값을 지정할 때 비로소 빈 공간을 확보하고 인덱스를 이름으로 지정하고 데이터의 주솟값을 저장하는 등의 동작을 수행

예제 1-22 : undefined와 null 비교 : 어떤 변수가 실제 null인지 undefined인지 동등 연산자로는 비교 불가능, 일치 연산자(===)를 사용해야함



예제 2-1 : 실행 컨텍스트와 콜 스택 : 콜스택에 실행 컨텍스트가 어떤 순서로 쌓이고, 어떤 순서로 코드 실행에 관여하는지 확인하는 과정

예제 2-2 : 매개변수와 변수에 대한 호이스팅(1) - 원본코드; 인자를 함수 내부의 다른 코드보다 먼저 선언 및 할당이 이뤄진 것으로 간주 가능

예제 2-3 : 매개변수와 변수에 대한 호이스팅(2) - 매개변수를 변수 선언/할당과 같다고 간주해서 변환한 상황, Environment Record는 현재 실행될 컨텍스트의 대상 코드 내에 어떤 식별자들이 있는지에만 관심이 있고, 각 식별자에 어떤 값이 할당될 것인지는 관심이 없으므로, 변수를 호이스팅할 때 변수명망 끌어올리고 할당 과정은 원래 자리에 그대로 남겨 둠.

예제 2-4 : 매개변수와 변수에 대한 호이스팅(3) - 호이스팅을 마친 상태; 처음에 예상한 값들은 (1)=1, (2)=undefined, (3)=2로 예상했으나 (2)=1이 출력이 되었음. 이는 호이스팅 개념을 정확히 이해하지 못하면 예측하기 어려운 결과임.

예제 2-5 : 함수 선언의 호이스팅(1) - 원본코드; a함수를 실행하는 순간 a 함수의 실행 컨텍스트가 생성 됨. 변수명과 함수 선언의 정보를 위로 끌어올림

예제 2-6 : 함수 선언의 호이스팅(2) - 호이스팅을 마친 상태; 호이스팅이 끝난 상태에서의 함수 선언문은 함수명으로 선언한 변수에 함수를 할당한 것처럼 여길 수 있음.

예제 2-7 : 함수 선언의 호이스팅(3) - 함수 선언문을 함수 표현식으로 바꾼 코드; 호이스팅 고려전에는 에러 또는 undefined, 'bbb', b 함수가 나오리라 생각했지만 실제로는 (1)=b 함수, (2) = 'bbb', (3) = 'bbb'가 나옴.

예제 2-8 : 함수를 정의하는 세 가지 방식; 함수 선언문은 function 정의부만 존재하고 별도의 할당 명령이 없는 것을 의미, 함수 표현식은 정의한 function을 별도의 변수에 할당하는 것을 말함.

예제 2-9 : 함수 선언문과 함수 표현식(1) - 원본 코드; 실행 컨텍스트의 LexicalEnvironment는 두 가지 정보를 수집하는데, 그 중 environmentRecord의 정보 수집 과정에서 발생하는 호이스팅을 살펴보는 과정

예제 2-10 : 함수 선언문과 함수 표현식(2) - 호이스팅을 마친 상태; 함수 선언문은 전체를 호이스팅한 반면 함수 표현식은 변수 선언부만 호이스팅, 함수도 하나의 값으로 취급할 수 있음의 예

예제 2-11 : 함수 선언문의 위험; 코드 실행 중 실제 호출 함수는 마지막에 할당된 함수 뿐임, 문제의 원인이 되는 sum 함수는 아무런 에러를 내지 않아서 어떤 함수가 문제인지 파악하기 어려움

예제 2-12 : 상대적으로 함수 표현식이 안전하다.; 원활한 협업을 위해서는 전역공간에 함수를 선언하거나 동명의 함수를 중복 선언하지 말아야함.

예제 2-13 : 스코프 체인; inner 함수 내부에서 a 변수를 선언했기 때문에 전역 공간에서 선언한 동일한 이름의 a 변수에는 접근할 수 없음 = 변수 은닉

예제 2-14 : 스코프 체인 확인(1) - 크롬 용용; 크롬 브라우저 환경에서는 스코프 체인 중 현재 실행 컨텍스트르 제외한 상위 스코프 정보들을 개발자 도구의 콘솔을 통해 확인 가능 = 확인 방법은 함수 내부에서 함수를 출력 하면 됨.

예제 2-15 : 스코프 체인 확인(2) - 크롬 전용; 디버거 = console.dir 부분을 debugger로 바꾸어 를 활용하면 더 자세한 정보 확인 가능함

예제 2-16 : 스코프 체인 확인(3) ; 전역 공간에서 선언한 변수는 전역번수이고, 함수 내부에서 선언한 변수는 지역변수





예제 3-1 : 전역 공간에서의 this(브라우저 환경); 전역 공간에서 this는 전역 객체를 가리킴. 전역 컨텍스트를 생성하는 주체 = 전역 객체

예제 3-2 : 전역 공간에서의 this(Node.js 환경); 브라우저 환경에서 전역객체는 window, Node.js 환경에서는 global

예제 3-3 : 전역변수와 전역객체(1); 전역공간에서의 this는 전역객체를 의미하므로 두 값이 같은 값을 출력하는 것이 당연. 자바스크립트의 모든 변수는 특정 객체의 프로퍼티로서 동작하기 때

예제 3-4 : 전역변수와 전역객체(2); 전역변수 선언과 전역객체의 프로퍼티 할당 사이에 전혀 다른 경우 = 삭제 명

예제 3-5 : 전역변수와 전역객체(3); var로 선언한 전역변수와 전역객체의 프로퍼티는 호이스팅 여부 및 configurable 여부에서임차이를 보임

예제 3-6 : 함수로서 호출, 메서드로서 호출

예제 3-7 : 메서드로서 호출 - 점 표기법, 대괄호 표기

예제 3-8 : 메서드 내부에서의 this

예제 3-9 : 내부함수에서의 this

예제 3-10 : 내부함수에서의 this를 우회하는 방법

예제 3-11 : this를 바인딩하지 않는 함수(화살표 함수)

예제 3-12 : 콜백 함수 내부에서의 this

예제 3-13 : 생성자 함수

예제 3-14 : call 메서드(1)

예제 3-15 : call 메서드(2)

예제 3-16 : apply 메서드

예제 3-17 : call/apply 메서드의 활용 1-1)유사배열객체에 배열 메서드를 적용

예제 3-18 : call/apply 메서드의 활용 1-2)arguments, NodeList에 배열 메서드를 적용

예제 3-19 : call/apply 메서드의 활용 1-3)문자열에 배열 메서드 적용 예시

예제 3-20 : call/apply 메서드의 활용 1-4) ES6의 Array.from 메서드

예제 3-21 : call/apply 메서드의 활용 2) 생성자 내부에서 다른 생성자를 호출

예제 3-22 : call/apply 메서드의 활용 3-1) 최대/최솟값을 구하는 코드를 직접 구현

예제 3-23 : call/apply 메서드의 활용 3-2) 여러 인수를 받는 메서드(Math.max/Math.min)에 apply를 적용

예제 3-24 : call/apply 메서드의 활용 3-3) ES6의 펼치기 연산자 활용

예제 3-25 : bind 메서드 - this 지정과 부분 적용 함수 구현

예제 3-26 : bind 메서드 - name 프로퍼티

예제 3-27 : 내부함수에 this 전달 - call vs. bind

예제 3-28 : bind 메서드 - 내부함수에 this 전달

예제 3-29 : 화살표 함수 내부에서의 this

예제 3-30 : thisArg를 받는 경우 예시 - forEach 메서드

예제 3-31 : 콜백 함수와 함께 thisArg를 인자로 받는 메서드
