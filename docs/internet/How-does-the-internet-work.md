---
layout: default
title: How does the internet work?
parent: Internet
nav_order: 2
---

## How does the internet work?

[How does the internet work? (Full Course)](https://www.youtube.com/watch?v=zN8YNNHcaZc)

[How does the Internet Work? - cs.fyi](https://cs.fyi/guide/how-does-internet-work)

[How Does the Internet Work?](http://web.stanford.edu/class/msande91si/www-spr04/readings/week1/InternetWhitepaper.htm)

### Switch & Local Area Network(LAN)

Switch는 서로 다른 여러개의 컴퓨터들이 통신할 수 있게 하는 장치이다. Switch를 통해 컴퓨터들이 통신하기 위해서는 서로 다른 컴퓨터들을 연결하는 케이블(cable)이 필요하다. 케이블의 종류에는 광섬유 케이블은(fiber optic cable)과 구리 케이블(copper cable)이 있으며 광섬유 케이블이 구리 케이블보다 데이터 전송 속도가 빠르다. 참고로, Switch 장치는 반드시 케이블로 연결되어야 하고 따라서 무선(wireless) 기술에는 활용될 수 없다. 무선 통신 기술을 활용하기 위해서는 Access Point 장치가 필요하다. 어찌되었든 핵심은 서로 다른 여러개의 컴퓨터들이 통신하기 위해서는 이들을 각각 연결하는 Switch 장치나 Access Point 장치가 필요하다는 것이다.

Switch 장치로 연결된 컴퓨터들은 network를 형성한다(서로 연결되어 있다). 그리고 컴퓨터들이 서로 통신할 수 있는 이유는 그들이 같은 네트워크 안에 존재하기 때문이다. 공공기관, 학교, 실험실, 대학교, 사무실과 같은 비교적 제한된 범위 안에 형성된 네트워크를 LAN(Local Area Network)이라고 한다. 그리고 사실, 전세계에 걸쳐 형성된 네트워크(인터넷)는 이러한 LAN의 확장판이라고 봐도 무방하다.

실제 Swtich 장치는 Port를 가지고 있으며 이것의 개수는 장치 별로 다양하다. Switch 장치의 Port는 이에 연결된 컴퓨터들이 LAN을 형성하기 때문에 LAN Ports라고 부른다. Switch 장치와 컴퓨터 간의 연결은 LAN Ports와 컴퓨터 사이를 Cable로 연결함으로써 형성된다.

컴퓨터에서 생성된 데이터를 Packet이나 Frame이라고 부른다. Switch 장치는 LAN Port에 케이블로 연결된 하나의 컴퓨터에서 생성 및 전송된 패킷의 내부 정보를 들여다 보고 그것의 목적지를 파악해 해당 목적지에 해당하는 또 다른 컴퓨터로 패킷을 전송함으로써 LAN 통신이 이루어진다. 이처럼 Switch 장치는 서로 다른 여러개의 컴퓨터들이 통신할수 있도록 하는 중간자 역할을 담당한다.

그렇다면 우리가 사용하는 컴퓨터가 단순히 이러한 Switch 장치에 연결하는 것만으로도 어떻게 인터넷이라는 LAN보다 거대한 네트워크에 연결될 수 있는 것일까?

### Router & Internet

LAN 내에서는 switch 장치만 있어도 충분하다. 하지만 인터넷에 연결하기 위해서는 router 장치가 필요하다. router 장치는 switch 장치를 중심으로 형성된 LAN을 넘어 컴퓨터가 인터넷에 연결될 수 있도록 하는 게이트 역할을 한다. switch 장치와 router 장치가 케이블로 연결되고 router 장치가 다시 인터넷에 케이블로 연결되면서 컴퓨터는 인터넷에 연결될 수 있다.

컴퓨터가 인터넷에 패킷을 전달하는 과정은 간략하게 다루자면 다음과 같다. 

1) 컴퓨터가 switch 장치에 패킷을 전달한다. 

2) switch 장치가 패킷을 해석하여 인터넷에 전달되어야 할 것을 파악하고 router 장치에 전달한다. 

3) router 장치가 switch로부터 전달받은 패킷을 해석하고 이를 인터넷에 전달한다. 

