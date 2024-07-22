---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정 </span> </p> </td> 
   <td colname="col2"> <p> 두 번 클릭/누르기로 확대/축소하는 동작의 매핑을 구성합니다. <span class="codeph"> 없음 </span>(으)로 설정하면 두 번 클릭/탭 확대/축소가 비활성화됩니다. <span class="codeph"> 확대/축소로 설정된 경우 </span> 이미지를 클릭하면 1단계 확대되고, Ctrl 키를 누른 상태에서 클릭하면 1단계 축소됩니다. <span class="codeph"> 재설정 </span>(으)로 설정하면 이미지를 한 번 클릭할 때 확대/축소가 초기 확대/축소 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 확대/축소 비율이 지정된 제한에 도달하거나 초과할 경우 재설정이 적용되며 그렇지 않으면 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

선택적.

## 기본값 {#section-814d6bc6a0834005a0a72c7040e45693}

데스크톱 컴퓨터에서는 `reset`이고, 터치 장치에서는 `zoomReset`입니다.

## 예 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
