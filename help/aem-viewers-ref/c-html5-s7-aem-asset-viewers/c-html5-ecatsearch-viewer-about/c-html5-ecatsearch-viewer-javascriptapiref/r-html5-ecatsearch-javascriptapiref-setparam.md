---
description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic Media
uuid: a732461f-1b34-4ebe-9dfd-69175762e574
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 2%

---


# setParam{#setparam}

eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.

[!DNL ` setParam( *`이름, 값`*)`]

뷰어 매개 변수를 지정된 값으로 설정합니다. 매개 변수는 뷰어별 구성 옵션 또는 소프트웨어 개발 키트 수정자입니다. 이 매개 변수는 [!DNL `init()`] 이전에 호출됩니다.

이 메서드는 뷰어 구성 정보가 [!DNL `config`] JSON 개체와 함께 생성자에 전달될 때 선택 사항입니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

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
[!DNL <instance>.setParam("style", "customStyle.css")]
```

