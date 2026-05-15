---
description: 요청 유형. 요청 유형을 지정합니다.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
TQID: 'https://experienceleague.adobe.com/-WzHmELeamQBbVFlzXNKbDE3fKVXw4x6pSoEz0LHav4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 8%

---

# req{#req}

요청 유형. 요청 유형을 지정합니다.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`옵션`*]`

* [catalogprops](r-catalogprops.md)
* [존재](r-exists.md)
* [imageprops](r-imageprops.md)
* [이미지 집합](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [맵](r-map-req.md)
* [마스크](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [메시지](r-message.md)
* [props](r-props.md)
* [해결](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [설정](r-set.md)
* [목표](r-targets.md)
* [tmb](r-tmb.md)
* [사용자 데이터](r-userdata.md)
* [유효성 확인](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

자세한 설명에 별도로 명시되지 않는 한 서버는 MIME 유형이 `text/plain`인 `text` 응답을 반환합니다. 일반적으로 기본값인 `text`, `javascript`, `xml` 또는 `json`과(와) 같은 많은 요청 유형을 사용하여 응답 유형을 지정할 수 있습니다. 연결된 응답 MIME 형식은 각각 `text/plain`, `text/javascript`, `text/xml` 및 `text/javascript`입니다.

별도로 명시하지 않는 한 응답은 `name=value`쌍 집합으로 포맷됩니다.

[속성](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)을 참조하세요.
