# Maven과 Gradle의 차이에 대해 설명하시오.

Spring Boot에서 Maven과 Gradle은 대표적인 빌드 도구로 사용되며, 프로젝트를 빌드하고 의존성을 관리하며 배포 가능한 산출물을 만드는 데 쓰인다.

주요 역할
- 의존성 관리
- 소스코드 컴파일 및 테스트
- 실행 가능한 JAR 또는 WAR 파일 생성
- 배포 자동화
- 플러그인 기반 확장 지원

Spring Boot에서는 둘 다 공식적으로 지원되며, Spring Initializr에서도 자유롭게 선택할 수 있습니다.

둘의 두요 차이점은 다음과 같이 나타낼 수 있다.

## 1. 빌드 스크립트 문법

### Maven

- XML 기반인 pom.xml 파일로 구성
- 명시적이고 정형화되어 있어 구조가 분명하다 되어있으나, 반복적인 코드가 많아 가독성이 떨어질 수 있다.

``` xml
<!-- Maven -->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>
```

Gradle: Groovy/Kotlin DSL 기반(build.gradle)
   - 코드처럼 유연하게 작성 가능, 가독성이 좋고 재사용 가능


``` groovy
// Gradle
implementation 'org.springframework.boot:spring-boot-starter-web'
```


## 2. 빌드 성능

- Gradle: 속도가 빠름
    - 캐싱, 증분 빌드, 병렬 빌드를 지원
    - 대규모 프로젝트에서 유리
- Maven: 상대적으로 느림
    - 전체 빌드 위주, 병렬 처리에 제한

## 3. 의존성 관리


