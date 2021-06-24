---
description: 이미지를 확대/축소합니다. 이미지 데이터에 형태적 희석화(반경 > 0) 또는 축소(반경 < 0)를 적용합니다.
solution: Experience Manager
title: op_grow
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_grow{#op-grow}

이미지를 확대/축소합니다. 이미지 데이터에 형태적 희석화(반경 > 0) 또는 축소(반경 &lt; 0)를 적용합니다.

`op_grow= *`반경`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 반경</span></span> </p> </td> 
  <td class="stentry"> <p>반지름을 픽셀 단위로 확대/손상시킵니다(int -100..100). </p></td> 
 </tr> 
</table>

`*``*` 컴포지트 이미지에 대해 픽셀 단위의 방사선을 생성합니다. 이미지가 색상이면 각 구성 요소는 독립적으로 처리됩니다.

주로 레이어 효과 크기를 수정하는 데 사용됩니다. 또한 마스크가 있는 텍스트 레이어 또는 단색 레이어에 특별한 효과를 주는 데 유용합니다.

## 속성 {#section-b1c66d65168d4ea695e8662ea690bd4e}

레이어 속성입니다. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다.

## 기본값 {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`: 변경되지 않음.

## 참조 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[레이어 효과](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
