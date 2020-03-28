---
description: 이름별로 개체를 선택합니다. 이름으로 지정된 비네팅 그룹을 선택하고 새 MSS를 시작합니다.
seo-description: 이름별로 개체를 선택합니다. 이름으로 지정된 비네팅 그룹을 선택하고 새 MSS를 시작합니다.
seo-title: obj
solution: Experience Manager
title: obj
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# obj{#obj}

이름별로 개체를 선택합니다. 이름으로 지정된 비네팅 그룹을 선택하고 새 MSS를 시작합니다.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 이름 </span></span> </p> </td> 
  <td class="stentry"> <p>그룹 이름 또는 경로/이름입니다. </p> </td> 
 </tr> 
</table>

전체 그룹 경로를 사용하여 하위 그룹 또는 개별 개체를 선택할 수 있습니다(즉, 모든 상위 그룹 앞에 /(슬래시)로 구분된 대상 그룹 또는 개체의 이름을 지정하여).

지정된 이름의 그룹/개체를 찾을 수 없으면 에 지정된 작업이 `attribute::OnObjFail` 수행됩니다.

## 속성 {#section-9463b36e8ff74c81a70c7c2b58927430}

선택 명령;MSS 구분 기호. 개체 선택은 `obj=` 또는 에서 다른 개체를 선택할 때까지 지속됩니다 `sel=`.

그룹/개체 경로 및 이름은 대/소문자를 구분하지 않습니다.

## 기본값 {#section-0c322850512c4896bb551856a549440e}

새 비네팅을 열면 렌더링 가능 개체가 포함된 비네팅의 첫 번째 그룹이 자동으로 선택됩니다.

## 참조 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
