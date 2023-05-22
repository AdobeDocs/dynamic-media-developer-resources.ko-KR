---
title: 효과
description: 효과 레이어 를 선택합니다. 효과 레이어를 선택하고 요청 문자열에서 현재 레이어와 연결된 새 레이어 세그먼트를 시작합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 3%

---

# 효과{#effect}

효과 레이어 를 선택합니다. 효과 레이어를 선택하고 요청 문자열에서 현재 레이어와 연결된 새 레이어 세그먼트를 시작합니다.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>효과 레이어 번호(int가 0과 같지 않음). </p></td> 
 </tr> 
</table>

새 세그먼트 내의 모든 명령이 지정된 효과 레이어에 적용됩니다. 효과 레이어 세그먼트는 다음 방법으로 종료됩니다 `layer=` 또는 `effect=` 또는 요청이 끝날 때까지.

*`n`* 바깥쪽 레이어 효과(즉, 부모 레이어 뒤의 효과)는 0보다 작아야 하고, 안쪽 레이어 효과(즉, 부모 레이어 내의 효과)는 0보다 커야 합니다. 효과 레이어 번호는 연속일 필요가 없습니다.

효과 레이어 번호는 동일한 모 레이어에 여러 효과 레이어가 있는 경우 z차수를 지정합니다. 번호가 높은 레이어는 번호가 낮은 레이어 위에 배치됩니다.

효과 레이어를 첨부할 수 있습니다. `layer=comp`.

## 속성 {#section-e11f795deff345779ce280a82cf221ca}

효과 레이어 명령. *`n`* 은(는) 0이 아니어야 합니다.

## 기본값 {#section-84bbe1cfe7a94040827c994323ac59d4}

없음.

## 예 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 참조 {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
