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
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|수직 맞춤|측면 맞춤</span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> 또는 <span class="codeph"> 오른쪽</span>으로 설정하면 추가 경계 확인 없이 패널이 지정된 방향으로 롤아웃되어 패널이 외부 컨테이너에 의해 잘릴 수 있습니다. </p> <p><span class="codeph"> fit-vertical</span> 로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동합니다. 그런 다음 이러한 기본 위치에서 다음 방향 중 하나로 패널을 롤아웃하려고 합니다. 아래쪽, 오른쪽, 왼쪽. 각 시도를 통해 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 위쪽, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복합니다. </p> <p><span class="codeph"> Fit-lateral</span>로 설정하면 구성 요소는 유사한 논리를 사용하지만, 기본 위치를 오른쪽으로 이동하고, 오른쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도합니다. 그런 다음, 기본 부분을 왼쪽으로 이동하고, 왼쪽, 아래로, 위로 롤아웃 방향을 시도합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
