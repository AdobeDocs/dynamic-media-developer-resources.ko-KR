---
description: 널
seo-description: 널
seo-title: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 없음|슬라이드|페이드 </span></span> </p> </td> 
   <td colname="col2"> <p> 플라이아웃 보기를 표시하거나 숨길 때 적용되는 효과의 유형을 지정합니다. 아무 <span class="codeph"> 것도 없는 </span>경우 플라이아웃 이미지가 활성화되고 준비되면 즉시 표시됩니다.슬라이드 애니메이션이 왼쪽에서 오른쪽 방향으로 재생되도록 <span class="codeph"> </span> 합니다.페이드 <span class="codeph"> 기능은 플라이아웃 이미지에 알파 전환을 </span> 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 쇼타임 </span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시를 완료하는 데 걸리는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 쇼지연 </span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시를 시작하는 사용자 동작과 애니메이션 자체의 표시 시작 사이의 지연 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 숨김을 완료하는 데 걸리는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 히데지연 </span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 숨기기 및 애니메이션 숨기기 시작 사이의 지연 시간(초)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
