---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`기간`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 슬라이드|회전|자동</span> </p> </td> 
   <td colname="col2"> <p> 프레임 변경에 적용되는 효과의 유형을 지정합니다. </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> 슬라이드</span>은(는) 이전 프레임이 보이지 않게 미끄러지고 새 프레임이 보이지 않게 미끄러지는 전환을 활성화합니다. </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> turn</span>을 사용하면 사용자가 네 개의 스프레드 모서리 중 하나를 드래그하여 대화형 페이지 뒤집기를 수행할 수 있는 경우 페이지 뒤집기 효과를 사용할 수 있습니다. </p> <p><span class="codeph"> turn</span>을 사용하면 구성 요소의 모양이 <span class="codeph"> pageturnstyle</span> 한정자로 제어되고 <span class="codeph"> .s7pagedivider</span> CSS 클래스가 무시됩니다. </p> <p>참고:  <p><span class="codeph"> turn</span> 애니메이션은 Motorola Xoom에서 지원되지 않습니다. </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span>은(는) 데스크톱 시스템에서 선반가공 프레임 전환을 설정하고 터치 장치에서 슬라이드 전환을 설정합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 기간</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 슬라이드</span> 또는 <span class="codeph"> 회전</span> 전환 효과의 기간(초)을 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-4d25a3f483834d2b9586fa70270ce6bd}

선택적.

## 기본값 {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## 예 {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
