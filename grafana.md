참고문서 : https://github.com/grafana/grafana/blob/master/contribute/developer-guide.md



# Install

1. go download
   `wget https://golang.org/dl/go1.16.linux-amd64.tar.gz`
2. go install

   - extract

   ```
   tar -C /usr/local -xzf go1.16.linux-amd64.tar.gz
   ```

   

   - Add /usr/local/go/bin to the `PATH` environment variable

   ```shell
   # .bashrc 파일 최 하단에 추가
   export PATH=$PATH:/usr/local/go/bin
   ```

   

   - Save path

   ```shell
   source ~/.bashrc
   ```

   

   - check version

   ```shell
   go version
   ```

   

3. node install
   https://tecadmin.net/install-latest-nodejs-npm-on-ubuntu/

   ```
   sudo apt-get update
   sudo apt-get install curl
   curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
   ```

   ```
   sudo apt-get install nodejs
   node -v
   ```

4. install yarn

   ```
   sudo npm install -g yarn
   ```

5. clone grafana

   ```
   git clone https://github.com/grafana/grafana.git
   ```

   

6. build grafana

   - frontend

   ```
   # open grafana directory
   
   yarn install --pure-lockfile
   yarn start
   ```

   

   - backend  
   grafana root 디렉토리에서 다음 명령어를 실행한다.

   ```
   # make 설치
   sudo apt-get install build-essential
   # or
   # sudo apt install make
   # sudo apt install make-guile
   
   # build
   make run
   ```
   
   `nohup make run &`  
   
   
 7. build grafana to docker image  
      
    `make build-docker-full`  
      
