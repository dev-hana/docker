
## 1. 도커 버전 확인하기  
  `docker --version`  

## 2. MySQL Image 다운로드  
  `docker pull mysql:8.0.17`  

## 3. Image 확인  
  `docker images`  

## 4. Container 생성 및 실행  
### user 생성 후 data directory 만들기(컨테이너 삭제 시 데이터 날라가는 것을 방지)  

  `docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password --name mysql -v /home/mysql/datadir:/var/lib/mysql mysql:8.0.17 --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci`    
  
## 5. docker 목록 확인  
  `docker ps -a`  

## 6. MYSQL Container bash shell 접속
  `docker exec -it [id/name] /bin/bash`  

## 7. mysql 접속  
  `mysql -u root -p`  
  
