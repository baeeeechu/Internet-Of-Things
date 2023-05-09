# Internet-Of-Things
23-1 Prof.Song

각 예제들에 대한 요점입니다.

예제 1-1 : 기본적인 변수 선언식, 가변 데이터 생성. 가변 데이터의 식별자 = a

예제 1-2 : 변수 선언과 더불어 데이터를 할당하는 과정, 변수영역과 데이터영역을 분리하면 중복 데이터에 대한 처리 효율 상승

예제 1-3 : 불변성; 문자열 값과 숫자 값 모두 한 번 만들었다면 다른 값으로 바꿀 수 없고, 새로 만드는 동작을 통해서만 이루어짐.

예제 1-4 : 참조형 데이터를 할당하는 과정; 가변형 데이터와는 달리 객체의 변수 영역이 별도로 존재 & 데이터 영역에 저장된 값은 모두 불변값

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

예제 1-21 : 반 요소와 배열의 순회 : 존재하지 않는 프로퍼티에 대해 순회 불가능한 것은 당연. 배열은 length 프로퍼티의 개수만큼 빈 공간을 확보하고 각 공간에 인덱스를 이름으로 지정할 것이라 생각하기 쉽지만, 실제로는 객체와 마찬가지로 특정 인덱스에 값을 지정할 때 비로소 빈 공간을 확보하고 인덱스를 이름으로 지정하고 데이터의 주솟값을 저장하는 등의 동작을 수행

예제 1-22 : undefined와 null 비교 : 어떤 변수가 실제 null인지 undefined인지 동등 연산자로는 비교 불가능, 일치 연산자(===)를 사용해야함



예제 2-1 : 실행 컨텍스트와 콜 스택 : 콜스택에 실행 컨텍스트가 어떤 순서로 쌓이고, 어떤 순서로 코드 실행에 관여하는지 확인하는 과정

예제 2-2 : 매개변수와 변수에 대한 호이스팅(1) - 원본코드; 인자를 함수 내부의 다른 코드보다 먼저 선언 및 할당이 이뤄진 것으로 간주 가능

예제 2-3 : 매개변수와 변수에 대한 호이스팅(2) - 매개변수를 변수 선언/할당과 같다고 간주해서 변환한 상황, Environment Record는 현재 실행될 컨텍스트의 대상 코드 내에 어떤 식별자들이 있는지에만 관심이 있고, 각 식별자에 어떤 값이 할당될 것인지는 관심이 없으므로, 변수를 호이스팅할 때 변수명만 끌어올리고 할당 과정은 원래 자리에 그대로 남겨 둠.

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

예제 3-5 : 전역변수와 전역객체(3); var로 선언한 전역변수와 전역객체의 프로퍼티는 호이스팅 여부 및 configurable 여부에서 차이를 보임

예제 3-6 : 함수로서 호출, 메서드로서 호출; 함수 앞에 점(.)이 있는지 여부로 구분 가능

예제 3-7 : 메서드로서 호출 - 점 표기법, 대괄호 표기; 점 표기법이든 대괄호 표기법이든, 어떤 함수를 호출할 때 그 함수 이름 앞에 객체가 명시돼 있는 경우에는 메서드로 호출한 것이고, 그렇지 않은 모든 경우에는 함수로 호출한 것.

예제 3-8 : 메서드 내부에서의 this; 일반적으로 혼란을 느끼기 쉬움 주의!, 어떤 함수로 호출했는지 파악하면 정확히 파악 가

예제 3-9 : 내부함수에서의 this; 어떤 함수를 함수로서 호출할 경우에는 this가 지정되지 않음.

예제 3-10 : 내부함수에서의 this를 우회하는 방법; 사람마다 각기 다른 변수명을 사용하지만 self가 가장 많이 사용되는 편

예제 3-11 : this를 바인딩하지 않는 함수(화살표 함수); call, apply 등의 메서드를 활용해 함수를 호출할 때 명시적으로 this를 지정하는 방법 有

예제 3-12 : 콜백 함수 내부에서의 this; 콜백 함수에서의 this는 특별하게 지정되지 않음. 특별히 정의되지 않은 경우에는 전역객체를 지칭한다고 보면 됨

