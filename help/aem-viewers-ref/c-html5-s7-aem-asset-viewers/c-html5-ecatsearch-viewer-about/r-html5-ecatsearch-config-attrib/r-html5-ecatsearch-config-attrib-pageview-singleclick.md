---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정 </span> </p> </td> 
   <td colname="col2"> <p> 한 번 클릭/누르기로 확대/축소하는 동작의 매핑을 구성합니다. <span class="codeph"> 없음 </span>(으)로 설정하면 한 번 클릭/탭 확대/축소가 비활성화됩니다. <span class="codeph"> 확대/축소로 설정된 경우 </span> 이미지를 클릭하면 1단계 확대되고, Ctrl 키를 누른 상태에서 클릭하면 1단계 축소됩니다. <span class="codeph"> 재설정 </span>(으)로 설정하면 이미지를 한 번 클릭할 때 확대/축소가 초기 확대/축소 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 확대/축소 비율이 지정된 제한에 도달하거나 초과할 경우 재설정이 적용되며 그렇지 않으면 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-edcfcd6c0bd24ac093442c56450b3c97}

선택적.

## 기본값 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

데스크톱 컴퓨터에서는 [!DNL `zoomReset`]이고, 터치 장치에서는 [!DNL `none`]입니다.

## 예 {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
