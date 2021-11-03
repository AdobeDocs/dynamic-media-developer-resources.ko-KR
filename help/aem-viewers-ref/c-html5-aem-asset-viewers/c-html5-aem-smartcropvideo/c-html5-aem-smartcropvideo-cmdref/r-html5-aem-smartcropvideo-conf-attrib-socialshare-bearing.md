---
description: 스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

스마트 자르기 비디오 뷰어에 대한 구성 속성입니다.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|수직 맞춤|측면 맞춤</span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> up</span>, <span class="codeph"> 아래로</span>, <span class="codeph"> 왼쪽</span>, 또는 <span class="codeph"> 오른쪽</span>로 설정하면 패널은 추가 경계 확인 없이 지정된 방향으로 롤아웃되므로 외부 컨테이너에 의해 패널 클리핑이 발생할 수 있습니다. </p> <p>로 설정된 경우 <span class="codeph"> 수직 맞추기</span>로 지정하는 경우 구성 요소는 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고 해당 기본 위치에서 아래쪽, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 매번 시도할 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 맨 위, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p>로 설정된 경우 <span class="codeph"> 적당한 측면</span>로 지정하는 경우 구성 요소는 유사한 논리를 사용합니다. 하지만 첫 번째, 오른쪽, 다운 및 롤아웃 방향을 시도하면서 베이스를 오른쪽으로 이동한 다음, 왼쪽, 다운 및 롤아웃 방향을 따라 베이스를 왼쪽으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
