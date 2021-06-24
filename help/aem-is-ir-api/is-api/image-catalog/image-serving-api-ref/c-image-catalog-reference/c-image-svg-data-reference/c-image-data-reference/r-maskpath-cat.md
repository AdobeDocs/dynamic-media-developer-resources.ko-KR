---
description: 마스크 파일 경로입니다. 이 카탈로그 레코드와 연결된 마스크 이미지 파일의 상대 또는 절대 경로 및 이름입니다.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# MaskPath{#maskpath}

마스크 파일 경로입니다. 이 카탈로그 레코드와 연결된 마스크 이미지 파일의 상대 또는 절대 경로 및 이름입니다.

이미지에 별도의 마스크를 첨부할 수 있습니다.

서버는 [소스 데이터 관리](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)에 설명된 경로 확인 규칙을 사용하여 데이터 파일을 찾습니다.

## 속성 {#section-cdc3b7e2811e41008479cd97887c01b7}

텍스트 문자열 값입니다. 선택 사항입니다. 지정한 경우 유효한 상대 또는 절대 이미지 서버 파일 경로여야 합니다. `attribute::DefaultExt` 파일 접미사가 없으면 이 추가됩니다.

카탈로그 레코드에 기본 이미지( `catalog::Path`)와 마스크 이미지( `catalog::MaskPath`)가 모두 정의된 경우 둘 다 동일한 픽셀 크기가 있어야 합니다. 마스크 이미지는 8비트 회색조여야 합니다.

`mask=` 요청에서 을 무시합니다  `catalog::MaskPath`.

`catalog::MaskPath` 기본 이미지(  `catalog::Path`)에서 알파 채널이 있고, 있는 경우, 알파 채널이 연결 해제된 경우(예: 사전 곱해지지 않음) 을 무시합니다. 이미지 알파를 미리 곱하면 `catalog::MaskPath` 은 무시되고 알파 채널은 항상 사용됩니다.

## 기본값 {#section-78533e35bfec469ba087cb68a35bb81b}

없음.

## 참조 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
