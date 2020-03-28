---
description: 해상도 기반의 이미지 크기 조절 요청한 해상도에 맞게 이미지 크기를 조정합니다.
seo-description: 해상도 기반의 이미지 크기 조절 요청한 해상도에 맞게 이미지 크기를 조정합니다.
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# res{#res}

해상도 기반의 이미지 크기 조절 요청한 해상도에 맞게 이미지 크기를 조정합니다.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>대상 해상도;일반적으로 인치당 픽셀 수(실제). </p> </td> 
 </tr> 
</table>

척도 인수는 *`val`* `catalog::Resolution`로 나누어 계산됩니다. 이 명령은 응답 이미지의 인쇄 해상도에 영향을 주지 않습니다.

이 기능을 사용하려면 원본 소스 이미지의 해상도를 알고 설정해야 합니다 `catalog::Resolution`. 응용 프로그램에 따라 해상도 단위가 다를 수 있습니다. 배경 무늬 또는 직물과 같은 반복 가능한 2D 텍스처 또는 재료 견본의 경우 해상도를 픽셀/인치 또는 픽셀/mm로 표시할 수 있습니다. 항공 사진 및 맵은 픽셀/마일 또는 픽셀/km로 더 잘 제공될 수 있습니다. 어떤 경우든, 에 사용된 단위는 에 사용된 단위와 동일해야 `catalog::Resolution` 합니다 `res=`.

정확한 해상도로 이미지를 얻는 `res=` 것 외에도, 동일한 해상도로 여러 이미지를 결합하는 데 사용할 수 있으므로 이러한 이미지에 표시되는 항목이 서로 정확하게 비례합니다.

>[!NOTE]
>
>일반적으로 복합 이미지는 클라이언트로 반환되기 전에 대상 보기 크기( `wid=`, `hei=`또는 `attribute::DefaultPix`에 의해 지정됨)로 크기가 조정됩니다. 이 크기 조정을 막고 에서 지정한 정확한 해상도로 이미지를 가져오려면 `res=`명시적으로 지정하여 보기 크기 조정을 비활성화해야 할 수 `scl=1`있습니다. 이렇게 하면 서버가 대상 보기 크기를 조정하지 않고 대상 보기 크기로 합성 이미지를 자릅니다.

## 속성 {#section-fdbd16e59cff4952a3717146bc91412e}

소스 이미지/마스크 속성입니다. 소스 이미지 또는 마스크와 연결되지 않은 레이어에서 무시됩니다. 레이어 0에 적용된 값은 에 `layer=comp`지정됩니다. 동일한 레이어에 대해 `scale=` 또는 `size=` 가 지정된 경우 무시됩니다.

## 기본값 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

지정하지 `scale=` 않거나 비율 인수를 `size=` 결정하거나 둘 다 지정하지 않으면 이미지가 비율 조정 없이 사용됩니다.

## 예 {#section-eb06f333e08e4247971fb1b18922597b}

이미지 렌더링 또는 이미지 작성에서 사용할 텍스처 이미지를 12픽셀/인치 개체 해상도로 검색할 수 있습니다. 최상의 품질을 위해 손실 없는 PNG 포맷과 향상된 품질 리샘플링을 지정합니다.

` http:// *`서버`*/myTexture?res=12&fmt=png&resMode=sharp`

## 참조 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
