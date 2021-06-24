---
description: 요청 유형. 요청 유형을 지정합니다.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 9%

---

# req{#req}

요청 유형. 요청 유형을 지정합니다.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`선택 사항`*]`

* [catalygprops](r-catalogprops.md)
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

자세한 설명에 별도로 언급되지 않는 한 서버에서 MIME 유형 `text/plain`으로 `text` 응답을 반환합니다. 많은 요청 유형을 사용하면 일반적으로 기본값, `javascript`, `xml` 또는 `json`인 `text` 등의 응답 유형을 지정할 수 있습니다. 연결된 응답 MIME 유형은 각각 `text/plain`, `text/javascript`, `text/xml` 및 `text/javascript`입니다.

별도로 언급되지 않는 한 응답 형식은 `name=value` 쌍 세트로 지정합니다.

[속성](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)을 참조하십시오.
