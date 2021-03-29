# 스프링부트 기준 application.properties 설정 방법

## 포트 설정
```properties
server.port=8060
```

## 커넥션 설정
```properties
spring.datasource.url=
spring.datasource.username=
spring.datasource.password=
spring.datasource.driver-class-name=org.mariadb.jdbc.Driver
```

## 구동 및 종료 시 동작
```properties
# JPA가 생성한 SQL문을 콘솔에 표시해준다.
spring.jpa.show-sql=true
# 옵션에 따라 서버 실행 또는 종료시 테이블에 다음과 같은 동작을 한다.
# create : 기존 테이블 삭제 후 새로 만든다.
# create-drop : 종료 시 기존 테이블을 삭제한다.
# update : 변경 부분만 적용한다.
# validate : 엔티티와 테이블간의 매핑 정상 여부만 검증한다.
# none : 아무런 동작을 하지 않는다.
spring.jpa.hibernate.ddl-auto=update
# 위 hivernate에 의한 옵션 기능을 사용할지의 여부
spring.jpa.generate-ddl=true

# 테이블 대문자 연동 (JPA Default는 소문자 테이블인듯)
spring.jpa.hibernate.naming.physical-strategy=org.hibernate.boot.model.naming.PhysicalNamingStrategyStandardImpl
spring.jpa.hibernate.naming.implicit-strategy=org.hibernate.boot.model.naming.ImplicitNamingStrategyLegacyJpaImpl
```
