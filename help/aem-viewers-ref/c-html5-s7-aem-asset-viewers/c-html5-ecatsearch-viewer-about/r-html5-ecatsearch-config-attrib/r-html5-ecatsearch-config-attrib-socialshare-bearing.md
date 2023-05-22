---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|수직 맞춤|가로 맞춤 </span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> 위로 </span>, <span class="codeph"> 아래로 </span>, <span class="codeph"> left </span>, 또는 <span class="codeph"> 오른쪽 </span>, 패널은 추가 경계 확인 없이 지정된 방향으로 롤아웃됩니다. 이 동작은 외부 컨테이너로 패널 클리핑을 발생시킬 수 있습니다. </p> <p>로 설정된 경우 <span class="codeph"> 세로 맞춤 </span>, 구성 요소는 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고, 이러한 기본 위치에서 아래쪽, 오른쪽 또는 왼쪽 중 하나에서 패널을 롤아웃하려고 합니다. 각 시도마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 맨 위로 이동하고 맨 위, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복합니다. </p> <p>로 설정된 경우 <span class="codeph"> 옆면 맞춤 </span>, 구성 요소는 수직 맞춤 과 유사한 논리를 사용하지만, 대신 오른쪽으로 첫 번째 시도 - 오른쪽, 아래쪽 및 위쪽 롤아웃 방향으로 베이스를 이동시킨 다음, 왼쪽으로 시도 - 아래쪽 및 위쪽 롤아웃 방향으로 베이스를 이동시킵니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8e843b967237426e9a8b3cd0f27b9820}

선택적.

## 기본값 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 예 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
