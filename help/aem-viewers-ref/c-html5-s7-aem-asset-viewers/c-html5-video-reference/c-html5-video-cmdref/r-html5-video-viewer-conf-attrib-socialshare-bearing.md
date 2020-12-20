---
description: 비디오 뷰어에 대한 구성 속성입니다.
seo-description: 비디오 뷰어에 대한 구성 속성입니다.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: d7d92d63-a4c2-4bd9-b0fd-fdfd47504a39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

비디오 뷰어에 대한 구성 속성입니다.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤</span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> 왼쪽</span> 또는 <span class="codeph"> 오른쪽</span>으로 설정하면 추가 경계 확인 없이 지정된 방향으로 패널이 롤아웃되며 외부 컨테이너에 의해 패널 클리핑이 발생할 수 있습니다. </p> <p><span class="codeph"> fit-vertical</span>로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고 해당 기본 위치의 아래쪽, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 각 작업을 수행하면 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 맨 위, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p><span class="codeph"> fit-lateral</span>으로 설정하면 구성 요소에도 유사한 로직이 사용됩니다. 하지만 일단 베이스를 오른쪽으로 이동시키고, 오른쪽, 아래로, 위쪽 롤아웃 방향을 시도한 다음, 베이스를 왼쪽으로 이동하고, 왼쪽, 아래쪽, 위쪽 롤아웃 방향을 시도합니다. </p> </td> 
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

