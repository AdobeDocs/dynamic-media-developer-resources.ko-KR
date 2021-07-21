---
description: '이 유형 내에서 pageReset 필드는 RenderSet 및 Catalog 이미지 자산 유형에 의미 있습니다 '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,이미지 세트
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# ImageSetMemberUpdate{#imagesetmemberupdate}

이 유형 내에서 pageReset 필드는 RenderSet 및 Catalog 이미지 자산 유형에 의미 있습니다.

* `RenderSet`에 대해 `pageReset`은 새 렌더링 보기/견본 그룹의 시작을 나타냅니다.

* 카탈로그의 경우 `pageReset`은(는) 새 페이지 보기의 시작을 나타냅니다. 일반적으로 페이지 보기당 2개의 페이지 이미지가 있지만 이보다 더 많거나 작을 수 있습니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 이미지 세트 멤버 배열의 자산 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3">페이지를 재설정합니다. <p>설정이 무시되고 <span class="codeph"> ImageSet</span> 및 <span class="codeph"> SpinSet</span>에 대해 값이 true로 강제 설정됩니다. </p></td> 
  </tr> 
 </tbody> 
</table>
