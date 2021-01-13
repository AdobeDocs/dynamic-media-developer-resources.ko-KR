---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
topic: Dynamic media
uuid: 0dcebbce-f449-4f5f-acbc-02960e1dbdba
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>구성 요소 미리 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>으로 설정하면 구성 요소가 유휴 상태일 때 모든 캐러셀 프레임을 미리 로드합니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 구성 요소는 현재 볼 수 있는 프레임, 이전 프레임 및 다음 프레임만 로드합니다. </p> <p><span class="codeph"><span class="varname"> 프리로딩 </span></span>nbrbrandroid는 유휴 상태일 때 현재 표시된 프레임 주위에 있는 보이지 않는 프레임의 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
