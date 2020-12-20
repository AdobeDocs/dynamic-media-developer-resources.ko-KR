---
description: 레이어를 선택합니다. 레이어를 선택하고 명령 시퀀스에서 새 레이어 정의 세그먼트를 시작합니다.
seo-description: 레이어를 선택합니다. 레이어를 선택하고 명령 시퀀스에서 새 레이어 정의 세그먼트를 시작합니다.
seo-title: 레이어
solution: Experience Manager
title: 레이어
topic: Scene7 Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# layer{#layer}

레이어를 선택합니다. 레이어를 선택하고 명령 시퀀스에서 새 레이어 정의 세그먼트를 시작합니다.

`layer= *``*|comp[, *`이름`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>선택할 레이어 수(0보다 큰 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>합성 이미지를 선택합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>레이어 이름. </p></td> 
 </tr> 
</table>

레이어 세그먼트 내의 모든 명령은 지정된 레이어에 적용됩니다. 레이어 세그먼트는 다음 `layer=` 또는 `effect=` 명령 또는 요청의 끝으로 종료됩니다.

합성 이미지(또는 일부 명령의 경우 보기)를 선택하려면 `layer=comp`을 지정합니다.

레이어 번호는 레이어의 z 순서를 효과적으로 지정합니다. 번호가 높은 레이어는 번호가 낮은 레이어 위에 배치됩니다.

레이어 번호는 연속되지 않아도 됩니다. 레이어 0이 필요합니다.

이름이 `layer= *`n`*, *`name`*` 명령 변형이 있는 레이어에 할당될 수 있습니다. 이름이 지정된 레이어를 정의하면 레이어 번호를 모르더라도 ` layer= *`name`*`으로 참조할 수 있습니다. 여러 개의 `layer= *`n`*, *`name`*` 명령을 사용하여 동일한 레이어에 여러 이름을 할당할 수 있습니다.

>[!NOTE]
>
>레이어 0은 합성 캔버스의 전체 크기를 결정합니다. 레이어 0의 경계 밖에 있는 레이어의 모든 부분은 컴포지션을 작성할 때 잘립니다.

## 속성 {#section-499963ee52c14f2898f0d0f90c1d01be}

레이어 명령. 대체 변수 참조는 `layer=`에서 지원되지 않습니다.

`comp` 은 문자열로 허용되지  *`name`* 않습니다. 동일한 *`name`*&#x200B;이(가) 둘 이상의 레이어에 할당되거나 이전에 정의되지 않은 *`name`*&#x200B;에서 레이어를 참조한 경우 오류가 반환됩니다.

## 기본값 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. `layer=comp`인 경우 많은 명령과 특성이 레이어 0에 적용됩니다.

## 특수 사례 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 동일한 이름이 여러 레이어에 매핑되는 경우(예:`layer=1,image&layer=2,image`) 오류가 발생합니다.
* 동일한 이름이 단일 레이어에 여러 번 매핑되는 경우(예:`layer=1,image&layer=1,image`), 범위는 오류 없이 평소대로 설정됩니다.
* 동일한 레이어의 이름이 여러 개 지원됩니다.

   두 이름을 사용하여 레이어를 참조할 수 있습니다(예:`layer=1,image&layer=1,picture`).
* 참조된 이름이 레이어 번호에 매핑되지 않는 경우(예:`layer=1,image&layer=picture`) 오류가 발생합니다.
* 대체 변수는 레이어 수정자에서 지원되지 않습니다(예:`layer=$image$`).

   이는 모든 순열에 적용되며 레이어 이름뿐만 아니라 일반적으로 레이어 수정자에 적용됩니다.

* 모든 병합 및 재정의 규칙은 동일한 레이어가 여러 소스(요청, 사전 또는 사후 수정자 카탈로그 레코드, 매크로 등)에서 참조되는 때와 정확히 일치해야 합니다.

## 예 {#section-cc40de6a0a754178aa752601539c815b}

[템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)의 예를 참조하십시오.