이처럼 router 장치는 switch 장치와 인터넷 사이의 매개 역할을 담당함으로써 컴퓨터가 인터넷에 연결할 수 있도록 돕는다. 그렇다면 router를 통해 연결되는 인터넷의 의미는 무엇이며 그것의 동작 방식은 구체적으로 어떻게 될까?

### What does the internet represent?

간단히 설명하자면 인터넷은 router들의 집합체라고 봐도 무방하다. 인터넷에 존재하는 router들은 조직적인 방식으로 전세계에 분산되어 있다. 그리고 앞서 정의했듯이 router는 LAN과 인터넷을 연결하는 매개 역할을 담당함으로, 인터넷은 전세계에 있는 모든 LAN이 연결된 네트워크라고 정의할 수 있다. 인터넷은 네트워크의 네트워크이다. 전세계에 퍼져 있는 LAN들은 인터넷을 통해 서로 연결될 수 있다.

여기서 한가지 의문이 들 수 있다. 왜 인터넷은 하나의 router 장치로 통합되어 간단하게 운용되는 것이 아닌 여러 router 장치를 통해 형성되어 있는 것일까? 첫번째 이유로는 컴퓨터 과학에는 하나의 single point에 의존하면 안된다는 단일 실패 지점 원칙이 있다. 만약 인터넷이 하나의 router 장치로 운용이 된다면, 수억개의 컴퓨터가 하나의 router 장치에 의존하게 된다. 만약 인터넷의 중심에 있는 유일한 router 장치에 결함이 발생하게 된다면 전세계에 있는 모든 컴퓨터의 인터넷 연결이 불가능해지게 된다. (최근 카카오 데이터 센터 화재 사건을 기억하라). 두번째 이유로는 케이블의 길이가 너무 길어지게 된다는 점이 있다. 전세계에 존재하는 router와 중심에 있는 giant router를 연결하려면 해당 케이블의 길이는 상상도 못할 만큼 길어질 것이고 이는 비용적인 측면이나 안정성과 관련된 측면에서 손실이다.

패킷이 인터넷을 거쳐 목적지에 도달하는 과정은 다음과 같다.

1) switch 장치로 패킷이 전달되고 switch 장치는 해당 패킷을 해석하여 목적지가 인터넷을 거쳐 도달해야 함을 파악한다. 인터넷을 거쳐 목적지에 도달해야 하기 때문에 router 장치로 패킷을 전송한다.

2) router로 패킷이 전달되면 router 역시 해당 패킷을 해석하고 목적지를 파악하여 경로 내에 존재하는 router로 패킷을 전달한다. 패킷이 router에서 router로 전달되는 이 시점이 바로 인터넷에 접속되는 순간이며 이 순간에 패킷을 전송하는 router를 key router라고 한다.

3) 인터넷 상에 존재하는 router로 패킷이 전달되면 마찬가지로 패킷을 해석하여 해당 패킷의 목적지를 파악한다. 그런데 인터넷 경로 상에는 무수히 많은 router가 존재하며, 때문에 패킷이 목적지에 도달하기 위해 거쳐야 하는 경로의 가지 수도 무수히 많다. 때문에 인터넷 경로 상에 존재하는 각각의 router들은 패킷이 목적지에 도달하기 위한 최적의 경로를 정해야만 한다. 인터넷 경로 상에 존재하는 각각의 router들은 각각 특별한 프로세서를 가지고 있는데 해당 프로세서는 수많은 알고리즘을 통해 최적의 경로 정보가 들어있는 routing table을 생성하며 이를 참고해 어떤 router로 패킷을 전달해야하는지 결정한다. 이러한 router가 경로를 결정하는 과정을 forwarding이라고 한다. 한번 경로가 결정되면 다른 경로 선택지는 무시되는데 이를 Route Filtering이라고 한다. 추가로 router는 최단 경로로 패킷을 목적지에 전달하는 것이 최우선 순위인 시스템이다. 하지만 실제 세계에서는 트래픽과 같은 문제로, 경로 상으로 보면 가장 빠르지만 실제로는 느릴 수도 있는 경우가 있다. router의 내부 프로세서는 여러 문제들을 전부 고려하여 경로를 결정하며 최단 경로만이 router의 알고리즘의 전부는 아니다.

