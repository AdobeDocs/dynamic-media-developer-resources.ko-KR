---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 수직/측면/맞춤</span> </p> </td> 
   <td> <p> 드롭다운 패널 모양 방향을 제어합니다. </p> <p>로 설정된 경우 <span class="codeph"> 수직 맞추기</span>로 지정하는 경우 구성 요소는 먼저 기본 패널 위치를 단추 아래로 이동하고 기본 위치에서 오른쪽 또는 왼쪽으로 패널을 롤아웃하려고 합니다. 각 시도를 통해 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 오른쪽 및 왼쪽 방향에서 롤아웃 반복 시도를 시도합니다. </p> <p>로 설정된 경우 <span class="codeph"> 적당한 측면</span>로 지정하는 경우 구성 요소는 유사한 논리를 사용하지만 기본 위치를 오른쪽으로 이동하고 아래로 그리고 롤아웃 방향을 설정합니다. 그리고 나서, 아래쪽으로 그리고 롤아웃 방향을 올려서 베이스를 왼쪽으로 이동합니다. </p> </td> 
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