예제 3-13 : 생성자 함수; 상황별로 this에 어떤 값이 바인딩되는지 추정

예제 3-14 : call 메서드(1); 객체의 메서드를 그냥 호출하면 this는 객체를 참조하지만 call 메서드를 이용하면 임의의 객체를 this로 지정 가

예제 3-15 : call 메서드(2); apply 메서드는 call 메서드와 기능적으로 완전 동일

예제 3-16 : apply 메서드; call & apply 메서드를 잘 활용하면 자바스크립트를 더욱 다채롭게 사용 가능

예제 3-17 : call/apply 메서드의 활용 1-1)유사배열객체에 배열 메서드를 적용; 객체에는 배열 메서드를 직접 적용할 수 없지만, 키가 0 또는 양의 정수인 프로퍼티가 존재하고 length 프로퍼티의 값이 0 또는 양의 정수인 객체 = 배열의 구조와 유사한 객체의 경우 call 또는 apply 메서드를 이용하여 배열 메소드를 차용할 수 있음.

예제 3-18 : call/apply 메서드의 활용 1-2)arguments, NodeList에 배열 메서드를 적용; 유사배열객체에는 call/apply 메서드를 이용하여 모든 배열 메서드를 적용할 수 있음. 배열처럼 length 프로퍼티를 지니는 문자열에 대해서도 마찬가지임. 

예제 3-19 : call/apply 메서드의 활용 1-3)문자열에 배열 메서드 적용 예시; ES6에서는 유사배열객체 또는 순회 가능한 모든 종류의 데이터 타입을 배열로 전환하는 Array.from 메서드를 새로 도입

예제 3-20 : call/apply 메서드의 활용 1-4) ES6의 Array.from 메서드; 생성자 내부에 다른 생성자와 공통된 내용이 있을 경우 call 또는 apply를 이용해 다른 생성자를 호출하면 간단하게 반복을 줄일 수 있음.

예제 3-21 : call/apply 메서드의 활용 2) 생성자 내부에서 다른 생성자를 호출; 여러 개의 인수를 받는 메서드에게 하나의 배열로 인수들을 전달하고 싶을 때 apply 메서드를 사용하면 좋음.

예제 3-22 : call/apply 메서드의 활용 3-1) 최대/최솟값을 구하는 코드를 직접 구현; 생성자 내부에 다른 생성자와 공통된 내용이 있을 경우 call 또는 apply를 이용해 다른 생성자를 호출하면 간단하게 반복을 줄일 수 있음.

예제 3-23 : call/apply 메서드의 활용 3-2) 여러 인수를 받는 메서드(Math.max/Math.min)에 apply를 적용; Math.max/Math.min 메서드에 apply를 적용하면 훨씬 간단해짐.

예제 3-24 : call/apply 메서드의 활용 3-3) ES6의 펼치기 연산자 활용; call/apply 메서드는 명시적으로 별도의 this를 바인딩하면서 함수 또는 메서드를 실행하는 훌륭한 방법이지만 오히려 이로 인해 this를 예측하기 어렵게 만들어 코드 해석을 방해한다는 단점이 있음. 그럼에도 불구하고 ES5 이하의 환경에서는 마땅한 대안이 없기 때문에 실무에서 매우 광범위하게 활용되고 있음.

예제 3-25 : bind 메서드 - this 지정과 부분 적용 함수 구현; call과 비슷하지만 즉시 호출하지 않고 넘겨 받은 this 및 인수들을 바탕으로 새로운 함수를 반환하기만 하는 메서드임. bind 메서드는 함수에 this를 미리 적용하는 것과 부분 적용 함수를 구현하는 두 가지 목적을 모두 지님.

예제 3-26 : bind 메서드 - name 프로퍼티; 원본 함수에 bind 메서드를 적용한 새로운 함수가 되므로 기존의 call/apply 보다 코드를 추적하기 수월

예제 3-27 : 내부함수에 this 전달 - call vs. bind; 메서드의 this를 그대로 바라보게 하기 위한 방법으로 call, apply, bind 메서드를 이용하면 더 깔끔하게 상위 컨텍스트의 this를 내부함수나 콜백 함수에 전달 가능함.

