---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 맞춤-측면|맞춤-수직</span> </p> </td> 
   <td> <p> 드롭다운 패널 모양 방향을 제어합니다. </p> <p><span class="codeph"> 맞춤-세로</span>(으)로 설정하면 구성 요소가 먼저 기본 패널 위치를 단추의 아래쪽으로 이동하고 기본 위치에서 오른쪽 또는 왼쪽으로 패널을 롤아웃하려고 합니다. 각 시도마다 구성 요소는 패널이 외부 컨테이너에 의해 잘리는지 확인합니다. 모든 시도가 실패하면 구성 요소는 베이스 패널 위치를 위쪽으로 이동하려고 하며 오른쪽 및 왼쪽 방향으로 롤아웃 시도를 반복합니다. </p> <p><span class="codeph"> 맞춤-측면</span>(으)로 설정된 경우 구성 요소는 유사한 논리를 사용하지만 아래를 오른쪽으로 먼저 이동하고 위로 롤아웃 방향을 시도합니다. 그런 다음 베이스를 왼쪽으로 이동하여 아래위로 롤아웃 방향을 시도합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 사용자가 유휴 상태일 때 패널을 숨기는 드롭다운 자동 숨기기 타이머의 지연 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-55436ddd78b04f538dbb9a7a8463feae}

선택적.

## 기본값 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 예 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
