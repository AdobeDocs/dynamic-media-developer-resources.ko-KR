---
description: 널
seo-description: 널
seo-title: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 3c10e625-f789-4454-8898-b3f293aa49b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 이미지가 재설정되고 있는 경우 이미지 상단에 아이콘 효과를 <span class="codeph"></span> 표시할 수 있으며, 이는 이미지와 상호 작용할 수 있는 동작을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 계수</span></span> </p> </td> 
   <td colname="col2"> <p> 아이콘 효과가 <span class="codeph"></span> 표시되고 다시 표시되는 최대 횟수를 지정합니다. 값이 <span class="codeph"> -1</span> 이면 아이콘이 항상 무한히 다시 나타납니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p>애니메이션 표시 또는 숨기기의 지속 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>아이콘 효과가 <span class="codeph"></span> 자동 숨기기 전에 완전히 표시되는 상태로 유지되는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 후 페이드 아웃 애니메이션이 시작되기 전의 시간입니다. 0으로 설정하면 <span class="codeph"></span> 자동 숨기기 동작이 비활성화됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
