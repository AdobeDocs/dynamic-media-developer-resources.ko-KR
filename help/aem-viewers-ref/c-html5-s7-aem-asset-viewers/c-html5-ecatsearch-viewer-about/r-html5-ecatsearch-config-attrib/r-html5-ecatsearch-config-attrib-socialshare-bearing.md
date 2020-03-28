---
description: 널
seo-description: 널
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|fit-vertical|fit-portable </span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> 위로, <span class="codeph"> 아래로, </span>왼쪽으로 <span class="codeph"> 또는 </span>오른쪽으로 설정하면, 추가 경계 확인 <span class="codeph"> </span><span class="codeph"> </span>없이 패널이 지정된 방향으로 롤아웃됩니다. 이 동작을 수행하면 외부 컨테이너가 패널 클리핑을 초래할 수 있습니다. </p> <p>세로 <span class="codeph"> </span>맞춤으로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고, 이러한 기본 위치에서 아래쪽, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 각 시도가 있을 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 위쪽으로 이동하고 위쪽, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p>측선에 <span class="codeph"> 맞추도록 설정하면 구성 요소는 수직과 유사한 로직을 </span>사용하지만, 대신 베이스를 오른쪽 첫 번째 시도 오른쪽, 아래쪽 및 위쪽 롤아웃 방향으로 이동한 다음, 왼쪽, 아래쪽 및 위쪽 롤아웃 방향을 시도합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8e843b967237426e9a8b3cd0f27b9820}

선택 사항입니다.

## 기본값 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 예 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