예제 3-28 : bind 메서드 - 내부함수에 this 전달; 콜백 함수를 인자로 받는 함수나 메서드 중에서 기본적으로 콜백 함수 내에서의 this에 관여하는 함수 또는 메서드에 대해서도 bind 메서드를 이용하면 this 값을 사용자의 입맛에 맞게 바꿀 수 있음.

예제 3-29 : 화살표 함수 내부에서의 this; ES6에 새롭게 도입된 화살표 함수는 실행 컨텍스트 생성 시 this를 바인딩하는 과정이 제외됨. 즉 이 함수 내부에는 this가 아예 없으며, 접근하고자 하면 스코프체인상 가장 가까운 this에 접근하게 됨.

예제 3-30 : thisArg를 받는 경우 예시 - forEach 메서드; 여러 내부 요소에 대해 같은 동작을 반복 수행해야하는 배열 메서드의 예시

예제 3-31 : 콜백 함수와 함께 thisArg를 인자로 받는 메서드; thisArg를 인자를 받는 메서드도 꽤 많이 존재함.



예제 4-1 : 콜백 함수 예제(1-1) setInterval; setInterval를 실행하면 반복적으로 실행되는 내용 자체를 특정할 수 있는 고유한 ID 값이 반환 됨.

예제 4-2 : 콜백 함수 예제(1-2) setInterval; 콜백 함수의 제어권을 넘겨받은 코드는 콜백 함수 호출 시점에 대한 제어권을 가짐.

예제 4-3 : 콜백 함수 예제(2-1) Array.prototype.map; map 메서드는 첫 번째 인자로 callback 함수를 받고, 생략 가능한 두 번째 인자로 콜백 함수 내부에서 this로 인식할 대상을 특정할 수 있습니다. thisArg를 생략할 경우에는 일반적인 함수와 마찬가지로 전역객체가 바인딩 됨. map 메서드는 메서드의 대상이 되는 배열의 모든 요소들을 처음부터 끝까지 하나씩 꺼내어 콜백 함수를 반복호출하고, 콜백 함수의 실행 결과들을 모아 새로운 배열을 만듬.

예제 4-4 : 콜백 함수 예제(2-2) Array.prototype.map - 인자의 순서를 임의로 바꾸어 사용한 경우; 콜백 함수의 제어권을 넘겨받은 코드는 콜백 함수를 호출할 때 인자에 어떤 값들을 어떤 순서로 넘길 것인지에 대한 제어권을 가짐.

예제 4-5 : 콜백 함수 예제(2-3) Array.prototype.map - 구현; 별도의 this를 지정하는 방식 및 제어권에 대한 이해를 높이기 위해 map 메서드를 직접 구현한 예제 

예제 4-6 : 콜백 함수 내부에서의 this; 제어권을 넘겨받을 코드에서 call/apply 메서드의 첫 번째 인자에 콜백 함수 내부에서의 this가 될 대상을 명시적으로 바인딩하기 때문에 this에 다른 값이 담기는 것

예제 4-7 : 메서드를 콜백 함수로 전달한 경우; 콜백 함수로 어떤 객체의 메서드를 전달하더라도 그 메서드는 메서드가 아닌 함수로서 호출됨. 콜백함수는 함수이기 때문에

예제 4-8 : 콜백 함수 내부의 this에 다른 값을 바인딩하는 방법(1)-전통적인 방식; this를 다른 변수에 담아 콜백 함수로 활용할 함수에서는 this 대신 그 변수를 사용하게 하고, 이를 클로저로 만드는 방식이 많이 쓰이고 있음.

예제 4-9 : 콜백 함수 내부에서 this를 사용하지 않는 경우; 간결해진게 장점이지만, 작성한 함수를 this를 이용하여 다양한 상황에 재활용 할 수 없게 됨.

예제 4-10 : 예제 4-8의 func 함수 재활용; 번거롭긴 하지만 this를 우회적으로 활용함으로써 다양한 상황에서 원하는 객체를 바라보는 콜백 함수를 만들 수 있는 방법

