---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic media
uuid: 791aaaa5-3777-4f68-a445-caa3d975d883
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> 드롭다운 패널 모양의 방향을 제어합니다. </p> <p><span class="codeph"> fit-vertical</span>로 설정하면 구성 요소가 먼저 기본 패널 위치를 단추 아래쪽으로 이동하고, 패널을 기본 위치에서 오른쪽 또는 왼쪽으로 롤아웃하려고 합니다. 각 작업을 수행하면 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 오른쪽 및 왼쪽 방향으로 롤아웃 시도를 반복하려고 합니다. </p> <p><span class="codeph"> Fit-lateral</span>으로 설정하면 구성 요소에서는 비슷한 논리를 사용하지만 아래쪽으로 롤아웃하여 방향을 오른쪽으로 이동합니다. 그런 다음 밑을 왼쪽으로 옮기고 아래쪽으로 내려가며 방향을 돌립니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 사용자가 유휴 상태일 때 패널을 숨기는 드롭다운 자동 숨기기 타이머에 대한 지연 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-55436ddd78b04f538dbb9a7a8463feae}

선택 사항입니다.

## 기본값 {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## 예 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
