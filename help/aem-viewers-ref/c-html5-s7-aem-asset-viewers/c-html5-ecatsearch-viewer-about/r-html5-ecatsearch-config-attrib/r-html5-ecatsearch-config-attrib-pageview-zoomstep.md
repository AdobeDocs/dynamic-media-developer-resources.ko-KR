---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
TQID: 'https://experienceleague.adobe.com/fceYX6xApL3EyDRk3FQFnzew7C4-Ax3acpPJH-HVrKw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`단계`*[, *`제한`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">단계</span></span> </p> </td> 
   <td colname="col2"> <p> 해상도를 2배율로 증가/감소시키는 데 필요한 확대/축소 동작 수를 구성합니다. 각 확대/축소 동작에 대한 해상도 변경은 단계당 2^1입니다. 한 번의 확대/축소 작업으로 전체 해상도로 확대/축소하려면 <span class="codeph"> 0</span>(으)로 설정하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 제한</span></span> </p> </td> 
   <td colname="col2"> <p> 전체 해상도 이미지를 기준으로 최대 확대/축소 해상도를 지정합니다. 기본값은 <span class="codeph"> 1.0</span>이며, 최대 해상도 범위를 넘지 않게 확대/축소를 제한합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-636d35a4791447039f1902973f568320}

선택적.

## 기본값 {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## 예 {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]

