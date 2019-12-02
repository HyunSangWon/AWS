# AWS memo :pencil2:

AWS 서비스를 핵심만 간략하게 정리용도 입니다.

## VPC(Virtual Private Cloud)
- 논리적으로 격리된 사용자 전용 네트워크 구역
- AWS에서는 default VPC를 제공
- VPC는 연결 및 데이터 전송에 비용이 발생, VPC 유지 자체 비용은 청구되지 않는다

## 서브넷
- VPC를 논리적으로 분리한 서브네트워크로 AWS 환경 내의 네트워크 최소 단위
- IGW (AWS 라우터)를 기준으로 Public 서브넷과 Private 서브넷으로 나뉨

## EC2
- AWS상의 가상 서버

## EBS
- 하드디스크 이며 최소 8GB 부터 시작가능
- 디스크는 늘릴 수 있으나 줄일 수는 없다
- EC2에서 분리(Detach)하여 유지하더라도 비용이 청구

## AMI(Amazon Machine Image)
- 즉시 사용이 가능한 상태의 OS 및 패키지 조합
- AWS 이외의 환경에서는 사용할 수 없기 때문에 온프레미스 환경에서는 사용할 수 없음
- AMI 가상화 타입으로 완전가상화인 HVM과 반가상화인 PV가 있고 HVM 성능이 더 좋다

## 보안그룹
- OS 레벨에서 네트워크 통신 필터링 룰을 정하는 것
- 인스턴스 단위로 통신을 제어 해준다
- Black List(특정 IP 포트를 allow)이며 Stateful 이므로 In 트래픽 포트만 명시해줘도 통신이 된다

## NACL
- 서브넷 단위로 통신을 제어 해준다
- White list(특정 IP 포트를 deny) 이고, Stateless 이므로 In/Out 에대한 포트가 정확히 명시되어야한다

## CDN (Amazon CloudFront)
- 응답 속도를 높이거나 웹 서버로의 접속을 줄일 수 있다


