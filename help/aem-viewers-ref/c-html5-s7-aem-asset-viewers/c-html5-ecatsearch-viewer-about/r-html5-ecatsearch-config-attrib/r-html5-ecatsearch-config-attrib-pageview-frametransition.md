---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,Business Practitioner
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`지속 시간`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 슬라이드|회전|자동</span> </p> </td> 
   <td colname="col2"> <p> 프레임 변경에 적용되는 효과 유형을 지정합니다. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> </span> 이전 프레임이 보기에서 슬라이딩되고 새 프레임이 슬라이딩되어 표시되는 전환을 슬라이딩합니다. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> </span> 뒤집기를 사용하면 사용자가 4개의 스프레드 모서리 중 하나를 드래그하고 대화형 페이지 뒤집기를 수행할 수 있는 경우 페이지 뒤집기 효과를 사용할 수 있습니다. </p> <p><span class="codeph"> turn</span>을 사용하면 구성 요소의 모양이 <span class="codeph"> pageurnstyle</span> 한정자로 제어되고 <span class="codeph"> .s7pagedivider</span> CSS 클래스가 무시됩니다. </p> <p>참고:  <p><span class="codeph"> </span> turnanimation은 Motorola Xoom에서 지원되지 않습니다. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> </span> 는 데스크톱 시스템에서 턴 프레임 전환을 자동화하고 터치 장치에서 슬라이드 전환을 자동화합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 지속 시간</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 슬라이드</span> 또는 <span class="codeph"> turn</span> 전환 효과의 지속 시간을 초 단위로 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-4d25a3f483834d2b9586fa70270ce6bd}

선택 사항입니다.

## 기본값 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 예 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
