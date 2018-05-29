# README

Docker로 Nginx와 PHP 환경을 빠르게 구성하는 방법을 소개하며 [Docker](https://www.docker.com/)가 설치되어 있어야합니다.

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
  
  자세한 설명은 `docker-compose --help`

  ```bash
  # container 생성 및 실행
  $ docker-compose up

  # container 실행
  $ docker-compose start
  
  # container 중단
  $ docker-compose stop
  
  # container 삭제
  $ docker-compose down
  ```
