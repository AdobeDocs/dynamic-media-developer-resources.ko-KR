---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소재설정 </span> </p> </td> 
   <td colname="col2"> <p> 확대/축소 작업을 위한 단일 클릭/탭 매핑을 구성합니다. 설정 대상 <span class="codeph"> 없음 </span> 단일 클릭/탭 확대/축소를 비활성화합니다. 로 설정된 경우 <span class="codeph"> 확대/축소 </span> 이미지를 한 확대/축소 단계로 확대/축소합니다. Ctrl 키를 누른 상태에서 클릭하여 한 확대/축소 단계를 축소합니다. 설정 대상 <span class="codeph"> 재설정 </span> 이미지를 한 번 클릭하면 확대/축소가 초기 확대/축소 수준으로 재설정됩니다. 대상 <span class="codeph"> zoomReset </span>, 현재 확대/축소 비율이 지정된 제한 이상인 경우 재설정이 적용되고, 그렇지 않은 경우 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-edcfcd6c0bd24ac093442c56450b3c97}

선택 사항입니다.

## 기본값 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` 데스크톱 컴퓨터에서 `none` 터치 장치

## 예 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
