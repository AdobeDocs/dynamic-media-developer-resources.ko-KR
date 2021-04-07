---
description: Video360 뷰어용 JavaScript API 참조 설명서.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,뷰어,SDK/API,360 VR 비디오
role: 개발자,비즈니스 전문가
exl-id: eb739d2d-7512-49e2-be13-10f05e2fcc1e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# setParam{#setparam}

Video360 뷰어용 JavaScript API 참조 설명서.

` setParam( *`이름, 값`*)`

뷰어 매개 변수를 지정된 값으로 설정합니다. 매개 변수는 뷰어별 구성 옵션 또는 소프트웨어 개발 키트 수정자입니다. 이 매개 변수는 `init()` 이전에 호출됩니다.

이 메서드는 뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달된 경우 선택 사항입니다.

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

## 매개 변수 {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 매개 변수의 {string}  </span> 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> 매개 변수 값. 값은 퍼센트 인코딩할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
