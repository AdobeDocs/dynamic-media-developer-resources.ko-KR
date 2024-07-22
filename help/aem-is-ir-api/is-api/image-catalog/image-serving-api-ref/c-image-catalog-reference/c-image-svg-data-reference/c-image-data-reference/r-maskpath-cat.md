---
description: 마스크 파일 경로. 이 카탈로그 레코드와 연결된 마스크 이미지 파일의 상대 또는 절대 경로 및 이름입니다.
solution: Experience Manager
title: 마스크 경로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# 마스크 경로{#maskpath}

마스크 파일 경로. 이 카탈로그 레코드와 연결된 마스크 이미지 파일의 상대 또는 절대 경로 및 이름입니다.

이미지에 별도의 마스크를 첨부할 수 있습니다.

서버에서 [Source 데이터 관리](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)에 설명된 경로 확인 규칙을 사용하여 데이터 파일을 찾습니다.

## 속성 {#section-cdc3b7e2811e41008479cd97887c01b7}

텍스트 문자열 값입니다. 선택 사항입니다. 지정하면 올바른 상대 또는 절대 이미지 서버 파일 경로여야 합니다. 파일 접미사가 없으면 `attribute::DefaultExt`이(가) 추가됩니다.

기본 이미지(`catalog::Path`)와 마스크 이미지(`catalog::MaskPath`)가 모두 카탈로그 레코드에 정의된 경우 두 이미지 모두 픽셀 크기가 정확히 동일해야 합니다. 마스크 이미지는 8비트 회색 음영이어야 합니다.

요청의 `mask=`이(가) `catalog::MaskPath`을(를) 재정의합니다.

`catalog::MaskPath`은(는) 기본 이미지(`catalog::Path`)의 알파 채널(있는 경우)과 알파 채널의 연결이 해제된 경우(즉, 사전 곱해지지 않은 경우)을 재정의합니다. 이미지 알파를 미리 곱하면 `catalog::MaskPath`이(가) 무시되고 항상 알파 채널이 사용됩니다.

## 기본값 {#section-78533e35bfec469ba087cb68a35bb81b}

없음.

## 참조 {#section-68d262f5949c4959b8723ba44611d1dc}

[특성::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [특성::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [카탈로그::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [마스크=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
