---
description: 색상을 기반으로 이미지를 자동으로 자르는 옵션입니다.
solution: Experience Manager
title: 자동 색상 자르기 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 29d3dcfe-fddb-4806-b2aa-b96e9bbcff98
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 9%

---

# 자동 색상 자르기 옵션{#autocolorcropoptions}

색상을 기반으로 이미지를 자동으로 자르는 옵션입니다.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 모퉁이</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 자동 자르기 모서리 선택. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 허용</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">색상 일치 사양입니다. 사용: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0을 입력하여 색상을 정확하게 일치시킵니다. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1을 클릭하여 가장 큰 색상 차이를 활성화합니다. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
