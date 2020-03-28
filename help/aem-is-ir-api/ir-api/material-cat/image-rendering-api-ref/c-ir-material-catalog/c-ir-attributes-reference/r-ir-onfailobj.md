---
description: 개체 선택 오류 처리. 비네팅 객체 계층에서 지정된 경로를 일치시킬 수 없으므로 obj= 명령이 실패할 경우 수행할 작업을 지정합니다.
seo-description: 개체 선택 오류 처리. 비네팅 객체 계층에서 지정된 경로를 일치시킬 수 없으므로 obj= 명령이 실패할 경우 수행할 작업을 지정합니다.
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
topic: Scene7 Image Serving - Image Rendering API
uuid: b9dcaf29-ffa5-47db-9c8c-d1809da73582
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailObj{#onfailobj}

개체 선택 오류 처리. 비네팅 객체 계층에서 지정된 경로를 일치시킬 수 없으므로 obj= 명령이 실패할 경우 수행할 작업을 지정합니다.

## 속성 {#section-2c779d9c133a443d9f0aed9fde7b703c}

열거형.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Inherit from <span class="codeph"> default::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>이전 선택 유지. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>선택 취소;재질을 적용하거나 개체를 표시하거나 숨기려는 모든 시도는 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>오류 반환. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>기본 그룹(렌더링할 수 있는 개체가 포함된 비네팅 계층 구조의 첫 번째 그룹)을 선택합니다. </p> </td> 
 </tr> 
</table>

## 기본값 {#section-a5a95a2b4a204a4eae350e5b544d1513}

정의되지 `default::OnFailObj` 않은 경우 상속됩니다.

## 참조 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
