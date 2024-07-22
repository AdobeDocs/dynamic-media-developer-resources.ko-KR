---
description: 색상에 따라 이미지를 자동으로 자르기 위한 옵션입니다.
solution: Experience Manager
title: 자동 색상 자르기 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 29d3dcfe-fddb-4806-b2aa-b96e9bbcff98
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# [!DNL AutoColorCropOptions]{#autocolorcropoptions}

색상에 따라 이미지를 자동으로 자르기 위한 옵션입니다.

구문

## 매개 변수 {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 모서리</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 자동 자르기 코너 선택. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 허용 한도</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">색상 일치 사양입니다. 사용: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0을 지정하면 색상이 정확하게 일치합니다. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 - 대부분의 색상 차이를 활성화합니다. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
