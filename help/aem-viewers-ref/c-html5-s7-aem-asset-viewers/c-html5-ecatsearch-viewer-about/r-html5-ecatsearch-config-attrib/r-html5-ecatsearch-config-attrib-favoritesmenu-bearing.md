---
description: 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.
solution: Experience Manager
title: FavoritesMenu.being
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
TQID: 'https://experienceleague.adobe.com/Pe9frhI8cmIorx5zE-cdC-frEP77UOksMwyM9PvUCdo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# FavoritesMenu.being{#favoritesmenu-bearing}

단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤-측면</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> 또는 <span class="codeph"> right</span>(으)로 설정된 경우 패널은 추가 경계 확인 없이 지정된 방향으로 롤아웃되며, 이로 인해 외부 컨테이너에 의해 패널 클립이 발생합니다. </p> <p><span class="codeph"> 맞춤-세로</span>(으)로 설정하면 구성 요소가 먼저 기본 패널 위치를 즐겨찾기 메뉴의 맨 아래로 이동하고 기본 위치에서 다음 방향 중 하나로 패널을 롤아웃하려고 합니다(아래, 오른쪽, 왼쪽). 각 시도마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 위쪽으로 이동하려고 하고 위, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복합니다. </p> <p><span class="codeph"> 맞춤-측면</span>(으)로 설정된 경우 구성 요소는 유사한 논리를 사용합니다. 베이스가 먼저 오른쪽으로 이동하며 오른쪽, 아래쪽, 위로 롤아웃 방향을 시도합니다. 그런 다음 베이스를 왼쪽으로 이동하여 왼쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
