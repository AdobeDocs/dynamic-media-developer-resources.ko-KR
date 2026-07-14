---
description: 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
TQID: 'https://experienceleague.adobe.com/lwSvqbGdXYM1txYvK2of-67envHzyEs4UMsnVmkPKj8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 1%

---

# setAsset{#setasset}

비디오 뷰어에 대한 JavaScript API 참조.

[!DNL ` setAsset( *`자산`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 자산 </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 문자열 </span> 새 자산 id 또는 선택적 이미지 제공 수정자가 <span class="codeph"> 뒤에 추가된 명시적 이미지 집합입니까? </span>. </p> <p> IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

새 자산을 설정합니다. 이 매개 변수는 [!DNL `init()`] 전이나 후에 언제든지 호출할 수 있습니다. [!DNL `init()`] 이후에 호출되는 경우 뷰어는 런타임 시 자산을 교체합니다.

[init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)도 참조하세요.

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

카탈로그에 정의된 이미지 세트에 대한 단일 참조:

```
 <instance>.setAsset("Viewers/Pluralist")
```

사전 결합된 페이지가 있는 명시적 이미지 세트:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

개별 페이지 이미지가 있는 명시적 이미지 세트:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

선명하게 하기 수정자가 세트의 모든 이미지에 추가되었습니다.

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
