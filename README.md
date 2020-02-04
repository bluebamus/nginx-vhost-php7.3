# nginx-vhost-php7.3
> nginx와 php7.3 기반으로 가상 호스팅을 Docker와 Docker-compose를 이용해 쉽게 구축할 수 있도록 솔루션을 제공한다.

## 서비스 특징

> shell script를 이용해 nginx와 php의 conf 파일을 도메인마다 독립적으로 만들 수 있도록 제공

> nginx와 php의 모든 config 파일을 Docker-compose의 volumes으로 연동시켜 구동 전, 구동 후에도 

  exec로 컨테이너에 들어가지 않고 제어가 가능함
  
> 단점으로는 상위와 같이 개별적인 conf를 작성하는것을 요구하다보니 독립적인 이미지로 만들기 어려움

  만약 외부와의 연동을 배제하고 독립적인 이미지로 구축하고자 한다면 제공되는 shell script로 conf를 만들고
  
  Docker 파일 혹은 Docker-compose 파일을 수정하여 컨테이너 내부에 복사하거나 스크립트를 수행하도록 만들면 된다.
  
  * 상위 단점에 제안하는 독립적인 Docker 이미지를 구축하는데 필요한 스크립트 및 방법은 따로 제공할 계획이 없다.


## 설치 방법

리눅스: Ubuntu

```sh
docker-compose up -d
```

## 사용 예제

스크린 샷과 코드 예제를 통해 사용 방법을 자세히 설명합니다.
- 업데이트 예정

## 개발 환경 설정

제공되는 shell script를 통해 
통합 시스템을 쉽게 구축할 수 있습니다.

```sh
shell script
```

## 업데이트 내역

* 0.0.1
    * 작업 진행 중

## 멤버

임도현 Owner S/W, H/W, 개발자/기획자

임태연 Member 디자이너/마케터

강동훈 Member S/W, H/W, 개발자/연구원

<!-- Markdown link & img dfn's -->
[npm-image]: https://img.shields.io/npm/v/datadog-metrics.svg?style=flat-square
[npm-url]: https://npmjs.org/package/datadog-metrics
[npm-downloads]: https://img.shields.io/npm/dm/datadog-metrics.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/dbader/node-datadog-metrics/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/dbader/node-datadog-metrics
[wiki]: https://github.com/yourname/yourproject/wiki
