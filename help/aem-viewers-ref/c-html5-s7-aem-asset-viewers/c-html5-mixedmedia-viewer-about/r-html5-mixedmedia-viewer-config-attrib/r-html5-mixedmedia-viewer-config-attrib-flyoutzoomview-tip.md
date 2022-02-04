---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 6%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`기간`*[, *`count`*][, *`페이드`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 지속 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 팁 텍스트가 숨겨지기 전에 표시되는 시간(초)을 지정합니다. 로 설정된 경우 <span class="codeph"> -1</span>인 경우, 사용자가 플라이아웃을 활성화하더라도 항상 메시지가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 계수</span></span> </p> </td> 
   <td colname="col2"> <p> 세트에서 새 이미지를 볼 때 텍스트가 표시되는 횟수를 지정합니다. 값 <span class="codeph"> -1</span> 는 세트에서 이미지를 볼 때 텍스트가 항상 표시됨을 의미합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> 텍스트가 나타나거나 사라질 때 발생하는 페이드 애니메이션의 지속 시간을 지정합니다. 값 <span class="codeph"> 0</span> 페이드 전환이 없음을 나타냅니다. </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
