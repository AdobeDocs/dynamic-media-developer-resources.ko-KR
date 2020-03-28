---
description: 마스크 파일 경로. 이 카탈로그 레코드와 연관된 마스크 이미지 파일의 상대 또는 절대 경로 및 이름입니다.
seo-description: 마스크 파일 경로. 이 카탈로그 레코드와 연관된 마스크 이미지 파일의 상대 또는 절대 경로 및 이름입니다.
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MaskPath{#maskpath}

마스크 파일 경로. 이 카탈로그 레코드와 연관된 마스크 이미지 파일의 상대 또는 절대 경로 및 이름입니다.

이미지에 개별 마스크를 첨부할 수 있습니다.

서버는 소스 데이터 관리에 설명된 경로 [확인](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) 규칙을 사용하여 데이터 파일을 찾습니다.

## 속성 {#section-cdc3b7e2811e41008479cd97887c01b7}

텍스트 문자열 값. 선택 사항입니다. 지정된 경우 올바른 상대 또는 절대 이미지 서버 파일 경로여야 합니다. `attribute::DefaultExt` 에 파일 접미어가 없으면 추가됩니다.

카탈로그 레코드에 기본 이미지( `catalog::Path`)와 마스크 이미지( `catalog::MaskPath`)가 모두 정의된 경우 둘 다 정확히 동일한 픽셀 크기를 가져야 합니다. 마스크 이미지는 8비트 회색 음영이어야 합니다.

`mask=` 를 무시합니다. `catalog::MaskPath`

`catalog::MaskPath` 기본 이미지()의 알파 채널( `catalog::Path`있는 경우)을 재정의하고 알파 채널이 연결되지 않은 경우(즉, 미리 곱하지 않은 경우) 알파 채널을 재정의합니다. 이미지 알파를 미리 곱하면 `catalog::MaskPath` 이 무시되고 알파 채널이 항상 사용됩니다.

## 기본값 {#section-78533e35bfec469ba087cb68a35bb81b}

없음.

## 참조 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)[, req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
