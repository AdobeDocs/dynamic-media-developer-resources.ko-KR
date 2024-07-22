---
title: obj
description: 이름으로 객체를 선택합니다. 지정된 비네팅 그룹을 이름별로 선택하고 새 MSS를 시작합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# obj{#obj}

이름으로 객체를 선택합니다. 지정된 비네팅 그룹을 이름별로 선택하고 새 MSS를 시작합니다.

` obj= *`이름`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 이름 </span> </span> </p> </td> 
  <td class="stentry"> <p>그룹 이름 또는 경로/이름입니다. </p> </td> 
 </tr> 
</table>

전체 그룹 경로를 사용하여(즉, 대상 그룹 또는 객체 앞에 모든 상위 그룹이 앞에 오도록 /(슬래시)로 구분하여 지정한 경우) 하위 그룹 또는 개별 객체를 선택할 수 있습니다.

지정한 이름의 그룹/개체가 없으면 `attribute::OnObjFail`에 지정된 작업을 수행합니다.

## 속성 {#section-9463b36e8ff74c81a70c7c2b58927430}

선택 명령, MSS 구분 기호. `obj=` 또는 `sel=`을(를) 사용하여 다른 개체를 선택할 때까지 개체 선택은 계속됩니다.

그룹/객체 경로 및 이름은 대소문자를 구분하지 않습니다.

## 기본값 {#section-0c322850512c4896bb551856a549440e}

렌더링 가능한 오브젝트가 포함된 비네팅의 첫 번째 그룹은 새 비네팅을 열 때 자동으로 선택됩니다.

## 참조 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [특성::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
