---
title: OnFailObj
description: 오브젝트 선택 오류 처리. 비네팅 개체 계층에서 지정된 경로를 일치시킬 수 없어 obj= 명령이 실패할 경우 수행할 작업을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# OnFailObj{#onfailobj}

오브젝트 선택 오류 처리. 비네팅 개체 계층에서 지정된 경로를 일치시킬 수 없어 obj= 명령이 실패할 경우 수행할 작업을 지정합니다.

## 속성 {#section-2c779d9c133a443d9f0aed9fde7b703c}

열거형.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>상속 대상 <span class="codeph"> default::OnFailObj </span>. </p> </td> 
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

## 기본값 {#section-a5a95a2b4a204a4eae350e5b544d1513}

상속 위치 `default::OnFailObj` 정의되지 않은 경우.

## 참조 {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
