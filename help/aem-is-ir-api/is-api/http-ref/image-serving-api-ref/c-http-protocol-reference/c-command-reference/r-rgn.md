---
title: rgn
description: 관심 영역. 픽셀 단위로 표시되는 합성 이미지의 사각형 관심 영역(ROI)을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# rgn{#rgn}

관심 영역. 픽셀 단위로 표시되는 합성 이미지의 사각형 관심 영역(ROI)을 지정합니다.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 주역</span> </p> </td> 
  <td class="stentry"> <p>합성 이미지의 왼쪽 위 모서리에서 ROI의 왼쪽 위(int, int)로의 픽셀 오프셋. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 크기</span> </p></td> 
  <td class="stentry"> <p>ROI 크기(픽셀 단위, int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` 은 이미지를 자르지 않고 ROI만 정의합니다. 날짜 `wid=` 및/또는 `hei=` 크기보다 큰 크기가 마찬가지로 적용되면 최종 응답 이미지에서 합성 이미지로부터의 추가 데이터가 표시될 수 있다.

## 속성 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다.

합성 이미지의 바깥쪽으로 확장되는 ROI의 모든 영역은 `bgc=`.

`rgn=` 를 사용하여 최종 배율 및 맞추기 전에 적용됩니다. `scl=`, `wid=`, `hei=`, `fit=`, `rect=`, 또는 `align=`.

## 기본값 {#section-6a3df8f670084def900ffef9dab7e94a}

전체 합성 이미지( `rgn=0,0,width,height`).

## 참조 {#section-07883760f25c4d17aedbee36b7883891}

[자르기=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [정렬=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [맞춤=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
