---
layout: default
title: What is domain name?
parent: Internet
nav_order: 3
---

# What is Domain Name?

## References

[What is a Domain Name? - Learn web development - MDN](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_domain_name)

[What is a domain name? - Domain name vs. URL - Cloudflare](https://www.cloudflare.com/en-gb/learning/dns/glossary/what-is-a-domain-name/)

[What is a Domain Name? - A Beginners Guide to How Domain Names Work!](https://www.youtube.com/watch?v=Y4cRx19nhJk)

## What is domain name?

도메인 이름(Domain Name)은 IP 주소에 대응되는 문자열 주소이다. 도메인 이름은 가독성이 좋은 웹 서버의 주소를 제공한다. 기본적으로 인터넷과 연결된 컴퓨터들에 접근하기 위해서는 공용 IP 주소가 필요하다. IP 주소는 컴퓨터의 입장에서는 인식하기가 쉽지만, 사람의 입장에서는 서버의 IP 주소만으로는 누가 서버를 운영하는지, 웹사이트가 제공하는 서비스는 무엇인지 알기 쉽지 않고, 때문에 기억하기 쉽지 않다. 이를 극복하기 위해서는 가독성이 좋은 웹 주소인 도메인 이름이 필요하다.

## Structure of domain names

도메인 이름은 다음과 같이 여러 개의 요소가 점으로 구분된 간단한 구조를 가지고 있다.

<img width="254" alt="Structure of domain names" src="https://user-images.githubusercontent.com/123535862/228137966-79d88040-190a-4759-8506-0752aa6ce5eb.png">

도메인 이름의 각 요소들은 도메인 이름 전체에 대한 특정한 정보를 내포하고 있다.

### TLD(Top-Level Domain)

TLD는 도메인 이름이 사용되는 일반적인 목적에 대해 알려준다. TLD에는 특수문자와 라틴 문자가 포함될 수 있으며 최대 63자까지 사용할 수 있지만 일반적으로는 2-3자까지 사용한다. 일반적으로 자주 사용되는 TLD들은 (`.com`, `.org`, `.net`과 같은) 이를 사용하는 웹 서비스에 어떠한 기준도 요구하지 않는 것과 반대로, 몇 TLD들은 웹 서비스에 엄격한 기준들을 적용하기 때문에 목적이 매우 명확하다.

예를 들어, 로컬 TLD들의 경우(`.us`, `.fr`, `.se`와 같은) 이를 사용하기 위해서는 웹 서비스가 사용하는 언어와 호스팅된 지역이 제시된 기준에 맞게 설정되어야 한다. `.gov`와 같은 특정 TLD들의 경우는 웹 서비스가 반드시 정부 측에서 운영되어야만 한다. `.edu`와 같은 TLD의 경우는 웹 서비스의 사용 목적이 교육이어야 하며 학술 기관 측에서 운영되어야만 한다.

### Label (or Component)

레이블(Label)은 TLD를 따르는 것이다. 레이블은 A에서 Z까지의 문자, 0에서 9까지의 숫자만 포함하여 사용할 수 있으며 최대 63자까지 사용할 수 있는, 대소문자를 구분하지 않는 문자 시퀀스이다. TLD의 바로 옆에 위치하고 있는 레이블은 특별히 SLD(Secondary Level Domain)라고도 불린다. 도메인 이름에는 많은 레이블이 포함될 수 있으며, SLD를 기준으로 여러 하위 도메인도 생성할 수 있다.

## Who manages domain name

도메인 이름을 소유하는 것은 불가능하다. 즉, 사용되지 않는 도메인 이름은 누군가에 의해 새롭게 재사용될 수 있다. 만약 도메인 이름을 사서 이를 영원히 소유할 수 있다면 웹 상에 존재하는 쓸만한 도메인 이름들은 하나도 없을 것이며 누구도 이를 사용할 수 없을 것이다. 대신에 도메인 등록기관(Registrar)과 일종의 계약을 맺는 것과, 이를 연장하는 것은 가능하다.
