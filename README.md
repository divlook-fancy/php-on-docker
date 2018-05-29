# Docker로 Nginx와 PHP 쉽게 설정하는 방법

- [참고사이트](http://geekyplatypus.com/dockerise-your-php-application-with-nginx-and-php7-fpm/)

  # 설정

  ## site.conf 수정

  ```conf
  server {
    ...
    # local.hostname.com을 사용할 hostname으로 변경
    server_name local.hostname.com;
  ```

  ## hosts 추가

  - Path
    - linux, osx : `/etc/hosts`
    - window : `/Windows/system32/drivers/etc/hosts`

  ```conf
  # 아래 형식으로 local.hostname.com을 사용할 hostname으로 변경하여 추가
  127.0.0.1       local.hostname.com
  ```

  # 실행

  ```bash
  $ docker-compose up
  ```
