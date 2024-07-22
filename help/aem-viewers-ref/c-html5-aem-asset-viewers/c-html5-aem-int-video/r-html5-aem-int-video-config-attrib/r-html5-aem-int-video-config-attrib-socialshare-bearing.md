---
title: SocialShare.bearing
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤-측면</span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> 또는 <span class="codeph"> right</span>(으)로 설정된 경우 패널은 추가적인 경계 검사 없이 지정된 방향으로 롤아웃되며, 이로 인해 패널이 외부 컨테이너에 의해 잘릴 수 있습니다. </p> <p><span class="codeph"> 맞춤-세로</span>(으)로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동합니다. 그런 다음 이러한 기본 위치에서 다음 방향 중 하나로 패널을 롤아웃하려고 합니다. 아래, 오른쪽, 왼쪽 매번 시도할 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 맨 위로 이동하려고 하고 상단, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복합니다. </p> <p><span class="codeph"> fit-lateral</span>(으)로 설정된 경우 구성 요소에서 유사한 논리를 사용하지만 오른쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도하면서 기본을 먼저 오른쪽으로 이동합니다. 그런 다음 베이스를 왼쪽으로 이동하여 왼쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
