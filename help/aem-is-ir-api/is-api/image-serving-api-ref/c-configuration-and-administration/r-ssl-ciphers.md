---
description: server.xml의 Connector 태그는 SSL 연결에 대해 선택할 수 있는 암호를 제한하는 phers 속성을 지원합니다.
solution: Experience Manager
title: SSL 암호 정의
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# SSL 암호 정의{#defining-ssl-ciphers}

server.xml의 Connector 태그는 SSL 연결에 대해 선택할 수 있는 암호를 제한하는 phers 속성을 지원합니다.

기본적으로 모든 암호를 사용할 수 있습니다. 목록은 쉼표로 구분되어 있으며 다음 값을 포함할 수 있습니다.

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

값이 잘못된 경우 Tomcat은 모든 단일 암호를 활성화합니다. 따라서 구성 후 외부 도구를 사용하여 실제로 어떤 클립이 사용되는지 확인하는 것이 중요합니다.

예를 들어 다음 구성은 &quot;128비트&quot; 암호화 세트 이상만 활성화합니다.

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
