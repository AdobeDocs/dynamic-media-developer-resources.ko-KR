---
title: FlyoutZoomView.팁
description: FlyoutZoomView.팁
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 122c6406-6fd7-4e45-bff2-11022a3f2cf7
TQID: 'https://experienceleague.adobe.com/RAxn-9VY1W6XWau-hMwdiiIks9Fzdrtex0C54aHs-tE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# FlyoutZoomView.팁{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`지속 시간`*[, *`카운트`*][, *`페이드`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간</span> </span> </p> </td> 
   <td colname="col2"> <p>팁 텍스트가 숨겨지기 전에 표시되는 시간(초)을 지정합니다. <span class="codeph"> -1</span>(으)로 설정된 경우 사용자가 플라이아웃을 활성화하더라도 메시지는 항상 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 개수</span> </span> </p> </td> 
   <td colname="col2"> <p>집합에서 새 이미지를 볼 때 텍스트가 표시되는 횟수를 지정합니다. 값 <span class="codeph"> -1</span>은(는) 집합에서 이미지를 볼 때 텍스트가 항상 표시됨을 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p>텍스트가 나타나거나 사라질 때 발생하는 페이드 애니메이션의 지속 시간을 지정합니다. <span class="codeph"> 0</span> 값은 페이드 전환이 없음을 의미합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택적.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
