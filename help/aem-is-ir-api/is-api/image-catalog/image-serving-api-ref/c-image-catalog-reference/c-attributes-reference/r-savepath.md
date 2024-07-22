---
description: saveToFile= 의 루트 경로입니다. req=saveToFile로 생성된 이미지를 기록해야 하는 루트 폴더의 상대 경로.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# SavePath{#savepath}

saveToFile= 의 루트 경로입니다. req=saveToFile로 생성된 이미지를 기록해야 하는 루트 폴더의 상대 경로.

`SavePath`은(는) 텍스트 문자열 값입니다.

## 속성 {#section-343d1371e966491c92854a8df14c3c50}

텍스트 문자열입니다. 비어 있거나 유효한 상대 폴더 경로여야 합니다. `ImageServer::SaveDirectory`(으)로 구성된 절대 루트 경로와 항상 결합됩니다.

## 기본값 {#section-ae751eea97654f399c6aaee3f3252cbb}

정의되지 않은 경우 `default::SavePath`에서 상속됩니다. 해결된 값이 비어 있으면 파일에 저장할 수 없습니다.

## 참조 {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
