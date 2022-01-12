---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`기간`*[, *`count`*][, *`페이드`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간</span> </span> </p> </td> 
   <td colname="col2"> <p>팁 텍스트가 숨겨지기 전에 표시되는 시간(초)을 지정합니다. 로 설정된 경우 <span class="codeph"> -1</span>인 경우, 사용자가 플라이아웃을 활성화하더라도 항상 메시지가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>세트에서 새 이미지를 볼 때 텍스트가 표시되는 횟수를 지정합니다. 값 <span class="codeph"> -1</span> 는 세트에서 이미지를 볼 때 텍스트가 항상 표시됨을 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p>텍스트가 나타나거나 사라질 때 발생하는 페이드 애니메이션의 지속 시간을 지정합니다. 값 <span class="codeph"> 0</span> 은 페이드 전환이 없음을 의미합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
