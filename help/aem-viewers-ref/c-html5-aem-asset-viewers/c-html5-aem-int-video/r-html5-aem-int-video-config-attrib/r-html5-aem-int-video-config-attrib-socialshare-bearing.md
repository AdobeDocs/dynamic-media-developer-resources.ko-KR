---
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤</span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> 왼쪽</span> 또는 <span class="codeph"> 오른쪽</span>으로 설정하면 추가 경계 확인 없이 패널이 지정된 방향으로 롤아웃되어 외부 컨테이너가 패널을 클리핑할 수 있습니다. </p> <p><span class="codeph"> fit-vertical</span>로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고 이러한 기본 위치의 다음 방향 중 하나로 패널을 롤아웃하려고 합니다.아래쪽, 오른쪽, 왼쪽. 각 작업을 수행하면 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 상단, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p><span class="codeph"> fit-lateral</span>으로 설정하면 구성 요소에서는 비슷한 논리를 사용하지만, 기준을 오른쪽으로 이동하여 오른쪽, 아래쪽 및 위쪽 롤아웃 방향을 테스트합니다. 그런 다음, 왼쪽, 아래 그리고 위쪽 롤아웃 방향을 시도하면서 베이스를 왼쪽으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

