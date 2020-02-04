# Spring-Note

동작부터 효율성까지!

스프링 원리부터 내부 코드까지 

모든 개념을 이해하고 키워드 정리



## bean 

- 특정기능이 정의된 클래스 

- 예) dto dao @controller 등등 

## 클래스 vs 객체

- 클래스는 `붕어빵`틀 객체는 `붕어빵` 

- 클래스로 객체를 여러개 생성한다.

## builder pattern

- .setemail 등등으로 이어서  `조금 더 명시적`으로

- 정확하게 객체를 만들 수 있다.


## 인터페이스 

- `클래스들의 구현 동작`을 지정하는 추상형 형태

- 다중상속 가능 

- 인터페이스 메소드만 알면됨

- 다형성을 이용해서 인터페이스의 구현객체를 손쉽게 교체

## 제네릭 

- 사용할 데이터 타입을 외부에서 지정하는 기법

## OOP vs AOP

- 캡슐화 다형성 추상형 상속

- 하나의 메소드나 클래스가 다른의미로 해석 (오버로딩)

- 객체지향 기능들을 클래스 단위로 쪼개서 재활용성이 좋지만 

- 로그 트랜잭션 등 때문에 모듈화 하기 어렵다.

=> `그래서`

- OOP의 한계 개선과 `횡단관심사를 분리`해서 기본 비즈니스로직 외 다른코드 와 분리

- core crosscutting 필요할때 소스코드가 자동으로 삽입됨 

## AOP 동작 구조

- target(핵심) 

- advice(횡단) 

- jointpoint(Advice가 target에 적용되는 지점) 

- pointcut(jointpoint가 적용되는 클래스를 선택)

- weaving (Advice가 target에 실제로 적용되는 것)


## IOC /DI

- 사용하는 객체를 new처럼 자기가 생성하는게 아니라 다른 곳에서 하는것 (주입을 받아 사용하는것)

- bean(spring ioc가 관린하는 객체)에 @controller @service 주입하는 예

## IOC컨테이너 = 어플리케이션 컨텍스트 

- 의존성 관리는 컨테이너만 비즈니스로직만 신경 그리고 확장성증가 

- `빈팩토리+다른 추가적인 인터패이스 제공`


## JSP vs Servelt 

- HTML    JAVA 

- 서블릿은 자바의 하나의 클래스이다. 동적페이지를 만들게 된는데 너무 복잡하고 느려져서

- jsp를 만든다 이런한 내용은 스프링 mvc 패턴에서 서블릿은 컨트롤러 jsp는 view를 담당한다. 

- 둘의 내용은 비슷한다.

- 웹컨테이너(서블릿 컨테이너) url과 서블릿 매핑 서블릿 생명주기 관리등


## Web Server vs WAS

- 정적            동적,여러개의 트랜잭션, 미들웨어, 과부화

- 로브밸런싱, 자바 php등 다향하게 씀, 과부하 방지 
                      
- 속도보단 !!



## 컨테이너 (Container)

- 특정 객체의 생성과 관리를 담당하며 객체 운용에 필요한 다양한 기능을 제공

- 개발자가 작성한 코드를 스스로 참조하여 알아서 객체의 생성과 소멸을 제어(control) 해준다.

 

 

## 결합도(Coupling)

- 하나의 클래스가 다른 클래스와 얼마나 많이 연결되어 있는지에 대한 정도

- 결합도가 높을수로 유지보수가 어렵다.

 

## 결합도를 낮추기 위한 방법

1. 다형성 이용하기

2. 디자인 패턴 이용하기 

3. 의존성 주입하기 (SpringFramework 방식)

## 프로시져

프로시져는 특정 동작이나 연산을 위한 명령들을 별도로 마련하여 필요할 때마다 사용하는 것으로 (함수로 구현)

프로그램에서 이름을 부를 때마다 실행이 됩니다. 

이 때 프로시져에서 사용하는 값을 매개변수를 통하여 전달하기도 합니다.


## array vs linked list

논리적 저장 순서와 물리적 저장 순서의 일치 여부이다!

array는 조회시 O(1) 다만 삭제 삽입이 힘들다. 다 당겨야돼서

linked는 다음것만 가르키기 때문에 삽입 삭제는 쉽지만 어떤값을 가려면 다알아야한다.


## jpa(ORM) vs mybatis(mapper)

재활용성

직관적 

객체와 디비 자동  직접쿼리

자동등록              세밀함,속도

## JVM

os관계없이 자바코드를 자동으로 해석해주고 실행시키는 운영체제

플랫폼 의존적 리눅스와 윈도우 다르다

메모리관리 가비지컬렉터 스택구조

메소드영역 클래스가 사용되면 분석하여 정보를 저장 

힙영역 여기서 인스턴스 생성

스택영역 메소드 호출시 메모리제공

## JRE

자바 실행 프로그램 + 라이브러리

## JDK 

개발 필요한 도구들


