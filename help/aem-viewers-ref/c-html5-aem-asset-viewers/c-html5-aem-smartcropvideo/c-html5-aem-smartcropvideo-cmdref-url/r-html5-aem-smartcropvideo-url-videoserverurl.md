---
title: videoServerUrl
description: 스마트 자르기 비디오 뷰어에 대한 URL 명령입니다.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9bd37d2c-c7ec-4f58-8328-45c0a156f330
TQID: 'https://experienceleague.adobe.com/9OQU4jury7TJFsaZrzBQYETRKCR1N5BGbKa18HFovfQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

스마트 자르기 비디오 뷰어에 대한 URL 명령입니다.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 비디오 서버 루트 경로입니다. 지정된 도메인이 없으면 대신 페이지가 제공되는 도메인이 적용됩니다. 표준 URI 경로 확인이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적. 표준 SaaS 사용에는 필요하지 않습니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
