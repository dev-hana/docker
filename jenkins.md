## 1. jenkins 이미지 받기  
   `docker pull jenkins/jenkins`  

## 2. jenkins 컨테이너 실행
   `docker run -d -p 30000:8080 --restart=always -v /var//jenkins:/var/jenkins_home -v/var/run/docker.sock:/var/run/docker.sock --name jenkins -u root jenkins/jenkins`   

## 3. jenkins 내부에 도커 설치  
   `docker exec -it jenkins /bin/bash`   
   `curl -fsSL https://get.docker.com/|sh`  

## 4. jenkins 접속 password 확인  
   `docker logs jenkins`  
