---
title: FavoritesMenu.bearing
description: 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|수직 맞춤|측면 맞춤</span> </p> </td> 
   <td colname="col2"> <p> 로 설정된 경우 <span class="codeph"> up</span>, <span class="codeph"> 아래로</span>, <span class="codeph"> 왼쪽</span>, 또는 <span class="codeph"> 오른쪽</span>로 설정하면 패널은 추가 경계 확인 없이 지정된 방향으로 롤아웃되므로 외부 컨테이너에 의해 패널이 클리핑됩니다. </p> <p>로 설정된 경우 <span class="codeph"> 수직 맞추기</span>를 지정하면 구성 요소가 먼저 기본 패널 위치를 즐겨찾기 메뉴 아래로 이동합니다. 패널은 이러한 기본 위치에서 다음 방향 중 하나로 롤아웃하려고 합니다. 아래쪽, 오른쪽, 왼쪽. 각 시도를 통해 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 맨 위, 오른쪽 및 왼쪽 방향에서 반복 롤아웃을 시도합니다. </p> <p>로 설정된 경우 <span class="codeph"> 적당한 측면</span>로 지정하는 경우 구성 요소는 유사한 논리를 사용합니다. 베이스는 오른쪽, 오른쪽, 아래로, 위로 롤아웃하여 오른쪽으로 이동됩니다. 그리고 나서, 기지들을 왼쪽으로, 아래로 그리고 위로 롤아웃하는 방향으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
