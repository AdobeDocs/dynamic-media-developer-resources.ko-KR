---
title: 실패 선택 시
description: 선택 오류 처리를 선택합니다. 지정된 픽셀 위치가 선택 가능한 개체의 마스크 영역 내에 있지 않기 때문에 sel= 명령이 실패할 경우 수행할 작업을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
TQID: 'https://experienceleague.adobe.com/rgp6VEJFX8BCZF76fg-1xzrGTuAm87-9HgGHpkNLmtE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 6%

---

# 실패 선택 시{#onfailsel}

선택 오류 처리를 선택합니다. 지정된 픽셀 위치가 선택 가능한 개체의 마스크 영역 내에 있지 않기 때문에 `sel=` 명령이 실패할 경우 수행할 작업을 지정합니다.

## 속성 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

열거형.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 기본::OnFailSel </span>에서 상속합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>이전 선택을 유지합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>선택을 해제하십시오. 재료를 적용하거나 오브젝트를 표시하거나 숨기려는 시도는 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>오류를 반환합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>기본 그룹(렌더링 가능한 개체가 포함된 비네팅 계층의 첫 번째 그룹)을 선택합니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-c25f458f9f8f4236963a95779529e664}

정의되지 않은 경우 `default::OnFailSel`에서 상속됩니다.

## 참조 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [특성::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
