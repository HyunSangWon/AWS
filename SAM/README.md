# AWS SAM :pencil2:

## What is SAM?
- AWS Serverless Application Model (AWS SAM)는 오픈 소스 프레임워크
- 서버리스 애플리케이션 은(는) Lambda 기능, 이벤트 소스 및 기타 리소스를 사용하여 작업을 수행
- 쉽게 설명하여 Lambda 디버깅, 관리가 가능함 

## SAM 사용방법 (python, sam, docker가 설치 되어 있어야 한다.)
- python 설치
- pip install --user aws-sam-cli (SAM 설치)
- docker 설치 (window 경우 WSL2 설치)  (https://www.docker.com/products/docker-desktop)
- docker window 설치 전 WSL2 설치 방법 (https://www.44bits.io/ko/post/wsl2-install-and-basic-usage)

## SAM 명령어
1. SAM 구성
- sam init --runtime python3.8 --name my-sls-app
2. 일회성 호출 만들기
 2-1. 이벤트 없이
 - sam local invoke "HelloWorldFunction" --no-event
 2-2. 이벤트 넣어서
 - sam local invoke "HelloWorldFunction" -e events/event.json
3. 디플로이 파일 만들고 s3에 업로드 
- sam package --template-file template.yaml --output-template-file deploy.yaml --s3-bucket-버킷이름