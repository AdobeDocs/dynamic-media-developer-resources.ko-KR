---
title: videoServerUrl
description: 모든 뷰어에 공통되는 매개 변수.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 6%

---

# videoServerUrl{#videoserverurl}

모든 뷰어에 공통되는 매개 변수.

>[!NOTE]
>
>이 명령은 비디오 이미지 뷰어에는 적용되지 않습니다.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 비디오 서버 루트 경로입니다. 지정된 도메인이 없으면 페이지가 제공되는 도메인이 대신 적용됩니다. 표준 URI 경로 해상도가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

선택 사항입니다. 표준 소프트웨어를 서비스 사용으로 사용할 필요는 없습니다.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 예 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