예제 4-11 : 콜백 함수 내부의 this에 다른 값을 바인딩하는 방법(2) - bind 메서드 활용; ES5에 등장한 bind 메서드를 이용하는 방법.

예제 4-12 : 콜백 지옥 예시(1-1); 콜백 지옥은 콜백 함수를 익명 함수로 전달하는 과정이 반복되어 코드의 들여쓰기 수준이 감당하기 힘들 정도로 깊어지는 현상으로, 자바스크립트에서 흔히 발생하는 문제로 주로 이벤트 처리나 서버 통신과 같이 비동기적인 작업을 수행하기 위해 등장

예제 4-13 : 콜백 지옥 해결- 기명함수로 변환; 가독성 문제와 값이 전달되는 순서가 아래에서 위로 향하는 어색함을 해결 할 수 있는 방법은 익명의 콜백함수를 모두 기명함수로 전환하는 것.

예제 4-14 : 비동기 작업의 동기적 표현(1) - Promise(1); 비동기적인 일련의 작업을 동기적으로 보이게끔 처리해주는 장치를 마련하고자 ES6에서는 Promise, Generator 등이 도입 됨.

예제 4-15 : 비동기 작업의 동기적 표현(2) - Promise(2); 예제 4-14의 반복적인 내용을 함수화하여 간결화, 클로저 등장

예제 4-16 : 비동기 작업의 동기적 표현(3) - Generator; next라는 메서드를 가진 Iterator가 반환되는데, 이 next 메서드를 호출하면 Generator 함수 내부에서 가장 먼저 등장하는 yield에서 함수의 실행을 멈춤 

예제 4-17 : 비동기 작업의 동기적 표현(4) - Promise + Async/await; Promise의 then과 유사한 효과- 비동기 작업을 수행하고자 하는 함수 앞에 async를 표기하고, 함수 내부에서 실질적인 비동기 작업이 필요한 위치마다 await를 표기하는 것만으로 뒤의 내용을 Promise로 자동 전환하고, 해당 내용이 resolve된 이후에야 다음으로 진행

예제 5-1 : 외부 함수의 변수를 참조하는 내부 함수(1); '클로저=어떤 함수에서 선언한 변수를 참조하는 내부함수에서만 발생하는 현상', 외부함수에서 변수를 선언하고 내부함수에서 해당 변수를 참조하는 형태의 코드

예제 5-2 : 외부 함수의 변수를 참조하는 내부 함수(2); 예제 5-1&5-2는 outer 함수의 실행 컨텍스트가 종료되기 이전에 inner 함수의 실행 컨텍스트가 종료돼 있으며, 이후 별도로 ㄹinner 함수를 호출할 수 없다는 공통점이 있음.

예제 5-3 : 외부 함수의 변수를 참조하는 내부 함수(3); 어떤 함수에서 선언한 변수를 참조하는 내부함수에서만 발생하는 현상 = 외부 함수의 LexicalEnvironmnet가 가비지 컬렉팅되지 않는 현상

예제 5-4 : return 없이도 클로저가 발생하는 다양한 경우; 외부로 전달이 곧 return만을 의미하는 것이 아님. 두 상황 모두 지역변수를 참조하는 내부함수를 외부에 전달했기 때문에 클로저임.

예제 5-5 : 클로저의 메모리 관리; 클로저는 어떤 필요에 의해 의도적으로 함수의 지역변수를 메모리를 소모하도록 함으로써 발생. 그 필요성이 사라진 시점에서는 더는 메모리 소모를 안하면 

예제 5-6 : 콜백 함수와 클로저(1); 콜백 함수 내부에서 외부 데이터를 사용하고자 할 때

예제 5-7 : 콜백 함수와 클로저(2); 공통 함수로 쓰고자 콜백 함수를 외부로 꺼내어 alertFruit라는 변수에 담아 직접 실행 가능, 콜백 함수의 인자에 대한 제어권을 addEventListener가 가진 상태

