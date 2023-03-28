---
layout: default
title: What is DNS? and How DNS works?
parent: Internet
nav_order: 4
---

# What is DNS? and How DNS works?

## References

[What is DNS? - How DNS works - Cloudflare](https://www.cloudflare.com/en-gb/learning/dns/what-is-dns/)

[DNS - MDN Web Docs Glossary: Definitions of Web-related terms - MDN](https://developer.mozilla.org/en-US/docs/Glossary/DNS)

## What is DNS?

**DNS(Domain Name System)**은 인터넷 상의 전화번호부와 같다. 우리가 웹 사이트에 접속할 때, 주로 도메인 이름을 통해 접속하지만 사실 웹 브라우저는 IP(Internet Protocol) 주소를 통해 상호작용한다. DNS는 도메인 이름을 IP 주소로 변환하여 웹 브라우저가 인터넷 리소스를 로드할 수 있도록 돕는다.

## DNS Component

DNS가 도메인 이름을 IP 주소로 변환하는 과정은 대부분 사용자 인터페이스 뒤편에서 일어나기 때문에 이를 이해하기 위해서는 DNS 쿼리가 거쳐야 하는 다양한 하드웨어 구성요소를 알아야 한다.

| DNS Recursive Resolver | 재귀 DNS 확인자는 도서관에서 책을 찾아주는 사서에 비유될 수 있다. DNS 리커서는 클라이언트로부터 도메인 이름을 수신하고 이에 대한 추가적인 요청을 서버로 송신한다. |
| --- | --- |
| DNS Root Nameserver | 루트 서버는 도서관 책꽂이의 색인(index)에 비유될 수 있다. DNS 레코드에 대한 참조다. |
| DNS TLD Nameserver | TLD 서버는 도서관의 책꽂이에 비유될 수 있다. 도메인 이름의 TLD 파트를 호스팅한다. |
| Authoritative Nameserver | 권한 있는 DNS 서버는 책에 비유될 수 있다. 해당 서버에는 DNS 레코드가 저장되어 있다. |

**재귀 DNS 확인자(DNS Recursive Resolver)**는 클라이언트로부터 받은 요청에 최종적으로 응답하고, 그 과정에서 DNS 레코드를 추적하기 위해 여러 서버들과 일련의 쿼리를 진행한다. 재귀 DNS 확인자는 DNS 레코드를 찾기 위해 다수의 요청을 매번 생성할 필요가 없다. 캐싱을 통해 이러한 과정들이 생략될 수 있기 때문이다.

<img width="756" alt="1-DNS Record Request Sequence" src="https://user-images.githubusercontent.com/123535862/228177798-f9eb1aad-e2e9-4335-ba4a-b342076e602d.png">

**권한 있는 DNS 서버(Authoritative Nameserver)**는 실제 DNS 레코드가 저장되어 있는 서버이다. 해당 서버는 DNS 파이프라인의 제일 끝단에 위치해있으며, DNS 쿼리를 IP 주소로 변환한다. 권한 있는 DNS 서버는 DNS 레코드를 찾기 위한 추가적인 데이터가 필요하지 않은 최종 서버이다. 참고로 DNS 쿼리에 서브 도메인이 포함될 경우 권한 있는 DNS 서버가 추가적으로 필요할 수도 있다.  

<img width="766" alt="2-CNAME DNS Record Request Sequence" src="https://user-images.githubusercontent.com/123535862/228177868-3efdb04a-e8ad-4064-8951-450209870025.png">

## How DNS work?

결과적으로 대부분의 상황에서 DNS는 도메인 이름을 IP 주소로 변환하는 일을 수행한다. 그리고 이러한 과정을 DNS 조회(lookup)라고 한다. DNS 조회 프로세스는 총 8가지 단계를 거친다.

| 1 | 사용자가 웹 브라우저의 주소창에 도메인 이름을 입력하고 재귀 DNS 확인자에게 전달된다. |
| --- | --- |
| 2 | 재귀 DNS 확인자가 루트 서버에 질의한다. |
| 3 | 루트 서버가 도메인 이름의 TLD에 해당하는 TLD 서버의 주소를 재귀 DNS 확인자에게 전달한다.  |
| 4 | 재귀 DNS 확인자가 TLD 서버에 질의한다. |
| 5 | TLD 서버는 도메인 이름 전체에 해당하는 도메인 서버의 주소를 재귀 DNS 확인자에게 전달한다. |
| 6 | 재귀 DNS 확인자가 도메인 서버에 질의한다. |
| 7 | 도메인 서버는 IP 주소를 재귀 DNS 확인자에게 전달한다. |
| 8 | 재귀 DNS 확인자가 IP 주소를 웹 브라우정에 전달한다. |

DNS 조회 8단계 프로세스를 거쳐 IP 주소가 반환되면 다음과 같은 과정을 거친다.

| 9 | 브라우저가 IP주소 HTTP 요청을 보낸다. |
| --- | --- |
| 10 | 해당 IP의 서버가 브라우저에 웹 페이지를 반환한다. |

<img width="405" alt="DNS lookup process" src="https://user-images.githubusercontent.com/123535862/228177926-acacc002-cf6f-41c0-bb25-8f762eede14b.png">
