# Internet-Of-Things
23-1 Prof.Song

각 예제들에 대한 요점입니다.

예제 1-1 : 기본적인 변수 선언식, 가변 데이터 생성. 가변 데이터의 식별자 = a
예제 1-2 : 변수 선언과 더불어 데이터를 할당하는 과정, 변수영역과 데이터영역을 분리하면 중복 데이터에 대한 처리 효율 상승
예제 1-3 : 불변성; 문자열 값과 숫자 값 모두 한 번 만들었다면 다른 값으로 바꿀 수 없고, 새로 만드는 동작을 통해서만 이루어짐.
예제 1-4 : 참조한 데이터를 할당하는 과정; 가변형 데이터와는 달리 객체의 변수 영역이 별도로 존재 & 데이터 영역에 저장된 값은 모두 불변값
예제 1-5 : 참조형 데이터의 프로퍼티를 재할당하는 과정; 새로운 객체가 만들어진 것이 아니라 기존의 객체 내부의 값만 바뀐 것 = 중첩객체
예제 1-6 : 중첩된 참조형 데이터객체의 프로퍼티 할당; 재할당 명령을 내리게 될 시 참조 카운트가 0이 되어 가비지컬렉터의 수거 대상이 됨
예제 1-7 : 변수 복사; 기본형 데이터와 참조형 데이터의 차이 - 복사과정은 동일하지만 데이터 할당 과정에서 차이 발
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
예제 1-18 : JSON을 활용한 간단한 깊은 복사 : 객체를 JSON 문법으로 표현된 문자열로 전환했다가 다시 JSON 객체로 바꾸는 방
예제 1-19 : 자동으로 undefined를 부여하는 경우 : 값을 대입하지 않는 경우 특이한 동작이 발생
예제 1-20 : undefined와 배열 : 각 3개의 빈 요소에는 문자 그대로 어떤 값도 할당돼 있지 않음을 의미
예제 1-21 : 반 요소와 배열의 순회 : 존재하지 안흔 프로퍼티ㅏ에 대해 순회 불가능한 것은 당연. 배열은 length 프로퍼티의 개수만큼 빈 공간을 확보하고 각 공간에 인덱스를 이름으로 지정할 것이라 생각하기 쉽지만, 실제로는 객체와 마찬가지로 특정 인덱스에 값을 지정할 때 비로소 빈 공간을 확보하고 인덱스를 이름으로 지정하고 데이터의 주솟값을 저장하는 등의 동작을 수행
예제 1-22 : undefined와 null 비교 : 어떤 변수가 실제 null인지 undefined인지 동등 연산자로는 비교 불가능, 일치 연산자(===)를 사용해야함

예제 2-1 : 실행 컨텍스트와 콜 스택 : 콜스택에 실행 컨텍스트가 어떤 순서로 쌓이고, 어떤 순서로 코드 실행에 관여하는지 확인하는 과
예제 2-2 : 매개변수와 변수에 대한 호이스팅(1) - 원본코드; 인자를 함수 내부의 다른 코드보다 먼저 선언 및 할당이 이뤄진 것으로 간주 가능
예제 2-3 : 매개변수와 변수에 대한 호이스팅(2) - 매개변수를 변수 선언/할당과 같다고 간주해서 변환한 상
예제 2-4 : 매개변수와 변수에 대한 호이스팅(3) - 호이스팅을 마친 상태
예제 2-5 : 함수 선언의 호이스팅(1) - 원본코드
예제 2-6 : 함수 선언의 호이스팅(2) - 호이스팅을 마친 상태
예제 2-7 : 함수 선언의 호이스팅(3) - 함수 선언문을 함수 표현식으로 바꾼 코드 
예제 2-8 : 함수를 정의하는 세 가지 방식 
예제 2-9 : 함수 선언문과 함수 표현식(1) - 원본 코드
예제 2-10 : 함수 선언문과 함수 표현식(2) - 호이스팅을 마친 상태
예제 2-11 : 함수 선언문의 위험
예제 2-12 : 상대적으로 함수 표현식이 안전하다.
예제 2-13 : 스코프 체인
예제 2-14 : 스코프 체인 확인(1) - 크롬 전
예제 2-15 : 스코프 체인 확인(2) - 크롬 전용
예제 2-16 : 스코프 체인 확인(3)

예제 3-1 : 전역 공간에서의 this(브라우저 환경)
예제 3-2 : 전역 공간에서의 this(Node.js 환경)
예제 3-3 : 전역변수와 전역객체(1)
예제 3-4 : 전역변수와 전역객체(2)
예제 3-5 : 전역변수와 전역객체(3)
예제 3-6 : 함수로서 호출, 메서드로서 호출
예제 3-7 : 메서드로서 호출 - 점 표기법, 대괄호 표기
예제 3-8 : 메서드 내부에
