---
description: 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.
seo-description: 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> 왼쪽</span> 또는 <span class="codeph"> 오른쪽</span>으로 설정하면 추가 경계 확인 없이 패널이 지정된 방향으로 롤아웃되어 외부 컨테이너에 의해 패널 클리핑됩니다. </p> <p><span class="codeph"> fit-vertical</span>로 설정하면 구성 요소가 먼저 기본 패널 위치를 [즐겨찾기] 메뉴의 아래쪽으로 이동하고 해당 기본 위치에서 다음 방향 중 하나로 패널을 롤아웃하려고 합니다.아래쪽, 오른쪽, 왼쪽. 각 작업을 수행하면 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 맨 위, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p><span class="codeph"> fit-lateral</span>으로 설정하면 구성 요소에도 유사한 로직이 사용됩니다. 기본이 오른쪽으로 이동되고, 오른쪽, 아래로 그리고 위로 롤아웃합니다. 그런 다음 왼쪽, 아래, 위로 방향을 돌려 밑면을 왼쪽으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
