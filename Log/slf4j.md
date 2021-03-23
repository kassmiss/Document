# 스프링부트 기준 application.properties 작성

```properties
# 전체 로그
logging.level.root=info

# 특정 패키지 로그
logging.level.com.grlife.login=info
logging.level.com.grlife.login.controller=debug

# 스프링 프레임워크 로그
logging.level.org.springframework.web=debug

# SQL 로그
logging.level.sql=error

# hibernate에서 생성하는 SQL 로그 끄기
logging.level.org.hibernate.SQL=off

# JDBC 로그
logging.level.jdbc=error
logging.level.jdbc.sqlonly=debug

# 명시한 용량을 초과할 경우 기존 로그를 .gz로 압축하고 신규로 로그를 쌓는다.
logging.logback.rollingpolicy.max-file-size=100MB

# 해당 일수가 지난 로그는 삭제한다.
logging.logback.rollingpolicy.max-history=9999999

# 사용자의 홈 디렉토리 아래 폴더 및 파일 생성 됨
logging.file.name=${user.home}/logs/product.log

#  로그 패턴 설정 (개발툴 콘솔 로그, 파일에 쌓이는 로그 패턴)
logging.pattern.console=%-5level %d{yyyy-MM-dd HH:mm:ss}[%thread] [%F - %M] [%logger{0}:%line] - %msg%n
logging.pattern.file= %-5level %d{yyyy-MM-dd HH:mm:ss}[%thread] [%F - %M] [%logger{0}:%line] - %msg%n
```

# 사용법
```java

public class LoginService {

    private final Logger logger = LoggerFactory.getLogger(this.getClass());

    private final LoginRepository loginRepository;

    public Long save(UserInfo userInfo) {

        logger.trace("Trace Level 테스트");
        logger.debug("DEBUG Level 테스트");
        logger.info("INFO Level 테스트");
        logger.warn("Warn Level 테스트");
        logger.error("ERROR Level 테스트");
        
    }
}

```