예제 5-8 : 콜백 함수와 클로저(3); 클릭한 대상의 과일명이 아닌 [object MouseEvent]라는 값이 출력되는 이유는 addEventListener는 콜백 함수를 호출할 때 첫 번째 인자에 이벤트 객체를 ㄹ주입하기 때문인데 이는 bind 메서드로 해결 가능

예제 5-9 : 콜백 함수와 클로저(4); 콜백 함수를 고차함수로 바꿔 함수의 실행 결과가 다시 함수가 되며, 이렇게 반환된 함수를 리스너에 콜백 함수로써 전달. alertFruitBuilder의 실행 결과로 반환된 함수에는 클로저가 존재

예제 5-10 : 간단한 자동차 객체; 값을 마음대로 바꾸지 못하도록 방어하려면 클로저를 활용.

예제 5-11 : 클로저로 변수를 보호한 자동차 객체(1); 비공개 멤버로 지정해 외부에서의 접근을 제한했고, 읽기 전용 속성을 부여하여 값을 변경하고자 하는 시도를 막음

예제 5-12 : 클로저로 변수를 보호한 자동차 객체(2); run 메서드로 다른 내용을 덮어씌우는 어뷰징은 여전히 가능함. 객체를 return하기 전에 미리 변경할 수 없게끔 조치

예제 5-13 : bind 메서드를 활용한 부분 적용 함수; 부분 적용 함수란 n개의 인자를 받는 함수에 미리 m개의 인자만 넘겨 기억시켰다가, 나중에 n-m개의 인자를 넘기면 비로소 원래 함수의 실행 결과를 얻을 수 있게끔 하는 함수

예제 5-14 : 부분 적용 함수 구현(1); addPartial 함수는 인자 5개를 미리 적용하고, 추후 추가적으로 인자들을 전달하면 모든 인자를 모아 원래의 함수가 실행되는 부분 적용 함수

예제 5-15 : 부분 적용 함수 구현(2); 비워놓음을 표시하기 위해 미리 전역객체에 _ 라는 프로퍼티를 준비하면ㅅ너 삭제 변경 등의 접근에 대한 방어 차원에서 여러 가지 프로퍼티 속성을 설

예제 5-16 : 부분 적용 함수 - 디바운스; 짧은 시간 동안 동일한 이벤트가 많이 발생할 경우 이를 전부 처리하지 않고 처음 또는 마지막에 발생한 이벤트에 대해 한 번만 처리하는 것으로, 프런트엔트 성능 최적화에 큰 도움을 주는 기능 중 하나(scroll, wheel, mousemove, resize 등에 적용하기 좋음)

예제 5-17 : 커링 함수(1); 여러 개의 인자를 받는 함수를 하나의 인자만 받는 함수로 나눠서 순차적으로 호출될 수 있게 체인 형태로 구성한 것. 커링은 한 번에 하나의 인자만 전달하는 것을 원칙으로 함.

예제 5-18 : 커링 함수(2); 원하는 시점까지 지연시켰다가 실행하는 것이 요긴한 상황이라면 커링을 쓰기에 적합함.(당장 필요한 정보만 받아서 전달하고 또 필요한 정보가 들어오면 전달하는 식으로 하면 결국 마지막 인자가 넘어갈 때까지 함수 실행을 미루는셈이 되는데 이를 지연실행 이라고 함)



예제 6-1 : Person.prototype; Person이라는 생성자 함수의 Prototype에 getName 메서드를 지정했다고 했을 때 인스턴스는 __ proto __ 프로퍼티를 통해 getName을 호출할 수 있음.

예제 6-2 : Prototype과 __ proto __ ; 생성자 함수의 prototype에 어떤 메서드나 프로퍼티가 있다면 인스턴스에서도 마치 자신의 것처럼 해당 메서드나 프로퍼티에 접근할 수 있게 됨.

예제 6-3 : constructor 프로퍼티; 원래의 생성자 함수(자기 자신)를 참조함. 굳이? 싶지만, 인스턴스로부터 그 원형이 무엇인지를 알 수 있게 만드는 수단

예제 6-4 : constructor 변경; constructor를 변경하더라도 참조하는 대상이 변경될 뿐, 이미 만들어진 인스턴스의 원형이 바귄다거나 데이터 타입이 변하는 것은 아님

