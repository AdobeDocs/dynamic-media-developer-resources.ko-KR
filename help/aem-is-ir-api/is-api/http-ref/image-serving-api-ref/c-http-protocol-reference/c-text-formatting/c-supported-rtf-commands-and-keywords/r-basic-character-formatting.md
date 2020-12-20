---
description: 기본 문자 서식에 다음 명령을 사용합니다.
seo-description: 기본 문자 서식에 다음 명령을 사용합니다.
seo-title: 기본 문자 서식
solution: Experience Manager
title: 기본 문자 서식
topic: Scene7 Image Serving - Image Rendering API
uuid: cc8f276a-ebcc-479b-bd86-7ac0dc755f11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 8%

---


# 기본 문자 서식{#basic-character-formatting}

기본 문자 서식에 다음 명령을 사용합니다.

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
   <td> <span class="codeph"> \일반 </span> </td> 
   <td> <p>문자 서식을 기본값으로 재설정합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴면. </p> </td> 
   <td> <p> <span class="codeph"> \fontbl  </span> 인덱스. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴 크기. </p> </td> 
   <td> <p>반점;기본값은 24입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴 색상. </p> </td> 
   <td> <p>0부터 시작하는 색인을 색상표로 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>굵은 스타일. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>기울임체 스타일입니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub  </span> </td> 
   <td> <p>아래 첨자. </p> </td> 
   <td> <p>글꼴 크기를 줄입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super  </span> </td> 
   <td> <p>위 첨자. </p> </td> 
   <td> <p>글꼴 크기를 줄입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul  </span> </td> 
   <td> <p>밑줄. </p> </td> 
   <td> <p>이미지 제공은 다음 RTF 밑줄 명령도 인식합니다. </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \d  </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uludash  </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb  </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth  </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw  </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave  </span> </li> 
     </ul> </p> <p>현재 표준 <span class="codeph"> \ul </span> 밑줄로 구현됩니다. 다른 모든 RTF 밑줄 명령은 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \url  </span> </td> 
   <td> <p>밑줄 끄기 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0  </span> </td> 
   <td> <p>밑줄 끄기 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \대문자 </span> </td> 
   <td> <p>대문자 </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps  </span> </td> 
   <td> <p>소문자("작은 대문자") </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용. </p> </td> 
  </tr> 
 </tbody> 
</table>

