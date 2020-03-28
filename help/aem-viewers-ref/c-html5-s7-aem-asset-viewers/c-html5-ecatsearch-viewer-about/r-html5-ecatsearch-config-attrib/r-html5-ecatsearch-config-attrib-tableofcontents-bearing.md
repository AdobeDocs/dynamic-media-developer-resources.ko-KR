---
description: 널
seo-description: 널
seo-title: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic media
uuid: 832ebacf-d57f-4efa-ab1a-6a454f7c7a32
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-horizontally|fit-vertical</span> </p> </td> 
   <td> <p> 드롭다운 패널 모양의 방향을 제어합니다. </p> <p>세로에 <span class="codeph"> 맞게</span>설정하면 구성 요소가 먼저 기본 패널 위치를 단추 아래쪽으로 이동하고 기본 위치에서 오른쪽 또는 왼쪽으로 패널을 롤아웃하려고 합니다. 시도할 때마다 구성 요소는 패널이 외부 컨테이너에 의해 잘렸는지 확인합니다. 모든 시도가 실패하면 구성 요소는 기본 패널 위치를 맨 위로 이동하고 오른쪽 및 왼쪽 방향에서 롤아웃 시도를 반복하려고 합니다. </p> <p>수평으로 <span class="codeph"></span>설정하면 구성 요소는 유사한 로직을 사용하지만, 아래쪽으로 롤아웃 방향을 시도하면서 베이스를 오른쪽으로 이동합니다. 그런 다음 밑을 왼쪽으로 이동하고 아래쪽으로 롤아웃합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 사용자가 유휴 상태일 때 패널을 숨기는 드롭다운 자동 숨기기 타이머의 지연 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-55436ddd78b04f538dbb9a7a8463feae}

선택 사항입니다.

## 기본값 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 예 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
