---
title: op_grow
description: 이미지 확장/비활성화. 형태학적 확장(반경 > 0) 또는 부식(반경 < 0)을 이미지 데이터에 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
TQID: 'https://experienceleague.adobe.com/vNFqqzcSqktgB5ohUZjqf0RtQNOD-t7fxITR2gZl-T4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# op_grow{#op-grow}

이미지 확장/비활성화. 형태학적 확장(반경 > 0) 또는 부식(반경 &lt; 0)을 이미지 데이터에 적용합니다.

`op_grow= *`반경`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 반경</span></span> </p> </td> 
  <td class="stentry"> <p>픽셀 단위 확장/역행 반경(int -100..100). </p></td> 
 </tr> 
</table>

`*`반경`*`은(는) 합성 이미지를 기준으로 픽셀 단위입니다. 이미지가 색상인 경우 각 구성 요소는 독립적으로 처리됩니다.

주로 레이어 효과 크기를 수정하는 데 사용됩니다. 또한 마스크를 사용하여 텍스트 레이어 또는 단색 레이어에 특수 효과를 구현하는 데 유용합니다.

## 속성 {#section-b1c66d65168d4ea695e8662ea690bd4e}

레이어 속성입니다. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다.

## 기본값 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`(변경 없음).

## 참조 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[레이어 효과](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
