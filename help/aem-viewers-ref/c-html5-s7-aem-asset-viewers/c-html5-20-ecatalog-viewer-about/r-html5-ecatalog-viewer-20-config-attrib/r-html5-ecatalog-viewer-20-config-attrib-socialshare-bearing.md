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
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|수직 맞춤|측면 맞춤 </span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> up </span>, <span class="codeph"> 아래로 </span>, <span class="codeph"> 왼쪽 </span>, 또는 <span class="codeph"> 오른쪽 </span>로 설정하면 추가 경계 확인 없이 지정된 방향으로 패널이 롤아웃됩니다. 이 동작은 외부 컨테이너에 의해 패널 클리핑이 발생할 수 있습니다. </p> <p>로 설정된 경우 <span class="codeph"> 수직 맞추기 </span>로 지정하는 경우 구성 요소는 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고 해당 기본 위치에서 맨 아래, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 각 시도를 통해 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 위쪽, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p>로 설정된 경우 <span class="codeph"> 적당한 측면 </span>로 지정하는 경우 구성 요소는 fit-vertical 과 유사한 로직을 사용합니다. 하지만, 베이스를 오른쪽 첫 번째 시도 오른쪽, 아래로 그리고 위로 롤아웃 방향으로 이동한 다음, 베이스를 왼쪽으로, 왼쪽, 아래로, 그리고 위로 롤아웃 방향으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8e843b967237426e9a8b3cd0f27b9820}

선택 사항입니다.

## 기본값 {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## 예 {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
