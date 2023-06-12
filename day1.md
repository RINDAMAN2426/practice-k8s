## day 1

### k8s 실습하기

Issue 1. Container creating 상태에서 stuck

- describe를 통해서 원인분석
- 원인은 flannel 설정이 제대로 안되는 부분이 있는 것으로 추정됨

해결 방법
- host path와 container path에 대한 마운트 설정을 cluster config에 추가로 정의해주어야한다
- 참고링크 https://routemyip.com/posts/k8s/setup/flannel/
- 또한 CNI plugin 세팅도 필요함 https://github.com/containernetworking/plugins
- 이거말고도 kind로 하는 경우 pod network cidrs 설정을 수정해야한다는데 도무지안됨
