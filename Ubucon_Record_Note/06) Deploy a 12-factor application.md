- Schiano Gregory
- 윤양순
- 13:30~15:00
### Overview
- OCI images
- operate Kubernetes
### Framework
- arm64 등 활용
### 12-factor 정의
패스-참(pass-charm)을 활용하여 12-factor 앱을 Ubuntu에서 구현하는 것은 12-factor 앱의 원칙을 준수하면서 애플리케이션을 배포하고 관리하는 것을 의미합니다. Ubuntu에서는 12-factor 앱을 위한 charms를 제공하며, 이를 통해 환경 변수 관리, 종속성 관리, 데이터베이스 마이그레이션 등 다양한 작업을 자동화할 수 있습니다. 

12-factor 앱이란?

12-factor 앱은 클라우드 환경에서 실행되는 웹 애플리케이션을 위한 일련의 방법론입니다. 주요 원칙은 다음과 같습니다: 

1. **코드베이스:** 한 번의 코드베이스, 여러 배포
2. **종속성:** 명시적으로 선언되고 분리된 종속성
3. **구성:** 환경 변수를 사용하여 구성
4. **백엔드 서비스:** 백엔드 서비스를 연결된 리소스로 취급
5. **빌드, 릴리즈, 실행:** 빌드, 릴리즈, 실행 단계를 엄격히 분리
6. **프로세스:** 무상태 프로세스로 실행
7. **포트 바인딩:** 포트 바인딩을 통해 서비스 제공
8. **동시성:** 수평적으로 확장 가능한 동시성
9. **폐기 가능:** 신속하고 안전한 종료
10. **개발/운영 환경 동등성:** 개발/운영 환경을 최대한 동일하게 유지
11. **로그:** 로그를 이벤트 스트림으로 처리
12. **관리 프로세스:** 관리 작업을 일회성 프로세스로 실행

Ubuntu에서의 12-factor 앱 지원:

Ubuntu에서는 12-factor 앱을 위한 charms를 제공하여 이러한 원칙들을 쉽게 구현할 수 있도록 돕습니다. 특히, [Ubuntu documentation](https://documentation.ubuntu.com/charmcraft/3.4.3/howto/manage-a-12-factor-app-charm/)은 12-factor 앱 charms를 관리하는 방법에 대한 자세한 정보를 제공합니다. 

패스-참 활용 예시:

- **환경 변수 관리:**
    
    12-factor 앱은 환경 변수를 통해 구성을 관리합니다. Ubuntu documentation은 charm 설정 파일 (예: `charmcraft.yaml`)을 사용하여 환경 변수를 정의하고, 이를 통해 애플리케이션에 필요한 설정을 주입할 수 있도록 지원합니다. 예를 들어, 데이터베이스 연결 문자열이나 API 키와 같은 민감한 정보를 환경 변수로 관리할 수 있습니다. 
    
- **종속성 관리:**
    
    12-factor 앱은 명시적인 종속성 선언을 통해 모든 종속성을 엄격하게 관리합니다. [The Twelve-Factor App](https://12factor.net/ko/dependencies)은 이러한 원칙을 설명하며, charm은 필요한 종속성들을 정의하고 관리하는 데 사용될 수 있습니다. 
    
- **데이터베이스 연동:**
    
    12-factor 앱은 데이터베이스를 백엔드 서비스로 취급합니다. [Ubuntu documentation](https://documentation.ubuntu.com/charmcraft/3.5.0/howto/manage-web-app-charms/use-web-app-charm/)은 charms를 사용하여 데이터베이스와 상호작용하는 방법을 제공하며, 예를 들어, 데이터베이스 마이그레이션 작업을 자동화할 수 있습니다. 
    
- **릴리즈 및 배포:**
    
    charm은 애플리케이션의 릴리즈 및 배포 프로세스를 자동화하는 데 사용될 수 있습니다. [Canonical](https://canonical.com/blog/how-we-used-flask-and-12-factor-charms-to-simplify-canonical-com-development)은 [Canonical.com](https://canonical.com/) 및 [Ubuntu.com](https://ubuntu.com/) 개발에 12-factor 앱 charms를 활용하여 배포 프로세스를 단순화한 사례를 소개합니다. 
    

결론:

패스-참을 활용하여 Ubuntu에서 12-factor 앱을 구현하는 것은 애플리케이션의 유연성, 확장성, 유지보수성을 향상시키는 데 도움이 됩니다. Ubuntu의 charm 프레임워크를 통해 12-factor 앱의 원칙을 쉽게 준수하고, 복잡한 배포 및 관리 작업을 자동화할 수 있습니다.
### Juju, Charmcraft, Rockcraft and 12-factor
#### juju
- OSO(Open Source Orchestration)
	- deployment
	- integration
	- lifecycle management of applications in the cloud using special software operators called 'charms'
	- AWS -> 쿠버네티스 -> Juju -> Google Cloud
##### Concepts
- Model
- Integration/Relation
- Offer
#### Charmcraft
#### Rockcraft
#### Observability
- generate, recorded as logs, metrics, and traces
#### COS
- Canonical Observability Stack
#### 12-factor principles
- setup automation
- minimize production
	- configuration difference
#### support
- Django
- FastAPI
- Go
- Flask
- ExpressJS
- SpringBoot

- 프레임 워크에 따라 적용을 달리 및 기회 제공함
### 실습 - django 기준
- 원하는 프레임 워크를 찾은 후 브랜치별로 따라가기
- 아마 git clone을 하면 브랜치를 switching 하면서 할 수 있을거임 ㅇㅇ
``` bash
cd django-hello-world
```
![[Pasted image 20250810135316.png]]
![[Pasted image 20250810135359.png]]
#### 01) multipass 설치
``` bash
multipass shell ubucon-workshop
```
#### 02) first Rock using Rockcraft
- 각 브랜치별로 진행 - Flask면 Flask tkdyd
#### charm using Rock craft
- requires에서 postgreSQL 부분만 주석 해제 후 실행
![[Pasted image 20250810142610.png]]

``` bash
find-offers
switch postgres
juju status
switch cursed-forest
wget tar 파일
```
- https://github.com/canonical/paas-charm-workshop/tree/flask-03-deploy

- agent initialising
	- live나 workload
		- if blocked 되있다면 postgre 받고 와서 다시 active되는 것을 볼 수 있음
		- relate postgresql-k8s
	- application 자체는 준비가 되있고, setup에 맞춰서 잉글레스를 붙여줘야 함
	- 8.번의 export Service_HOSTNAME 어쩌고를 넣어서 라우터 설정이라던가 그런걸 다 설정할 수 있음
	- ![[Pasted image 20250810143859.png]]
- teraform deploy 시에 다 될거임
- health 했을 때 okay 뜨면 되는거긴 한데
``` bash
curl http://mock-arces.ubuntu.lan/fibonacchi/21
```