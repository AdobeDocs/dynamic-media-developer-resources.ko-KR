---
description: 선택 오류 처리를 선택합니다. 지정된 픽셀 위치가 선택 가능한 객체의 마스크 영역 내에 있지 않으므로 sel= 명령이 실패할 경우 수행할 작업을 지정합니다.
solution: Experience Manager
title: OnFailSel
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 12%

---


# OnFailSel{#onfailsel}

선택 오류 처리를 선택합니다. 지정된 픽셀 위치가 선택 가능한 객체의 마스크 영역 내에 있지 않으므로 sel= 명령이 실패할 경우 수행할 작업을 지정합니다.

## 속성 {#section-cec491e6c5c744f9bfafaaa9d8774f83}

열거형.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 기본값::OnFailSel </span>에서 상속합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>이전 선택 유지. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>선택 취소;재료를 적용하거나 개체를 표시/숨기려는 모든 시도는 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>오류 반환. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>기본 그룹(렌더링 가능한 객체가 포함된 비네팅 계층 구조의 첫 번째 그룹)을 선택합니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-c25f458f9f8f4236963a95779529e664}

정의되지 않은 경우 `default::OnFailSel`에서 상속됩니다.

## 참조 {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ,  [속성::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
