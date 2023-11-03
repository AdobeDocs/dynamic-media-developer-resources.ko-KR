---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`페이드`*][, *`자동 숨기기`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 를 활성화합니다. <span class="codeph"> iconeffect</span> 이미지가 재설정 상태이고 이미지와 상호 작용할 수 있는 동작을 연상시킬 때 이미지의 상단에 를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 계수</span></span> </p> </td> 
   <td colname="col2"> <p> 다음 횟수의 최대 횟수를 지정합니다. <span class="codeph"> iconeffect</span> 나타나고 다시 나타납니다. 값 <span class="codeph"> -1</span> 은 아이콘이 항상 무한정 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p>애니메이션을 표시하거나 숨기는 기간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 자동 숨기기</span></span> </p> </td> 
   <td colname="col2"> <p>다음 시간(초) 숫자 설정 <span class="codeph"> iconeffect</span> 자동으로 숨기기 전에 완전히 표시됩니다. 즉, 페이드 인 애니메이션이 완료된 다음 페이드 아웃 애니메이션이 시작되기 전까지의 시간을 의미한다. 의 설정 <span class="codeph"> 0</span> 자동 숨기기 동작을 비활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
