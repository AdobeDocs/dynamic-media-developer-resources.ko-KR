---
description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 4929884e-b072-4177-83c3-1f9b4e5df569
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# setParams{#setparams}

eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.

[!DNL ` setParams( *`params`*)`]

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 이름=값 쌍을 [!DNL `&`]으로 구분하여 나타냅니다. 쿼리 문자에서처럼 이름 및 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. [!DNL `init()`]을(를) 호출하기 전에 이 매개 변수를 호출해야 합니다.

이 메서드는 뷰어 구성 정보가 [!DNL `config`] JSON 개체와 함께 생성자에 전달될 때 선택 사항입니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하십시오.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value 매개 변수 쌍은  <span class="codeph"> &amp;</span>로 구분됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```

