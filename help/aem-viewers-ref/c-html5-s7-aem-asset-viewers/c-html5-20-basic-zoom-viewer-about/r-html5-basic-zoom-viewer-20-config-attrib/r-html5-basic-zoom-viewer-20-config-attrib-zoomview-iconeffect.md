---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
TQID: 'https://experienceleague.adobe.com/pVlxftuVZ3kgRfQElIXwGcoTgjWduRisjcBZGKq85LE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 이미지가 재설정 상태이고 이미지와 상호 작용할 수 있는 동작을 연상시킬 때 이미지의 상단에 IconEffect를 표시할 수 있도록 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 개수</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 나타나고 다시 나타나는 최대 횟수를 지정합니다. <span class="codeph"> -1</span> 값은 아이콘이 항상 무기한으로 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p>애니메이션을 표시하거나 숨기는 기간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자동 숨기기</span> </span> </p> </td> 
   <td colname="col2"> <p>자동으로 숨기기 전에 IconEffect가 완전히 보이는 상태를 유지하는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 다음 페이드 아웃 애니메이션이 시작되기 전까지의 시간을 의미한다. <span class="codeph"> 0</span> 설정은 자동 숨기기 동작을 사용하지 않도록 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택적.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
