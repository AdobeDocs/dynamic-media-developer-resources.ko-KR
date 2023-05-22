---
title: setParam
description: 회전판 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# setParam{#setparam}

회전판 뷰어에 대한 JavaScript API 참조.

` setParam( *`이름, 값`*)`

viewer 매개 변수를 지정된 값으로 설정합니다. 매개 변수는 뷰어별 구성 옵션 또는 소프트웨어 개발 키트 수정자입니다. 이 매개 변수는 전에 호출됩니다. `init()`.

뷰어 구성 정보가 로 전달된 경우 이 메서드는 선택 사항입니다 `config` 생성자에 대한 JSON 개체입니다.

참조: [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## 매개 변수 {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이름 </span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 매개 변수 이름. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 매개 변수 값입니다. 값은 퍼센트 인코딩할 수 없습니다. </p> </td>
  </tr>
 </tbody>
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```
