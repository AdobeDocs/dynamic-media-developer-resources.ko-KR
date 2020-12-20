---
description: 요청 유형. 요청 유형을 지정합니다.
seo-description: 요청 유형. 요청 유형을 지정합니다.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 9%

---


# req{#req}

요청 유형. 요청 유형을 지정합니다.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`선택 사항`*]`

* [카탈로그 속성](r-catalogprops.md)
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
* [userdata](r-userdata.md)
* [유효성 확인](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

자세한 설명에 달리 명시되어 있지 않는 한, 서버는 MIME 유형이 `text/plain`인 `text` 응답을 반환합니다. 많은 요청 유형을 사용하여 일반적으로 기본값인 `text`, `xml` 또는 `json`과 같은 응답 유형을 지정할 수 있습니다. `javascript` 연결된 응답 MIME 유형은 각각 `text/plain`, `text/javascript`, `text/xml` 및 `text/javascript`입니다.

별도의 언급이 없는 한 응답은 응답의 형식을 `name=value` 쌍 집합으로 지정합니다.

[속성](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)을 참조하십시오.