4) 위의 과정이 반복되며 목적지의 router로 패킷이 전달되고 해당 router는 패킷을 switch 장치로 전달한다.

5) switch 장치는 전달받은 패킷을 목적지인 컴퓨터로 전달한다.

추가로 요즘에는 switch-router 조합 대신 home router를 사용한다. home router는 router와 switch의 역할을 결합한 장치이다. home router는 무선 네트워크를 가능케하는 access point의 기능도 동시에 가지고 있다. home router는 가정에서와 같이 적은 컴퓨터와 연결될 때는 효율적이지만 많은 컴퓨터와 연결될 때 비효율적이다. 하나의 환경에서 많은 컴퓨터가 인터넷에 연결되기를 바란다면 앞서 언급했던 switch-router 장치 조합을 사용해 인터넷에 연결하는 것이 효율적이다.

### Wide Area Network(WAN)

Wide Area Network는 두 개 이상의 LAN이 결합되어 있는 범위의 네트워크를 말한다. WAN을 통해 각지에 존재하는 LAN이 하나의 네트워크를 공유할 수 있다. 하지만 알다시피 서로 다른 LAN은 WAN을 형성하지 않고도 인터넷을 통해 서로 연결될 수 있다. 그렇다면 왜 WAN이 필요한 것일까?

인터넷은 public network이기 때문에 모든 이들이 공유할 수 있다. 때문에 정보 전송 과정에서 보안과 관련된 문제들이 발생할 수 있다. 만약 LAN 네트워크 안에서 정보 전송이 이루어진다면 해당 LAN에 접속하기 위해서는 LAN 관리자의 허락이 필요하고 정보를 불법적으로 해킹하려는 사람들은 LAN 네트워크에 접속할 수 없으므로 해당 정보를 빼내기란 불가능하다. 하지만 정보가 LAN을 넘어 인터넷을 거쳐 전송된다면 인터넷은 모두에게 공유되므로 해당 정보를 불법적으로 해킹하는 것이 충분히 가능하다.

WAN을 형성하는 것은 비용이 많이 들고 쉬운 작업이 아니지만 몇가지 비교적으로 비용이 덜 들고 간단한 방식이 존재한다. VPN을 사용하는 방법이다. VPN은 Vritual Private Network의 줄임말이다. 보통 VPN은 제한된 사이트에 접속할 때 주로 사용된다. VPN은 익명성을 보장해주고 패킷을 보내기 전 데이터를 암호화하기 때문에 높은 보안성을 가지고 있다. 

VPN의 보안성과 관련하여 주목해야 할 기능은 tunneling이라는 기술이다. tunneling은 인터넷 위에 특별한 네트워크 연결을 형성하여 privacy와 security, anonymity를 제공한다. tunneling 기능은 패킷의 보안성이 매우 높기 때문에 패킷이 견고한 직선의 터널을 통해 전송되는 것처럼 보이게 한다. 즉, 패킷의 출발 지점에 있는 router와 도착 지점에 있는 router가 높은 보안성을 가진 터널로 연결이 구축되어 있는 형태를 가진다. 형태적으로는 높은 보안성을 가진 터널을 통과하는 것처럼 보이지만 tunneling을 통한 패킷 역시 인터넷에 있는 수 많은 router들을 거친다. 하지만 tunneling 기술을 통해 전송되는 패킷은 또 다른 패킷으로 이중으로 감싸지고 그 안에 저장되어 존재하는 패킷은 암호화되어 있기 때문에 외부에서 가로채는 것이 어려울 뿐더러 가로채더라도 이를 해석하는 것이 매우 어렵다. 때문에 높은 보안성을 가진 터널을 지나는 것처럼 패킷이 전송되는 것이다. 이처럼 라우터와 라우터 사이 tunneling을 활용해 형성된 연결을 site to site VPN이라고 한다. 이는 WAN을 형성하는 가장 대표적인 방식이다.

