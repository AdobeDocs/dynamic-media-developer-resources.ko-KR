---
description: MetadataField/type, saveMetadataFieldParam/fieldType 및 createMetadataField/fieldType에서 사용됩니다.
solution: Experience Manager
title: 메타데이터 필드 유형
feature: Dynamic Media Classic,SDK/API,메타데이터
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# 메타데이터 필드 유형{#metadata-field-types}

MetadataField/type, saveMetadataFieldParam/fieldType 및 createMetadataField/fieldType에서 사용됩니다.

구문

## 값 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: 값  [!DNL `SingleFixedTag`] 및 값으로 초기화된 수정할 수 없는 사전의 특수  [!DNL `True`] 사례입니다  [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: 닫힌 사전에서 문자열 값이 0개 이상 있습니다. 관리자만 사전을 수정할 수 있습니다.
* [!DNL `MultiTag`]: 문자열 값이 0개 이상 있습니다.
* [!DNL `SingleFixedTag`]: 닫힌 사전의 단일 문자열 값입니다. 사전에 없는 값으로 `setAssetMetadata` 또는 `batchSetAssetMetadata`을 호출하면 오류가 반환됩니다. 관리자만 사전을 수정할 수 있습니다.

* [!DNL `SingleTag`]: 모든 단일 문자열 값.
* [!DNL `String`]