## 람다식 

익명의 함수만들때 => {}로 표현한다 .

식별자 없이 실행가능한 함수표현식 함수형프로그래밍 

-> {} 코드가 더 직관적 

일급객체가 아니다 변수에 저장x , 리턴값 x, 파라미터 x,

하나의 인터페이스 하나의 추상클래스 


### JAR vs WAR

JAR 수많은 자바 클래스 파일들이 압축되어 있는 상태 

자바 플랫폼에 응용소프트웨어나 라이브러리를 배포하기 위한 패키지 파일

WAR 자바 이외에도 jsp 서블릿 html 등 이 더해져 있는상태 


## Annotion 

말그대로 주석 컴파일러에게 이 클래스나 메소드가 뭔지 알려주는 역할


## apache Spark

spark SQL등 사용되고 다양한 언어를 제공하면서 

빅데이터 고속 처리를 위한 오픈소스 병렬 분산 처리 플랫폼

## apache Kafka

분산 시스템을 기본으로 설계되었기 때문에, 기존 메시징 시스템

분산 복제에 유리

 메시징 플랫폼
 
 대용량의 메시지를 빠르게 처리하도록 개발

여러 스토리지의 데이터를 분석 시스템에 연결해 주기 위한 도구

## TCP vs UDP 

- 둘다 다른 컴퓨터와 데이터 통신을 하기위한 규약(프로토콜)의 일종입니다.

- TCP(Transmission Control Protocol)는 패킷 전송할때 송수신자가 패킷을 보내고받을때 

서로 확인하기 때문에 데이터의 전송이 정확하지만 느립니다. 신뢰성이 보장되기 때문에 

현존하는 대부분의 네트워크 프로그램은 TCP 방식입니다.

- UDP(User Datagram Protoco)는 패킷 전송할때 송수신자가 패킷을 보내고받을때 확인하지 않기 때문에

100% 정확하게 전송되지 않아 누락된 데이터가 있지만 빠릅니다. 보통 유튜브 같은 스트리밍 서비스, VoIP 서비스가 UDP 방식입니다.

## DNS
Domain name system의 약자로 IP주소를 외우기 너무 힘들기 때문에 domain이란 것을 만들었다.

## API vs Rest API

결론 API가 더 크다 굳이 차이점이라면 http 프로토콜을 사용하는 API 끝 


## NoSQL

- 조인 연산이 불가능하며, 각 데이터가 독립적으로

 설계되어 있어 데이터를 여러 서버에 분산하여 작업하는 방식으로
- 데이터를 여러 서버에 분산하는 것을 통하여 각 서버에서 처리하는

 데이터의 양이 줄고 따라서 대량의 데이터의 입출력이 있어도 처리가 간단한 특징이 있습니다.




## REST의 특징

-  Uniform (유니폼 인터페이스) : HTTP 표준에만 따른다면, 안드로이드/IOS 플랫폼이든, 

특정 언어나 기술에 종속되지 않고 모든 플랫폼에 사용이 가능

- Stateless (무상태성) : HTTP는 Stateless Protocol 이므로, REST 역시 무상태성을 갖는다. 

즉, HttpSession과 같은 컨텍스트 저장소에 상태정보를 따로 저장하고 관리하지 않고, 

API 서버는 들어오는 요청만을 단순 처리하면 된다. 

세션과 같은 컨텍스트 정보를 신경쓸 필요가 없어 구현이 단순해진다.

- Cacheable (캐시가능) 

- Self-descriptiveness (자체 표현 구조) : 동사(Method) + 명사(URI) 로 이루어져있어 어떤 메서드에 

무슨 행위를 하는지 알 수 있으며, 메시지 포맷 역시 JSON을 이용해서 직관적으로 이해가 가능한 구조로

, REST API 메시지만 보고도 이를 쉽게 이해할 수 있다.

- Client - Server 구조 : 의존성 줄임

- 계층형 구조 : API 서버는 순수 비지니스 로직을 수행하고, 그 앞단에 사용자 인증, 암호화(ssl),

 로드밸런싱 등을 하는 계층을 추가하여 구조상의 유연상을 둘 수 있다. 
 
 API gateway 등을 활용하여 Micro Service Architecture로도 구현이 가능하게 한다.


## 동기 비동기 논블락킹 블락킹

응답과 요청 동시에, 종료시간 시작시간 같으면 동기 

다른요청이 있을때 까지 기다려야한다.


## 동작구조

1. 요청 => 컨트롤러 => 서비스 => DAO => myBatis => DB 

2. 요청 => 디스패치서블릿(퍼스트컨트롤러) => 핸들러맵핑 => 맵핑된 컨트롤러가 잇으면 처리요청 =>

dto =>[ Service(비즈니스 계층) => dao(퍼시스턴트 계층)  model]=> mybatis => db

=> mapper =>dao => Service =>dto =>controller(servlet) => jsp(view) => client

