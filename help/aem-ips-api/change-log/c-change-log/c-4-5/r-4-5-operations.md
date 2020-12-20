---
description: IPS API 버전 4.5의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-description: IPS API 버전 4.5의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.
seo-title: 작업 새로 만들기 및 수정됨
solution: Experience Manager
title: 작업 새로 만들기 및 수정됨
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# 작업:새로 만들기 및 수정됨{#operations-new-and-modified}

IPS API 버전 4.5의 새 작업 방법 및 변경된 작업 방법에 대해 설명합니다.

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

## 수정한 작업 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` 포함 `animatedGifInfo`,  `swcInfo`,  `cssInfo`및  `javascriptInfo` 매개 변수

* `createMetadataField` 선택적 매개 변수를  `isHidden` 포함합니다.

* `saveMetadataField` 선택적 매개 변수를  `isHidden` 포함합니다.

* `searchAssets`
* 
* `renameFiles` 매개 변수는 이전 릴리스에 대해 더 이상 사용되지 않으며 `renameAsset` 작업에서 제거되었습니다. 실제 파일 경로는 영향을 받지 않지만, 새 자산 이름과 일치하도록(파일 확장명 유지) 가상 파일 경로가 변경됩니다. API 클라이언트는 새 API 버전으로 업데이트할 때 이 매개 변수에 대한 참조를 제거해야 합니다.

