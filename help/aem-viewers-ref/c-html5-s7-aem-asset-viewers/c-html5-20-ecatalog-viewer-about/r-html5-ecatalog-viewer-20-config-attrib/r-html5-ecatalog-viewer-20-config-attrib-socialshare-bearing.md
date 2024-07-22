---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤-측면 </span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> <span class="codeph">(위쪽 </span>, <span class="codeph"> 아래쪽 </span>, <span class="codeph"> 왼쪽 </span> 또는 <span class="codeph"> 오른쪽 </span>)으로 설정하면 패널이 추가 경계 검사 없이 지정된 방향으로 롤아웃됩니다. 이 동작은 외부 컨테이너로 패널 클리핑을 발생시킬 수 있습니다. </p> <p><span class="codeph"> 맞춤-세로 </span>(으)로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고 이러한 기본 위치에서 아래쪽, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 매번 시도할 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 맨 위로 이동하고 맨 위, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복합니다. </p> <p><span class="codeph"> 맞춤-측면 </span>(으)로 설정된 경우 구성 요소는 맞춤-세로와 유사한 논리를 사용합니다. 그러나 베이스를 우측으로 먼저 시도하는 오른쪽, 아래로, 위로 롤아웃 방향으로 이동한 다음 베이스를 왼쪽으로 이동하는 왼쪽, 아래로, 위로 롤아웃 방향을 시도합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8e843b967237426e9a8b3cd0f27b9820}

선택적.

## 기본값 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 예 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
