---
description: 기본 문자 서식을 지정하려면 다음 명령을 사용하십시오.
solution: Experience Manager
title: 기본 문자 서식
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d3bd6d4d-d7bd-4c9b-bc9e-7edaaac6378e
TQID: 'https://experienceleague.adobe.com/-QEj-7BWb1yXOLxH25Ay6qBDcMJhI8D6VdHNs0bLgUE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 2%

---

# 기본 문자 서식{#basic-character-formatting}

기본 문자 서식을 지정하려면 다음 명령을 사용하십시오.

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> 명령 </th> 
   <th class="entry"> 설명 </th> 
   <th class="entry"> 주의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \plain </span> </td> 
   <td> <p>문자 서식을 기본값으로 재설정합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>만. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f <span class="varname"> N </span> </span> </td> 
   <td> <p>글꼴. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl </span> 인덱스. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs <span class="varname"> N </span> </span> </td> 
   <td> <p>글꼴 크기입니다. </p> </td> 
   <td> <p>1/2 포인트, 기본값은 24입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf <span class="varname"> N </span> </span> </td> 
   <td> <p>글꼴 색입니다. </p> </td> 
   <td> <p>0 기반 색인을 색상표로 변환. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>대담한 스타일. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>이탤릭체 스타일입니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub </span> </td> 
   <td> <p>아래 첨자 </p> </td> 
   <td> <p>글꼴 크기를 줄입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super </span> </td> 
   <td> <p>위 첨자. </p> </td> 
   <td> <p>글꼴 크기를 줄입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul </span> </td> 
   <td> <p>밑줄. </p> </td> 
   <td> <p>이미지 제공에서는 다음 RTF 밑줄 명령도 인식합니다. </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashed </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave </span> </li> 
     </ul> </p> <p>이러한 기능은 현재 표준 <span class="codeph"> \ul </span> 밑줄로 구현됩니다. 다른 모든 RTF 밑줄 명령은 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone </span> </td> 
   <td> <p>밑줄 끄기 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0 </span> </td> 
   <td> <p>밑줄 끄기 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \caps </span> </td> 
   <td> <p>대문자 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>만. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps </span> </td> 
   <td> <p>소문자("작은 대문자") </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>만. </p> </td> 
  </tr> 
 </tbody> 
</table>
