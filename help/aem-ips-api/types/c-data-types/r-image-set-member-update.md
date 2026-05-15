---
description: 이 유형 내에서 pageReset 필드는 RenderSet 및 Catalog 이미지 자산 유형에 의미가 있습니다
solution: Experience Manager
title: 이미지 집합 구성원 업데이트
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
TQID: 'https://experienceleague.adobe.com/c9-ANQJjBlcpQYnSmrD8nQQ08Vllqt3ZcpW6IBJ9-4I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 4%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

이 유형 내에서 pageReset 필드는 RenderSet 및 Catalog 이미지 자산 유형에 의미가 있습니다.

* `RenderSet`의 경우 `pageReset`은(는) 새 렌더링 보기/견본 그룹의 시작을 나타냅니다.

* 카탈로그의 경우 `pageReset`은(는) 새 페이지 보기의 시작을 나타냅니다. 일반적으로 페이지 보기당 2개의 페이지 이미지가 있지만 더 많거나 더 적을 수 있습니다.

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
   <td colname="col3"> 이미지 집합 구성원 배열의 자산 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">페이지를 재설정합니다. <p>설정이 무시되고 <span class="codeph"> ImageSet</span> 및 <span class="codeph"> SpinSet</span>에 대해 값이 true로 설정됩니다. </p></td> 
  </tr> 
 </tbody> 
</table>
