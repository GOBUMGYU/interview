### Restful API에 대해 설명

- Restful API는 HTTP 통신을 Rest설계 규칙을 잘 지켜서 개발한 API를 Restful한 API라고 한다.
- Rest설계 규칙은 URI는 정보의 자원만 표현해야 하며, 자원의 상태와 행위는 HTTP Method에 명시하는 걸 말함

### 프레임워크와 라이브러리의 차이에 대해 설명

이 둘의 차이점은 제어 흐름에 대한 주도권이 누구에게어디에 있는가 이다.

- 프레임워크는 내가 작성한 코드를 제어하고, 대신 실행 (Junit)
- 라이브러리는 내가 작성한 코드가 직접 제어의 흐름을 담당한다면 라이브러리

### Call By Value와 Call By Reference의 차이점에 대해 설명

- Call By Value(값에 의한 호출) - 인자로 받은 값을 복사하여 처리하는 방식
    - 장점 - 값을 복사하여 처리하기 때문에 원래의 값이 보존된다.
    - 단점 - 복사하기 때문에 메로리 사용량이 증가한다.
- Call By Reference(참조에 의한 호출) - 인자로 받은 값이 주소를 참조하여 직접 저장해 값에 영향을 주는 방식
    - 장점 - 복사하지 않고 직접 참조하기에 다르다
    - 단점 - 직접 참조를 하기에 원래의 값이 영향을 받는다.

### OAuth2.0의 흐름에 대해 간단히 설명

- 사용자가 클라이언트에게 사용 요청을 보낸다.
- 클라이언트는 권한 서버에 권한 부여 승인 코드 요청(response_type=code 로 지정하여 요청)을 보낸다.
- 이후 클라이언트는 권한 서버에서 제공하는 로그인 페이지를 띄어 사용자에게 보여준다.
- 사용자가 로그인 하면 권한 서버는 (2)권한 부여 승인 코드 요청에 전달받은 redirect_url로 Authorization Code를 전달한다.
- Authorization Code는 권한 서버에게 제공하는 API를 통해 Access Token으로 교환된다.

### 동적 쿼리란 무엇이고 언제 동적 쿼리를 사용하나요

- 동적 쿼리란 실행시에 특정 조건이나 상황에 따라 쿼리 문장이 변경되어 실행되는 쿼리문을 말한다.
- 컴파일시에 SQL문장을 확정할 수 없는 경우에 사용한다. 실행 시점에 따라 where 조건이 달라질 때 사용
- 쿼리문이 변하냐 변하지 않느냐에 따라 정적쿼리/동적쿼리가 된다.

### 대칭키, 비대칭키 암호와 방식에 대해 설명

대칭키와, 비대칭키는 양방향 암호와 방식이다.

- 대칭키는 암호화와 복호화에 같은 암호 키를 쓰는 알고리즘
    - 이는 중간에 누군가 암호키를 가로채면 정보가 유출될 수 있다는 단점이 있는데, 이러한 문제를 보완한 방식이 바로 비대칭키이다.
- 비대칭키는 암호화와 복화를 할 때 서로 다른 키를 쓰는 알고리즘이다.
    - 타인에게 절대 노출되어서는 안되는 개인키와 공개적으로 개방되어 있는 공개키를 쌍으로 이룬 형태
