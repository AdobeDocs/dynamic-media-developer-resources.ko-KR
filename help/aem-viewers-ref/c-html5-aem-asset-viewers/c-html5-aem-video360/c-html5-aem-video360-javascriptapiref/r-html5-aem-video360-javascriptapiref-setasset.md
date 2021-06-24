---
description: Video360 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR 비디오
role: Developer,Business Practitioner
exl-id: 1fcd7dbe-d122-4501-92f4-3ce93a94a933
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 4%

---

# setAsset{#setasset}

Video360 뷰어에 대한 JavaScript API 참조.

`setAsset(asset)`

새 자산을 설정합니다. 이 매개 변수는 `init()` 전이나 후에 언제든지 호출할 수 있습니다. `init()` 다음에 호출되면 뷰어는 런타임 시 자산을 교체합니다.

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 문자열</span>}의 새 자산 ID입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Viewers/space_station_360-AVS")
```
