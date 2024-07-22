---
title: SocialShare.bearing
description: Video360 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f00b2539-3159-487a-b0fa-9589b694c2e6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

Video360 뷰어에 대한 구성 속성입니다.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤-측면</span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> 또는 <span class="codeph"> right</span>(으)로 설정된 경우 패널은 추가 경계 검사 없이 지정된 방향으로 롤아웃되며, 이로 인해 외부 컨테이너에 의해 패널 클립이 발생할 수 있습니다. </p> <p><span class="codeph"> 맞춤-세로</span>(으)로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고 해당 기본 위치에서 맨 아래, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 매번 시도할 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 맨 위로 이동하려고 하고 상단, 오른쪽 및 왼쪽 방향으로 롤아웃 시도를 반복합니다. </p> <p><span class="codeph"> 맞춤-측면</span>(으)로 설정된 경우 구성 요소는 유사한 논리를 사용합니다. 그러나 오른쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도하여 베이스를 먼저 오른쪽으로 이동하고 왼쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도하여 베이스를 왼쪽으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