3. 요청=> 디스패치서블릿 => 핸들러맵핑 => 맵핑된 컨트롤러 검색 => 처리요청 

=> 컨트롤러 => 디스패치 서블릿  모델과 뷰로 결과리턴 => 뷰가 없으면 모델만 

뷰가있으면 => 뷰리절버에서 찾아서 => 뷰까지 보내줌 

## 스프링 




# 프레임워크

- 개발환경 뼈대 소프트웨어는 아니다.
- 솔루션이 아니다 반제품이다. (개발자가 어느정도 개발해야함) 

## 분류

- 계층 분류(시스템인프라, 미들웨어, 엔터프라이즈)
- 확장 분류(화이트, 블랙)
- 처리 영역 분류(기능, 지원, 통합)

## 화이트 박스 Framework vs 블랙 박스 Framework

- 객체지향 언어가 제공하는 `상속이나 동적바인딩`의 의존 확장 Framework
- Framework 코어의 베이스 클래스를 상속 미리 정의된 Hook Point

- Framework에서 정의한 인터페이스를 구현`하고 구현한 객체를 인터페이스로 확장함 
- 상속없이 컴포지션과 딜리게이션(위임)으로 확장, 의존성 낮음, 미래 개발자가 다 개발해야함 




## 자바프레임 워크

### 웹어플리케이션 Framework

- SpringMVC
- struts
- WebWork

### 데이터베이스 관련 Framework

- iBatis
- Hibernate
- SpringDAO

### 비즈니스 관련 framework

- Spring

## Spring Framework의 특징 

- 크기와 부하의 `경량`

- IOC(제어역행) 결합도를 낮춤

- AOP 풍부한 자원 지원

- 어플리케이션 객체의 생명주기와 설정을 포함하고 관리 일종의 Container

- 간단한 컴포넌트로 복잡한 어플리케이션을 구상 설정 가능 


## IOC

- 기존에는 userDAO를 메소드 마다 new로 만들어야 한다면 

- setUserDAO()메소드만 만들면 된다. 

## AOP

- 겹치는 로깅 보안 트랜잭션을 모듈로 분리해서 (횡단)

- 비지니스 로직과 시스템 서비스를 분리한다.

## Container 

- 객체의 생성 및 관리를 담당하는 일종의 서버 개념 

- 기존 컨테이너들 서블릿 컨테이너 EJB 컨테이너는 각각 서블릿 EJB를 관리 했지만

- 스프링 컨테이너는 애플리케이션 객체의 생명주기와 설정을 포함하고 관리함 

- 관리대상인 `Bean의 객체` 대한 제어, 연관도 자유롭게 설정

### 복잡한 구조 개발가능

- XML 사용 


## Spring Framework의 구성 

`7개의 모듈`로 제공 됨 

- Spring AOP

- Spring ORM

- Spring DAO

- Spring Web

- Spring Context

- Spring Web MVC

- Spring Core


### Spring AOP

- Spring의 메타데이터 자원을 사용해서 메타데이터 프로그래밍 가능

- Spring이 어디에 어떻게 aspect를 적용할지 annotation 제공

### Spring ORM

- Hibermate, iBATIS를 포함하는 객체-관계 맵핑 API를 위한 통합 레이어 제공 

### Spring DAO

- JDBC 코딩과 데이터베이스 업체 특성 에러코드의 파싱의 필요를 제거하는 JDBC추상화 레이어를 제공

- JDBC패키지는 특정 인터페이스를 구현하는 클래스와 POJO 객체들을 위한 선언적인 트랜잭션 관리 

### Spring Web

- 멀티파트기능, 서블릿 리스너를 사용한 컨텍스트 초기화, 웹-기반 통합 기능 제공 

- WebWork, Struts 와 Spring으 사용할 때 통합될 수 있도록 지원 

### Spring Core

- Framework의 가장 기본적인 부분 

- beanContainer를 기능적으로 관리 DI기능 제공 

- 프로그램에 따른 싱글톤의 필요성을 제거하는 factory패턴 제공

- BeanFactory임 = 실질적인 프로그램 로직으로부터 설정과 의존성 명시 분리 



### Controller 

- 단순처리 -> AbstractController

- 파라미터매핑 -> AbstractCommandMapping

- 입력폼처리 -> SimpleFormController

- 다중 페이지 입력 폼처리 - AbstactWizzardFormController

- 정적뷰 매핑 -> 파라미터 뷰 컨트롤러, urlfilenameviewController

- 다중액션 -> MultiActionController

### Annotation

#### AOP 설정 

- @Aspect 
- @Pointcut


#### Aspect 설정 

- @Before
- @After
- @AfterReturning
- @AfterThrowing
- @Around

### AOP


### 라우터

라우터를 10개로 쪼갠거랑 1개로 나눈거랑 속도는 절대로 관련없다!!! 

[localhost:4000/zetsu](http://localhost:4000/zetsu/)

