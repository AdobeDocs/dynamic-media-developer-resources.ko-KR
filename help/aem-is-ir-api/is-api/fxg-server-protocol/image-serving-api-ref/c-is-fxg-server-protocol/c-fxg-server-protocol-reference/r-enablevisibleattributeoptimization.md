---
description: FXG의 최적화를 활성화합니다.
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

FXG의 최적화를 활성화합니다.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

이 FXG를 전달하는 동안 FXG에서 가시성이 false로 설정된 요소를 제거하여 FXG의 처리 시간을 줄입니다. FXG의 다른 요소에는 영향을 주지 않는 false로 표시되는 요소만 제거됩니다. 예를 들어 다음에 텍스트가 있는 경우 `Path` 및 의 가시성 `Path` 가 false로 설정된 경우 텍스트를 이 경로에 그려야 하므로 이 수정자가 활성화된 경우에도 FXG에서 제거되지 않습니다.

기본값은 1입니다.
