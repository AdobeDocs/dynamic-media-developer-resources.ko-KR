---
description: saveToFile=의 루트 경로입니다. req=saveToFile을 사용하여 생성된 이미지를 작성해야 하는 루트 폴더의 상대 경로입니다.
seo-description: saveToFile=의 루트 경로입니다. req=saveToFile을 사용하여 생성된 이미지를 작성해야 하는 루트 폴더의 상대 경로입니다.
seo-title: SavePath
solution: Experience Manager
title: SavePath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# SavePath{#savepath}

saveToFile=의 루트 경로입니다. req=saveToFile을 사용하여 생성된 이미지를 작성해야 하는 루트 폴더의 상대 경로입니다.

`SavePath` 은 텍스트 문자열 값입니다.

## 속성 {#section-343d1371e966491c92854a8df14c3c50}

텍스트 문자열. 비어 있거나 유효한 상대 폴더 경로여야 합니다. 항상 `ImageServer::SaveDirectory`으로 구성된 절대 루트 경로와 결합합니다.

## 기본값 {#section-ae751eea97654f399c6aaee3f3252cbb}

정의되지 않은 경우 `default::SavePath`에서 상속됩니다. 해결된 값이 비어 있으면 파일에 저장을 사용할 수 없습니다.

## 참조 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
