---
title: 실패 선택 시
description: 선택 오류 처리를 선택합니다. 지정된 픽셀 위치가 선택 가능한 개체의 마스크 영역 내에 있지 않기 때문에 sel= 명령이 실패할 경우 수행할 작업을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# 실패 선택 시{#onfailsel}

선택 오류 처리를 선택합니다. 다음과 같은 경우 수행할 작업을 지정합니다. `sel=` 지정한 픽셀 위치가 선택 가능한 개체의 마스크 영역 내에 있지 않으므로 명령이 실패합니다.

## 속성 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

열거형.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>상속 대상 <span class="codeph"> default::OnFailSel </span>. </p> </td> 
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

상속 위치 `default::OnFailSel` 정의되지 않은 경우.

## 참조 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
