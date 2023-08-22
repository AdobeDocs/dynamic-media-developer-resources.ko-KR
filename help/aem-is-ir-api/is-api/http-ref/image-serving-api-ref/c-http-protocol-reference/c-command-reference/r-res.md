---
title: res
description: 해상도 기반 이미지 크기 조절. 요청한 해상도로 이미지 크기를 조정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# res{#res}

해상도 기반 이미지 크기 조절. 요청한 해상도로 이미지 크기를 조정합니다.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>타겟 해상도, 일반적으로 인치당 픽셀 단위(실수). </p> </td> 
 </tr> 
</table>

척도 인자는 나누어서 계산됩니다 *`val`* 작성자: `catalog::Resolution`. 이 명령은 응답 이미지의 인쇄 해상도에는 영향을 주지 않습니다.

이 기능을 사용하려면 원본 소스 이미지의 해상도를 알고 있어야 합니다 `catalog::Resolution`. 용도에 따라 해상도 단위는 달라질 수 있습니다. 배경 화면 또는 패브릭과 같은 반복 가능한 2D 텍스처 또는 재료 견본의 경우 해상도는 픽셀/인치 또는 픽셀/mm으로 표현될 수 있다. 항공 사진 및 지도는 픽셀/마일 또는 픽셀/km로 더 잘 제공될 수 있습니다. 어떤 경우든, 다음에 사용되는 장치 `catalog::Resolution` 은(는) 다음에 사용된 장치와 동일해야 합니다. `res=`.

정확한 해상도로 이미지를 얻는 것 외에도 `res=` 여러 이미지를 동일한 해상도로 결합하여 이러한 이미지에 표시되는 항목이 서로 정확하게 비례하도록 할 수도 있습니다.

>[!NOTE]
>
>일반적으로 합성 이미지는 대상 보기 크기로 크기가 조정됩니다(에 의해 지정됨) `wid=`, `hei=`, 또는 `attribute::DefaultPix`)를 반환한 후 클라이언트로 반환합니다. 이렇게 크기를 조정하지 않도록 하려면에서 지정한 정확한 해상도로 이미지를 가져옵니다. `res=`를 지정하는 방식으로 뷰 배율을 비활성화해야 할 수 있습니다 `scl=1`. 이렇게 하면 서버에서 합성 이미지를 확대하지 않고 대상 보기 크기로 자릅니다.

## 속성 {#section-fdbd16e59cff4952a3717146bc91412e}

소스 이미지/마스크 속성. 소스 이미지 또는 마스크와 연결되지 않은 레이어에서 무시됩니다. 레이어 0에 적용됨은 `layer=comp`. 다음 중 하나의 경우 무시됨 `scale=` 또는 `size=` 은 동일한 레이어에 대해 지정됩니다.

## 기본값 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

지정하지 않으면 `scale=` 또는 `size=` 배율 계수를 결정하거나, 둘 다 지정하지 않으면 이미지가 배율 조정없이 사용됩니다.

## 예 {#section-eb06f333e08e4247971fb1b18922597b}

이미지 렌더링 또는 이미지 작성에 사용할 텍스처 이미지를 12픽셀/인치 개체 해상도로 검색합니다. 손실 없는 PNG 포맷과 최상의 품질을 위한 더 나은 품질의 리샘플링을 지정합니다.

` http:// *`서버`*/myTexture?res=12&fmt=png&resMode=sharp`

## 참조 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
