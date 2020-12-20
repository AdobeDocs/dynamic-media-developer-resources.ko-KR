---
description: MetadataField/type, saveMetadataFieldParam/fieldType 및 createMetadataField/fieldType에서 사용됩니다.
seo-description: MetadataField/type, saveMetadataFieldParam/fieldType 및 createMetadataField/fieldType에서 사용됩니다.
seo-title: 메타데이터 필드 유형
solution: Experience Manager
title: 메타데이터 필드 유형
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# 메타데이터 필드 유형{#metadata-field-types}

MetadataField/type, saveMetadataFieldParam/fieldType 및 createMetadataField/fieldType에서 사용됩니다.

구문

## 값 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:값 및 [!DNL `SingleFixedTag`] 으로 초기화된 수정할 수 없는 사전의 특수  [!DNL `True`] 경우입니다 [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:닫힌 사전에서 문자열 값이 0개 이상 있습니다. 관리 사용자만 사전을 수정할 수 있습니다.
* [!DNL `MultiTag`]:문자열 값이 0개 이상 있습니다.
* [!DNL `SingleFixedTag`]:닫힌 사전의 단일 문자열 값입니다. 사전에 없는 값으로 `setAssetMetadata` 또는 `batchSetAssetMetadata`을(를) 호출하면 오류가 반환됩니다. 관리 사용자만 사전을 수정할 수 있습니다.

* [!DNL `SingleTag`]:단일 문자열 값입니다.
* [!DNL `String`]

