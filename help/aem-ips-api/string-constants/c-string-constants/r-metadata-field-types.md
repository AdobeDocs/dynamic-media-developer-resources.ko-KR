---
description: MetadataField/type, saveMetadataFieldParam/fieldType 및 createMetadataField/fieldType에서 사용됩니다.
solution: Experience Manager
title: 메타데이터 필드 유형
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# 메타데이터 필드 유형{#metadata-field-types}

MetadataField/type, saveMetadataFieldParam/fieldType 및 createMetadataField/fieldType에서 사용됩니다.

구문

## 값 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: [!DNL `True`] 및 [!DNL `False`] 값으로 초기화된 수정할 수 없는 사전이 있는 [!DNL `SingleFixedTag`]의 특수 사례입니다.

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: 닫힌 사전의 문자열 값이 0개 이상입니다. 관리자만 사전을 수정할 수 있습니다.
* [!DNL `MultiTag`]: 0개 이상의 문자열 값입니다.
* [!DNL `SingleFixedTag`]: 닫힌 사전의 단일 문자열 값입니다. 사전에 없는 값으로 `setAssetMetadata` 또는 `batchSetAssetMetadata`을(를) 호출하면 오류가 반환됩니다. 관리자만 사전을 수정할 수 있습니다.

* [!DNL `SingleTag`]: 단일 문자열 값입니다.
* [!DNL `String`]
