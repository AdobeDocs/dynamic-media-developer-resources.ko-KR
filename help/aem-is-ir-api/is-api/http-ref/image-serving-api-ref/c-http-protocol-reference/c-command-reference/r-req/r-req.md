---
description: 요청 유형. 요청 유형을 지정합니다.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# req{#req}

요청 유형. 요청 유형을 지정합니다.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`선택 사항`*]`

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

자세한 설명에 별도로 명시되지 않는 한 서버는 `text` MIME 유형의 응답 `text/plain`. 다음과 같은 많은 요청 유형을 사용하여 응답 유형을 지정할 수 있습니다. `text`, 이는 일반적으로 기본값입니다. `javascript`, `xml`, 또는 `json`. 연결된 응답 MIME 유형은 다음과 같습니다 `text/plain`, `text/javascript`, `text/xml`, 및 `text/javascript`, 각각

별도로 언급되지 않는 한, 응답은 다음 집합으로 포맷됩니다. `name=value` 쌍.

다음을 참조하십시오 [속성](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