예제 6-5 : 다양한 constructor 접근 방법; 어떤 인스턴스로부터 생성자 정보를 알아내는 유일한 수단인 constructor가 항상 안전하지는 않지만 오히려 그렇기 때문에 클래스 상속을 흉내 내는 등이 가

예제 6-6 : 메서드 오버라이드; 인스턴스가 동일한 이름의 프로퍼티 또는 메서드를 가지고 잇는 상황이라면, 자신으로부터 가장 가까운 메서드에만 접근할 수 있지만, 그 다음으로 가까운 __ proto __ 의 메서드도 우회적인 방법이긴하지만 접근이 가능함.

예제 6-7 : 배열에서 배열 메서드 및 객체 메서드 실행; 기본적으로 모든 객체의 __ proto __ 에는 object.prototype이 연결됨. prototype 객체도 예외가 아님.

예제 6-8 : 메서드 오버라이드와 프로토타입 체이닝; 어떤 데이터의 __ proto __ 프로퍼티 내부에서 다시 __ proto __ 프로퍼티가 연쇄적으로 이어진 것을 프로토타입 체인이라 하고, 이 체인을 따라가며 검색하는 것을 프로토타입 체이닝이라고 함.

예제 6-9 : Object.prototype에 추가한 메서드에의 접근; 어떤 생성자 함수이든 prototype은 반드시 객체이기 때문에 object.prototype이 언제나 프로토타입 체인의 최상단에 존재하게 됨. 따라서 객체에서만 사용할 메서드는 다른 여느 데이터 타입처럼 프로토타입 객체 안에 정의할 수가 없음.

예제 6-10 : Grade 생성자 함수와 인스턴스; 대각선의 __ proto __ 를 연결하는 방법은 __ proto __ 가 가리키는 대상, 즉 생성자 함수의 prototype이 연결하고자 하는 상위 생성자 함수의 인스턴스를 바라보게끔 해주면 됨.




예제 7-1 : 스태틱 메서드, 프로토타입 메서드; 인스턴스에 상속되는지(인스턴스가 참조하는지) 여부에 따라 스태틱 멤버와 인스턴스 멤버로 나뉘어짐. / 자바스크립트에서는 인스턴스에서도 직접 메서드를 정의할 수 있기에 혼란을 야기할 수 있음. 때문에 프로토타입 메서드라고 불림.

예제 7-2 : 6-2-4절의 Grade 생성자 함수 및 인스턴스; Length 프로퍼티가 configurable(삭제가능)하다는 점과, Grade.prototype에 빈 배열을 참조시켰다는 문제점이 있음.

예제 7-3 : length 프로퍼티를 삭제한 경우; 다시 push했더니, push한 값이 0번째 인덱스에 들어갔고, length가 1이 됨. 내장객체인 배열 인스턴스의 length 프로퍼티는 configurable 속성이 false라서 삭제가 불가능하지만, Grade 클래스의 인스턴스는 배열 메서드를 상속하지만 기본적으로는 일 객체의 성질을 그대로 지니므로 삭제가 가능해서 문제가 됨.

예제 7-4 : 요소가 있는 배열을 prototype에 매칭한 경우; Array 내장 클래스를 상속하는 Grade 클래스의 case & 클래스에 있는 값이 인스턴스의 동작에 영향을 주면 안됨. 인스턴스와의 관계에서는 구체적인 데이터를 지니지 않고 오직 인스턴스가 사용할 메서드만을 지니는 추상적인 틀로서만 작용하게끔 작성하면 예기치 않은 오류가 발생할 가능성 X

예제 7-5 : Rectangle.Square 클래스; 사용자가 정의한 두 클래스 사이에서의 상속관계 case, 넓이를 구하는 getArea 메서드를 각 클래스에 추가한 상황

예제 7-6 : Square 클래스 변형; Square에서 width 프로퍼티만 쓰지 않고 height 프로퍼티에 width 값을 부여하는 형태가 된다면 getArea도 동일하게 고칠 수 있음.

