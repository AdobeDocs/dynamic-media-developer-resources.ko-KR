---
title: 레이어
description: 레이어를 선택합니다. 레이어를 선택하고 명령 시퀀스에서 새 레이어 정의 세그먼트를 시작합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---

# 레이어{#layer}

레이어를 선택합니다. 레이어를 선택하고 명령 시퀀스에서 새 레이어 정의 세그먼트를 시작합니다.

`layer= *`n`*|comp[, *`이름`*]`

`layer= *`이름`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>선택할 레이어 수(0개 이상 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>복합 이미지를 선택합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 이름</span></span> </p></td> 
  <td class="stentry"> <p>레이어 이름. </p></td> 
 </tr> 
</table>

레이어 세그먼트 내의 모든 명령은 지정된 레이어에 적용됩니다. 레이어 세그먼트는 다음으로 끝납니다 `layer=` 또는 `effect=` 명령 또는 요청 끝입니다.

지정 `layer=comp` 합성 이미지(또는 보기, 일부 명령)를 선택합니다.

레이어 번호는 레이어의 z 순서를 효과적으로 지정합니다. 번호가 높은 레이어는 번호가 낮은 레이어의 맨 위에 배치됩니다.

레이어 번호는 연속될 필요가 없습니다. 레이어 0이 필요합니다.

이름이 `layer= *`n`*, *`이름`*` 명령 변형입니다. 명명된 레이어가 정의되면 ` layer= *`이름`*`레이어 번호를 알 필요가 없습니다. 여러 이름을 사용하여 동일한 레이어에 여러 이름을 지정할 수 있습니다 `layer= *`n`*, *`이름`*` 명령.

>[!NOTE]
>
>레이어 0은 합성 캔버스의 전체 크기를 결정합니다. 컴포지션을 빌드하면 레이어 0의 경계를 벗어나는 레이어의 모든 부분이 잘립니다.

## 속성 {#section-499963ee52c14f2898f0d0f90c1d01be}

레이어 명령. 대체 변수 참조는 `layer=`.

`comp` 는 *`name`* 문자열. 동일한 경우 오류가 반환됩니다 *`name`* 둘 이상의 레이어에 할당되거나, 레이어가 *`name`* 이전에 정의되지 않은 주제입니다.

## 기본값 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 많은 명령 및 속성이 `layer=comp`.

## 특별 사례 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 동일한 이름이 여러 레이어에 매핑되는 경우(예: `layer=1,image&layer=2,image`)이면 오류가 발생합니다.
* 동일한 이름이 단일 레이어에 여러 번 매핑되는 경우(예: `layer=1,image&layer=1,image`), 범위는 정상적으로 설정되어 오류 없이 설정됩니다.
* 동일한 레이어의 여러 이름이 지원됩니다.

   두 이름 중 하나를 사용하여 레이어를 참조할 수 있습니다(예: `layer=1,image&layer=1,picture`).
* 참조된 이름이 레이어 번호에 매핑되지 않는 경우(예: `layer=1,image&layer=picture`)이면 오류가 발생합니다.
* 대체 변수는 레이어 수정자에서 지원되지 않습니다(예: `layer=$image$`).

   이는 레이어 이름뿐만 아니라 일반적으로 레이어 수정자에 적용되는 모든 순열에 적용됩니다.

* 모든 병합 및 재정의 규칙은 여러 소스(요청, 사전 또는 사후 수정자 카탈로그 레코드, 매크로 등)에서 동일한 레이어를 참조한 것과 동일하게 작동해야 합니다.

## 예 {#section-cc40de6a0a754178aa752601539c815b}

의 예를 참조하십시오. [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
