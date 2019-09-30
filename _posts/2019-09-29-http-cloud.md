---
title: "Cloud IaaS-SaaS-PaaS"
excerpt: "IaaS-SaaS-PaaS"
categories: 
  - http
comments: true
date: 2019-09-29
# last_modified_at: 2019-08-12T19:37:00+09:00
tag: 
    - http
    - iaas
    - saas
    - paas
---

# IaaS-SaaS-PaaS란

- IaaS (Infrastructure as a service)

IaaS는 가장 쉽게 정의할 수 있다. 업체에 상관없이 거의 동일한 개념으로 사용된다. IaaS는 서드파티 업체가 제공하는 고도로 자동화되고 확장 가능한 IT 인프라를 의미한다. 이 인프라에는 스토리지, 호스팅, 컴퓨팅, 네트워킹 등이 포함된다. 비용은 사용한 만큼만 지급하면 된다. 기업은 IaaS를 통해 소프트웨어 라이선스와 서버 등 IT 자산을 직접 소유하는 대신 필요에 따라 이들 리소스를 유연하게 대여할 수 있다.

가트너에 따르면, 2016년 기준 IaaS 시장 규모는 250억 달러에 달한다. 2018년에는 450억 달러까지 늘어날 것으로 전망된다. 현재 이 시장을 장악하고 있는 업체는 2006년부터 클라우드 서비스를 제공해 온 AWS다. 시너지 리서치가 2017년 2월에 내놓은 보고서를 보면, AWS의 시장 점유율은 40%에 달한다. 마이크로소프트와 구글, IBM 등이 이 시장에서 AWS와 경쟁하고 있지만 이들 업체의 점유율을 모두 합해도 23%에 불과하다.

단, 마이크로소프트의 행보는 눈여겨 볼만하다. '클라우드 퍼스트'를 주창한 사타야 나델라 CEO의 진두지휘 속에 전 세계에서 방대한 규모의 자체 클라우드 네트워크를 구축했고 이를 기반으로 빠르게 점유율을 끌어올리고 있다. 거대 인터넷 기업인 구글은 GCP(Google Cloud Platform)라는 브랜드로 퍼블릭 클라우드 서비스와 IaaS 사업을 확대하고 있다.

- PaaS (Platform as a service)

PaaS는 가장 정의하기 까다로운 클라우드 모델이다. 기본 개념은 모든 기본 IaaS는 물론 개발 툴과 기능, 애플리케이션 배포 등을 안전하게 제공하는 것이다. 미들웨어와 데이터베이스 관리, 애널리틱스 혹은 운영체제 등이 포함된다. PaaS는 개발자가 애플리케이션을 개발하고 배포하는 데 필요한 모든 것을 제공해야 한다. PaaS를 이용하면 개발자는 기반 인프라스트럭처를 전혀 프로비저닝할 필요가 없다.

PaaS는 방대한 영역의 기능을 제공해야 하기 때문에 PaaS 업체는 주로 대형 IT 기업이다. 구글 앱 엔진(Google App Engine), 오라클 클라우드 플랫폼(Oracle Cloud Platform), 피보탈의 클라우드 파운드리(Cloud Foundry), 세일즈포스 히로쿠(Heroku) 등이다.

PaaS의 기반이 되는 인프라스트럭처는 제공하는 PaaS에 따라 차이가 있다. 예를 들어 오라클과 AWS는 사용자가 자사 인프라에서 작업하도록 유도하지만 다른 업체들은 이에 대해 비교적 관대하다. SAP 클라우드 플랫폼의 경우 AWS와 애저, GCP 클라우드 인프라스트럭처에서 모두 사용할 수 있다. 레드햇의 오픈시프트(OpenShift) 역시 SAP와 비슷하다.

- SaaS (Software as a service)

SaaS는 서드파티가 호스팅 방식으로 소프트웨어를 제공하는 것이다. 일반적으로 웹을 통해 접속해 로그인하기만 하면 사용할 수 있다. 사용자 혹은 시트(seat)를 기준으로 구독 방식으로 과금되는 것이 보통이다. SaaS는 머신 혹은 서버를 기준으로 소프트웨어 라이선스를 구매해 직접 설치해 사용하던 기존 구매 방식과 차별화된다.

SaaS는 이메일이나 CRM(customer relationship management) 소프트웨어 등에서 널리 사용되고 있다. 지메일이나 구글 독스 혹은 드롭박스 같은 클라우드 파일 스토리지를 사용해 봤다면 이미 SaaS를 경험한 것이다. SaaS 업체는 다양하다. 오피스를 웹 기반 오피스 365로 전환한 마이크로소프트를 비롯해, SaaS CRM 솔루션을 시장을 개척한 세일즈포스 같은 기업용 소프트웨어 업체도 있다. 클라우드 기반 HR 소프트웨어를 제공하는 워크데이(Workday)도 주요 SaaS 업체 중 하나다.

내용 출처 : http://www.ciokorea.com/news/37345#csidx274c37f4546200c8ba747644cf89679 



### 추가 정보

- 하이퍼바이저란

하이퍼바이저란 컴퓨터의 운영 체제와 응용프로그램을 물리적 하드웨어에서 분리하는 프로세스를 말한다. 주로 소프트웨어처럼 실행되지만 임베디드된(embedded) 하이퍼바이저를 모바일 기기용으로 만들 수도 있다. 하이퍼바이저는 물리적인 호스트 시스템이 여러 대의 가상 머신을 게스트로 운영할 수 있게 해, 메모리, 네트워크 대역폭, CPU 등과 같은 컴퓨팅 자원을 더 효과적으로 사용할 수 있도록 도와준다.

출처 : http://www.ciokorea.com/insider/36713#csidx15e1fafadaaf79c8603d62abce2a3d9 

- 가상화란

가상화는 단일한 물리 하드웨어 시스템에서 여러 시뮬레이션 환경이나 전용 리소스를 생성할 수 있는 기술입니다. 하이퍼바이저라 불리는 소프트웨어가 하드웨어에 직접 연결되며 1개의 시스템을 VM(가상 머신)이라는 별도의 고유하고 안전한 환경으로 분할할 수 있습니다. 이러한 VM은 하이퍼바이저의 기능을 사용하여 머신의 리소스를 하드웨어에서 분리한 후 적절하게 배포합니다.

- 클라우드 컴퓨팅이란

클라우드 컴퓨팅은 네트워크 전체에서 컴퓨팅, 네트워크, 스토리지 인프라 리소스, 서비스, 플랫폼, 애플리케이션을 사용자에게 온디맨드로 제공하는 원칙이자 접근 방식입니다. 이러한 인프라 리소스, 서비스, 애플리케이션은 클라우드, 즉 관리와 자동화 소프트웨어를 통해 오케스트레이션되는 가상 리소스 풀에서 소싱되므로 사용자는 자동 스케일링과 동적 리소스 할당이 지원되는 셀프 서비스 포털을 통해 온디맨드로 클라우드에 액세스할 수 있습니다.