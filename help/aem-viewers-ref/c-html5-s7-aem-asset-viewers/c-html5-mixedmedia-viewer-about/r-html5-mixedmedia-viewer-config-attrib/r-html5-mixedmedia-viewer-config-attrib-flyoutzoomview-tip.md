---
title: FlyoutZoomView.팁
description: FlyoutZoomView.팁
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
TQID: 'https://experienceleague.adobe.com/Pnrb2IBaQgvQL2acyGn7eJuCy1ko0ok42azq9b2y50w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# FlyoutZoomView.팁{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`지속 시간`*[, *`카운트`*][, *`페이드`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 기간</span></span> </p> </td> 
   <td colname="col2"> <p> 팁 텍스트가 숨겨지기 전에 표시되는 시간(초)을 지정합니다. <span class="codeph"> -1</span>(으)로 설정된 경우 사용자가 플라이아웃을 활성화하더라도 메시지는 항상 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 개수</span></span> </p> </td> 
   <td colname="col2"> <p> 집합에서 새 이미지를 볼 때 텍스트가 표시되는 횟수를 지정합니다. 값 <span class="codeph"> -1</span>은(는) 집합에서 이미지를 볼 때 텍스트가 항상 표시됨을 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> 텍스트가 나타나거나 사라질 때 발생하는 페이드 애니메이션의 지속 시간을 지정합니다. <span class="codeph"> 0</span> 값은 페이드 전환이 없음을 나타냅니다. </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