### Switch VS Router

서로 다른 LAN의 switch와 switch의 port를 케이블로 연결하는 방식으로도 LAN을 형성할 수 있다. 그리고 이런 형식으로 형성된 LAN을 Campus Area Network(CAN)이라고 부른다. 또한 서로 다른 LAN의 router와 router 사이에 tunneling을 구축함으로써 VPN 방식으로 WAN을 형성할 수도 있다.

LAN(또는 CAN)은 언제나 VPN으로 구축한 WAN보다 높은 보안성을 가지고 있다. 왜냐하면 LAN은 인터넷과 다르게 공유되지 않는 네트워크이고 독립적인 케이블을 통해서만 연결될 수 있기 때문이다. 패킷에 접근 자체가 불가능하다면 인터넷 위에 구축되어 접근은 가능한 VPN으로 구축한 WAN보다는 보안성이 높을 수 밖에 없다. 인터넷 위에 tunneling으로 구축된 WAN의 경우를 public WAN이라고 부른다. 하지만 router와 router 사이를 케이블로 연결하여 보안성의 수준이 LAN과 비슷한 WAN을 형성할 수도 있는 이를 private WAN이라고 한다. 하지만 private WAN의 경우 ISP 케이블을 구매하고 이를 연결하는 과정에 비용이 많이 들기 때문에 대부분의 회사들은 public WAN을 선호한다.

LAN을 형성하는데에는 switch 장치를 사용하고 WAN을 형성하는데에는 router 장치를 사용한다. 이 말은 전통적인 switch 장치를 활용하여 WAN을 형성할 수 없다는 말이다. WAN은 기본적으로 서로 다른 LAN이 동일한 네트워크를 공유하는 범위를 뜻한다. switch 장치를 통해 형성된 LAN이 다른 지역의 네트워크를 공유하고 싶다면 앞서 말했듯이 router 장치가 필요하다. router 장치는 대부분 인터넷과 연결될 때 주로 사용되지만, 사실 그보다 더 본질적인 목적과 기능은 다른 네트워크와 연결되는 데 있다.

### Internet Service Provider(ISP)

ISP는 인터넷 서비스를 제공하는 영리 목적의 기업을 칭한다. 세계에는 수많은 ISP 기업들이 있다. 우리가 ISP를 통해 인터넷에 접속하기 위해서 가장 먼저 해야할 일은 local ISP에 접속하는 것이다. local ISP는 ISP 중 가장 작은 범위(마을 단위)의 연결을 담당한다. 해당 범위 내의 연결은 하나의 router 장치만으로도 충분하다. 추가로 router 장치를 관리하는 곳을 point of presence(POP)라고 부른다.

local ISP 여럿은 다시 regional ISP로 연결된다. local ISP가 마을의 연결을 책임졌다면 regional ISP는 도시 단위의 연결을 책임진다. 마을 안에서의 연결은 local ISP만 거치면 됐지만 서로 다른 도시와의 연결을 위해서는 regional ISP를 거쳐야 한다. 한 국가의 network는 수많은 loacl ISP와 regional ISP의 결합으로 이루어진다. 국가 내에서의 연결은 local ISP와 regional ISP로 충분하지만 국가와 국가를 넘어서는 network를 위해서는 Global ISP가 필요하다. 

### Connecting to the internet from a computer’s perspective

컴퓨터가 인터넷에 연결된다는 것은 컴퓨터가 router 기능과 인터넷을 통해 원하는 곳에 패킷을 전송할 수 있고 또 패킷을 전송 받을 수 있는 상태를 의미한다. 만약에 우리가 유튜브에 업로드되어 있는 어떤 비디오를 클릭(요청)한다면 컴퓨터는 router를 통해 해당 비디오를 요청(request)하는 패킷을 인터넷을 거쳐 해당 비디오가 저장되어 있는 서버에 전송한다. 그리고 인터넷을 거쳐 도착한 요청 패킷을 서버가 해석해 이에 대한 응답(response) 패킷(요청한 비디오)을 인터넷과 router를 거쳐 컴퓨터로 전송한다. 

**Where to Begin? Internet Addresses**

