---
description: SocialShare.베어링
solution: Experience Manager
title: SocialShare.베어링
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
TQID: 'https://experienceleague.adobe.com/YQHHEkxD3goTHedA78xWDI59PaHnM-vOMdjcBa3TNq8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 1%

---

# SocialShare.베어링{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위쪽|아래쪽|왼쪽|오른쪽|맞춤-세로|맞춤-측면 </span> </p> </td> 
   <td colname="col2"> <p> 단추 컨테이너의 슬라이드 애니메이션 방향을 지정합니다. </p> <p> <span class="codeph">(위쪽 </span>, <span class="codeph"> 아래쪽 </span>, <span class="codeph"> 왼쪽 </span> 또는 <span class="codeph"> 오른쪽 </span>)으로 설정하면 패널이 추가 경계 검사 없이 지정된 방향으로 롤아웃됩니다. 이 동작은 외부 컨테이너로 패널 클리핑을 발생시킬 수 있습니다. </p> <p><span class="codeph"> 맞춤-세로 </span>(으)로 설정하면 구성 요소가 먼저 기본 패널 위치를 SocialShare의 맨 아래로 이동하고 이러한 기본 위치에서 아래쪽, 오른쪽 또는 왼쪽에서 패널을 롤아웃하려고 합니다. 각 시도마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 맨 위로 이동하고 맨 위, 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복합니다. </p> <p><span class="codeph"> 맞춤-측면 </span>(으)로 설정된 경우 구성 요소는 맞춤-수직과 유사한 논리를 사용하지만 대신 베이스를 오른쪽으로 첫 번째 시도 오른쪽, 아래로 및 위로 롤아웃 방향으로 이동한 다음 베이스를 왼쪽으로 시도, 아래로 및 위로 롤아웃 방향으로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-8e843b967237426e9a8b3cd0f27b9820}

선택적.

## 기본값 {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## 예 {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
