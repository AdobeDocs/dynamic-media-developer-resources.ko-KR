---
description: IPS API 버전 4.5에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.
solution: Experience Manager
title: 새 작업 및 수정된 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# 작업: 신규 및 수정됨{#operations-new-and-modified}

IPS API 버전 4.5에 대한 새로운 작업 및 변경된 작업 방법에 대해 설명합니다.

구문

## 새 작업 {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## 수정된 작업 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 에는  `animatedGifInfo`,  `swcInfo`,  `cssInfo`및  `javascriptInfo` 매개 변수가 포함됩니다.

* `createMetadataField` 에는 선택적  `isHidden` 매개 변수가 포함되어 있습니다.

* `saveMetadataField` 에는 선택적  `isHidden` 매개 변수가 포함되어 있습니다.

* `searchAssets`
* 
* `renameFiles` 매개 변수는 이전 릴리스에서 더 이상 사용되지 않으며 `renameAsset` 작업에서 제거되었습니다. 가상 파일 경로가 새 자산 이름과 일치하도록(파일 확장명 유지) 변경되지만 실제 파일 경로는 영향을 받지 않습니다. API 클라이언트는 새 API 버전으로 업데이트할 때 이 매개 변수에 대한 참조를 제거해야 합니다.