예제 7-7 : Rectangle을 상속하는 Square 클래스; Square의 생성자 함수 내부에서 Rectangle의 생성자 함수를 함수로써 호출. 인자 height 자리에 width를 전달 & 메서드를 상속하기 위해 Square의 프로토타입 객체에 Rectangle의 인스턴스를 부여

예제 7-8 : 클래스 상속 및 추상화 방법(1) - 인스턴스 생성 후 프로퍼티 제거; 클래스가 구체적인 데이터를 지니지 않게 하는 첫 번재 방법으로, extendClass1 함수는 SuperClass & SubClass에 추가할 메서드들이 정의된 객체를 받아서 SubClass의 prototype 내용을 정리하고 freeze하는 내용으로 구성돼있음.

예제 7-9 : 클래스 상속 및 추상화 방법(2) - 빈 함수를 활용; 클래스가 구체적인 데이터를 지니지 않게 하는 두 번째 방법으로, Bridge라는 빈 함수를 만들고, Bridge.prototype이 Rectangle.prototype을 참조하게 한 다음, Square.prototype에 new Bridge()로 할당하면, 우측 그림처럼 Rectangle 자리에 Bridge가 대체됨. 이로써 인스턴스를 제외한 프로토타입 체인 경로상에는 더는 구체적인 데이터가 남아있지 않게 됨. 즉시실행함수 내부에서 Bridge를 선언해서 이를 클로저로 활용함으로써 메모리에 불필요한 함수 선언을 줄임. subMethods에는 SubClass의 prototype에 담길 메서드들을 객체로 전달하게끔 함.

예제 7-10 : 클래스 상속 및 추상화 방법(3) - Object.create 활용; ES5에 도입된 방법으로 SubClass의 prototype의 __ proto __ 가 SuperClass의 prototype을 바라보되, SuperClass의 인스턴스가 되지 않으므로 앞서 소개한 두 방법보다 간단하면서 안전함.

예제 7-11 : 클래스 상속 및 추상화 방법 - 완성본(1) - 인스턴스 생성 후 프로퍼티 제거; Constructor 복구 방법으로, 앞선 방법 세 가지로는 SubClass 인스턴스에는 constructor가 없고, SubClass.prototype에도 없는 상태. 프로토타입 체인상에 가장 먼저 등장하는 SuperClass.prototype의 constructor에서 가리키는 대상 SuperClass가 출력될 뿐.

예제 7-12 : 클래스 상속 및 추상화 방법 - 완성본(2) - 빈 함수를 활용; SubClass.prototype.constructor가 원래의 SubClass를 바라보도록 함.

예제 7-13 : 클래스 상속 및 추상화 방법 - 완성본(3) - Oject.create 활용; 일반적인 객체지향 언어에서의 클래스보다는 부족하지만, 어쨋건 기본적인 상속 및 추상화 달성

예제 7-14 : 상위 클래스 접근 수단인 super 메서드 추가; 하위 클래스에서 상위 클래스의 프로토타입 메서드에 접근하기 위한 별도의 수단으로, 다른 객체지향 언어들의 클래스 문법 중 하나인 'super'를 흉내 내보며 상위 클래스에의 접근 수단을 제공함.

예제 7-15 : ES5와 ES6의 클래스 문법 비교; class, constructor, staticMethod 바로 뒤에 {} 등장 & 메서드와 다음 메서드 사이에 콤마(.)로 구분 안함 & method라는 이름은 prototpye 객체 내부에 자동으로 할당되는 메서드임.

예제 7-16 : ES6의 클래스 상속; ES5에는 상속 문법 자체가 없음. & Square를 Rectangle 클래스를 상속받는 SubClass로 만들기 위해 class 명령어 뒤에 단순히 extend Rectangle 내용을 추가하여 상속 관계 설정을 끝냄 & constructor 내부에는 super 라는 키워드를 함수처럼 사용할 수 있는데 이는 SuperClass의 constructor를 실행함. & constructor 메서드를 제외한 다른 메서드에서는 super 키워드를 마치 객체처럼 사용할 수 있고, 이때 객체는 SuperClass.prototype을 바라보는데, 호출한 메서드의 this는 super가 아닌 원래의 this를 그대로 따름.

