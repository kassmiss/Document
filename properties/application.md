``properties

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

``