인터넷에 연결되어 있는 컴퓨터들은 반드시 고유한 주소를 가지고 있어야 한다. 인터넷 주소는 nnn.nnn.nnn.nnn의 형태로 되어있으며 ‘nnn’에 해당되는 부분은 0-255까지의 자연수로 이루어진다. 이러한 인터넷 주소를 IP 주소라고 하며 이때 IP는 Internet Protocol의 약자이다. 

<img width="436" alt="스크린샷 2023-03-20 오후 4 59 13" src="https://user-images.githubusercontent.com/123535862/226279753-a9a8d013-de90-45b1-b83f-2561821487c3.png">


위 그림은 두 개의 컴퓨터가 인터넷에 연결되어 있는 모습을 묘사한다. 1.2.3.4의 IP 주소를 가진 컴퓨터는 인터넷을 통해 5.6.7.8의 IP 주소를 가진 컴퓨터에 연결될 수 있다. 

ISP(Internet Service Provider)를 통해 인터넷에 연결되면 연결된 컴퓨터들은 ISP로부터 유효기간 동안만 유효한 고유의 IP 주소가 발급된다. 만약 컴퓨터가 LAN에 연결되어 있고 이로부터 인터넷에 연결되고자 한다면 DHCP(Dynamic Host Configuration Protocol) 서버로부터 IP 주소를 발급받게 된다. 어찌되었든 인터넷에 연결되기 위해서는 반드시 IP 주소가 필요하다.

**Protocol Stacks and Packets**

컴퓨터에 IP 주소가 부여되었고 인터넷에 연결되면 통신이 가능해진다. 이때 이 ‘통신’은 어떤 방식으로 이루어질까? 인터넷 통신은 기본적으로 유선 통신이다. 즉, 1.2.3.4의 IP 주소를 가진 컴퓨터가 인터넷을 통해 5.6.7.8의 IP 주소를 가진 컴퓨터에 ‘Hello’ 라는 메시지를 전송한다고 치면 해당 메시지는 전선을 통해 전송된다. 때문에 ‘Hello’라는 메시지는 반드시 전기 신호로 변환되어 전송되어야하고, 이후 전송된 전기 신호는 다시 ‘Hello’라는 메시지로 변환되어야 한다. 이러한 과정은 Protocol Stack을 통해 자세히 설명할 수 있다. Protocol Stack은 다음과 같은 요소로 이루어져 있다.

| Protocol Layer | Comments |
| --- | --- |
| Application Protocols Layer | 웹 브라우저, 이메일, FTP와 같은 애플리케이션 단계에서의 프로토콜 |
| Transmission Control Protocol Layer | 포트 번호를 통해 패킷을 특정 애플리케이션으로 전송하는 역할을 담당 |
| Internet Protocol Layer | IP 주소를 통해 패킷을 특정 컴퓨터로 전송하는 역할을 담당 |
| Hardware Layer | 이진수 패킷을 변환하는 역할을 담당 |

그리고 다음과 같은 도식처럼 인터넷 통신이 이루어진다.

<img width="513" alt="스크린샷 2023-03-20 오후 5 00 32" src="https://user-images.githubusercontent.com/123535862/226279918-2be5f625-319a-4902-b3fa-0d45cf57fb2e.png">

1. 1.2.3.4 컴퓨터가 메신저(Application)를 통해 ‘Hello’라는 메시지의 전송 버튼을 누른다.
2. ‘Hello’라는 메시지는 몇개의 덩어리로 쪼개진다. 이를 패킷이라고 한다.
3. TCP Layer에서는 몇개의 덩어리로 쪼개진 각각의 패킷들에 포트 번호가 새겨진다.
4. IP Layer에서는 몇개의 덩어리로 쪼개진 각각의 패킷들에 IP 주소가 새겨진다.
5. 패킷이 포트 번호와 IP 주소를 가지게 되면 인터넷을 통해 5.6.7.8 컴퓨터에 전송될 준비가 완료된 것이다. 패킷의 준비가 완료되면 Hardware Layer에서는 패킷을 전기 신호로 변환해 전송한다.
6. 변환된 전기신호는 인터넷 내에 존재하는 router 장치들을 거쳐 5.6.7.8 컴퓨터에 전송된다.
7. 전기신호는 Hardware Layer에서 패킷으로 변환된다.
8. IP → TCP Layer의 순으로 패킷의 IP 주소와 포트 번호가 제거된다.
9. Application Layer에서는 패킷을 ‘Hello’라는 메시지의 형태로 결합한다.

