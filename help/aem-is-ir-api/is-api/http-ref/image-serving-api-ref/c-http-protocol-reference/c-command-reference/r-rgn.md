---
description: 관심 영역. 합성 이미지에서 픽셀 단위로 표시되는 사각형 영역 ROI(관심 영역)를 지정합니다.
solution: Experience Manager
title: rgn
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# rgn{#rgn}

관심 영역. 합성 이미지에서 픽셀 단위로 표시되는 사각형 영역 ROI(관심 영역)를 지정합니다.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 코드</span> </p> </td> 
  <td class="stentry"> <p>컴포지트 이미지의 왼쪽 위 모서리에서 ROI의 왼쪽 위(int, int)까지 픽셀 오프셋입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 크기</span> </p></td> 
  <td class="stentry"> <p>ROI 크기(픽셀 단위)입니다(int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` 이미지를 잘라내지 않고 ROI만 정의합니다. 크기보다 큰 `wid=` 및/또는 `hei=` 도 적용될 때 합성 이미지의 추가 데이터가 최종 회신 이미지에 표시될 수 있습니다.

## 속성 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

속성 보기. 현재 레이어 설정에 관계없이 적용됩니다.

합성 이미지 외부에 있는 ROI의 모든 영역은 `bgc=`으로 채워집니다.

`rgn=` 은  `scl=`,  `wid=`,  `hei=`,  `fit=`,  `rect=` 또는  `align=`을 사용하여 최종 크기 조절 및 맞춤 전에 적용됩니다.

## 기본값 {#section-6a3df8f670084def900ffef9dab7e94a}

전체 합성 이미지( `rgn=0,0,width,height`).

## 참조 {#section-07883760f25c4d17aedbee36b7883891}

[자르기=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [확장=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
