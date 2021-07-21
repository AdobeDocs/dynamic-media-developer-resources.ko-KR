---
description: 회사의 게시 대상을 정의합니다.
solution: Experience Manager
title: PublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0656d6c-0f73-4f1d-9e1f-20b07cfe44b9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 10%

---

# PublishContext{#publishcontext}

회사의 게시 대상을 정의합니다.

구문

## 매개 변수 {#section-577d46cc75774c7c8fbdcff203a0d9ac}

자산은 각 게시 상태 및 컨텍스트에 대해 별도의 마커를 유지합니다. [setAssetsContextState](../../operations/c-operations-intro/c-methods/r-set-asset-context-state.md#reference-da96f9caef734f2883fddaf58cd886d7)로 게시 상태를 설정합니다.

<table id="table_1165D5DDC89140CD8222E5A04B39048E">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 이름 </th>
   <th colname="col2" class="entry"> 유형 </th>
   <th colname="col3" class="entry"> 설명 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string </span></td>
   <td colname="col3"> 게시 컨텍스트를 처리합니다. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextName</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3"> 게시 컨텍스트의 이름입니다. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextType</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">게시 컨텍스트 유형입니다. 다음을 포함합니다. 
    <ul id="ul_04CA7C755E5441AA8ABBD0BA3F245A78">
     <li id="li_7F578422D38E40D1A590AB21ADD84E90"><span class="codeph"> ImageServing</span></li>
     <li id="li_C112E12028E44ED7914ED0D3D6B3A45E"><span class="codeph"> ImageRendering</span></li>
     <li id="li_9430D600FA4343F6951F9AE8EA7F9530"><span class="codeph"> 비디오</span></li>
     <li id="li_4122D853BE1B4ED3B412CFA7B659EB1D"><span class="codeph"> ServerDirectory</span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [컨텍스트 게시](../../string-constants/c-string-constants/r-publish-context.md#reference-3ade116df0df40deb86154eb0ac7c12a)

