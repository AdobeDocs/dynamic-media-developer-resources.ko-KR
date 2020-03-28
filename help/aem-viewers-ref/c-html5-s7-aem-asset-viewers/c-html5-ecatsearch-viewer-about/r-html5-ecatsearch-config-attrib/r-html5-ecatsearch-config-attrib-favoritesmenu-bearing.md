---
description: 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.
seo-description: 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: c3f415ad-f976-464a-9067-a5d526908352
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|fit-vertical|fit-portable</span> </p> </td> 
   <td colname="col2"> <p> 위로 <span class="codeph"> ,</span>아래로 <span class="codeph"> ,</span>왼쪽 <span class="codeph"> 또는 오른쪽으로</span><span class="codeph"></span>설정하면 추가 경계 확인 없이 지정된 방향으로 패널이 롤아웃되며, 이로 인해 패널은 외부 컨테이너에 의해 클리핑됩니다. </p> <p>세로에 <span class="codeph"> 맞게</span>설정하면 구성 요소가 먼저 기본 패널 위치를 즐겨찾기 메뉴 아래쪽으로 이동하고 이러한 기본 위치의 다음 방향 중 하나로 패널을 롤아웃하려고 합니다.하단, 오른쪽, 왼쪽 시도할 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 위쪽, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p>측면 <span class="codeph"> 맞춤으로</span>설정하면 구성 요소에도 비슷한 논리가 사용됩니다. 베이스가 오른쪽, 오른쪽, 아래쪽, 위쪽 롤아웃 방향으로 이동합니다. 그런 다음, 왼쪽, 아래, 위로 롤아웃하여 밑을 왼쪽으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