**Transmission Control Protocol**

TCP는 Application에서 이루어진 전송을 목적지의 컴퓨터의 정확한 Application에 도달할 수 있도록 하는 프로토콜이다. 그리고 이를 가능하게 하는 것이 바로 포트 번호이다. 같은 컴퓨터에서 쿠팡 쇼핑을 하며 동시에 카톡을 읽을 수도 있는 것이 바로 이 때문이다. 쿠팡과 카톡은 서로 다른 포트 번호를 가지고 있기 때문에 설령 IP 주소가 같아 서로 다른 Application의 패킷이 동시에 하나의 컴퓨터에 전송되더라도 각자의 Application에 도달할 수 있다. 한마디로 정리하자면 TCP Layer는 포트 번호를 통해 패킷이 도달해야할 Application을 결정하는 Layer라고 볼수 있다.

TCP의 동작방식을 조금 더 자세히 설명해보도록 하자. 데이터를 전송하는 입장에서는 TCP가 Application으로부터 데이터를 전달받는다. 그러면 TCP는  해당 데이터를 관리 가능하도록 패킷으로 쪼개고 각각의 패킷에 TCP 헤더를 추가한다. TCP 헤더의 주요 내용은 해당 패킷이 전송되어야 하는 Application의 포트 번호이다. 역으로 데이터를 전달받는 입장에서 TCP는 IP로부터 패킷을 전달받는다. 그러면 TCP는 TCP 헤더를 제거하고 패킷을 데이터로 결합하여 Application으로 전달한다.

추가로 TCP는 단순한 textual 프로토콜이 아니다. TCP는 연결지향적이고, 신뢰가능한, 그리고 바이트 서비스이다. TCP를 사용하는 두 Application은 서로 데이터를 교환하기 전에 먼저 서로 연결이 되어있는 상태이어야만한다. 또한 TCP는 데이터가 손상, 손실, 복제되지 않았음과 패킷이 올바른 순서대로 전달되었음을 보장하기에 Application은 따로 소프트웨어에 통신 보호 장치를 구축하지 않아도 된다. 

한가지 유의할 것은 TCP 헤더에는 IP 주소가 있지 않다는 것이다. 앞서 잠깐 말했듯이 IP 주소는 IP단계에서 처리되어 삭제된다. 무엇보다 TCP는 올바른 Application을 찾아가는 역할만 담당하기에 IP 주소가 필요가 없다. IP 주소와 관련된 작업, 즉 올바른 컴퓨터를 찾아가는 작업은 IP Layer에서 담당한다.

**Internet Protocol**

TCP와 다르게 IP는 신뢰성이 없고, 연결지향적이지 않은 프로토콜이다. IP는 패킷이 Application에 온전하게 전달되었는지를 책임지지 않을 뿐만 아니라 패킷의 순서도 보장하지 않는다. 거기다 당연히 IP는 연결 및 포트 번호에 대해 알지 못한다. IP는 패킷이 올바른 컴퓨터를 찾아가는 작업만을 담당한다. IP와 TCP의 유일한 공통점은 데이터를 수신할 때와 데이터 전송 시 패킷에 IP 헤더를 제거 및 추가한다는 점 뿐이다. 

데이터 전송시에 Application Layer에서 출발한 데이터는 IP Layer를 거치게 되면 IP header와 TCP header를 가진 패킷의 형태를 가지게 된다. 이처럼 IP 주소와 포트 번호를 가진 패킷은 ‘socket’이 구비된 전송가능한 패킷이 된다.

<img width="602" alt="스크린샷 2023-03-20 오후 5 01 18" src="https://user-images.githubusercontent.com/123535862/226280055-d58acccf-5843-412c-a97b-285117089ad1.png">

