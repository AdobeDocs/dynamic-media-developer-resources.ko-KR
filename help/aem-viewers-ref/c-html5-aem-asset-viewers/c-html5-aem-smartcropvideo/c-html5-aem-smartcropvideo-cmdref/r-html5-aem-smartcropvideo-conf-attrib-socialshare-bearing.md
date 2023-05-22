---
title: SocialShare.bearing
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|수직 맞춤|가로 맞춤</span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> 위로</span>, <span class="codeph"> 아래로</span>, <span class="codeph"> left</span>, 또는 <span class="codeph"> 오른쪽</span>, 패널은 추가 경계 확인 없이 지정된 방향으로 롤아웃되며, 이로 인해 외부 컨테이너에 의해 패널 클리핑이 발생할 수 있습니다. </p> <p>로 설정된 경우 <span class="codeph"> 세로 맞춤</span>, 구성 요소는 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고, 해당 기본 위치에서 맨 아래, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 매번 시도할 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 맨 위로 이동하려고 하고 상단, 오른쪽 및 왼쪽 방향으로 롤아웃 시도를 반복합니다. </p> <p>로 설정된 경우 <span class="codeph"> 옆면 맞춤</span>, 구성 요소는 유사한 논리를 사용합니다. 그러나 오른쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도하여 베이스를 먼저 오른쪽으로 이동하고 왼쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도하여 베이스를 왼쪽으로 이동합니다. </p> </td> 
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
