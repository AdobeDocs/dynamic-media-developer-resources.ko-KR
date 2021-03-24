---
description: 색상을 기반으로 이미지를 자동으로 자르는 옵션
solution: Experience Manager
title: AutoColorCropOptions
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 9%

---


# AutoColorCropOptions{#autocolorcropoptions}

색상을 기반으로 이미지를 자동으로 자르는 옵션

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
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> [자동 자르기 모퉁이]를 선택합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 허용치</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">색상 일치 사양. 사용: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">색상을 정확하게 일치시키기 위해 0을 설정합니다. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 - 색상 차이가 가장 많이 나는 것을 활성화합니다. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

