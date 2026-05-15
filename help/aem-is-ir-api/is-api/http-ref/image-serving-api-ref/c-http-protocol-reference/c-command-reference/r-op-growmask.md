---
title: op_growMask
description: 이미지 확장/비활성화. 형태학적 딜레이트(반경 > 0) 또는 에로드(반경 < 0)를 마스크 데이터에 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
TQID: 'https://experienceleague.adobe.com/-MDsQlyw5ts3RL59hw4-EeF146qdxZqc3fOfzL8BUOA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 2%

---

# op_growMask{#op-growmask}

이미지 확장/비활성화. 형태학적 딜레이트(반경 > 0) 또는 에로드(반경 &lt; 0)를 마스크 데이터에 적용합니다.

`op_growMask= *`반경`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 반경</span> </p> </td> 
  <td class="stentry"> <p>반경이 전체 해상도 마스크에 적용된다고 가정하여 다운샘플링 마스크에 대해 축소되는 픽셀 단위의 확장/역모드 반경(int -100..100). </p></td> 
 </tr> 
</table>

주로 마스크 가장자리 주변의 아티팩트를 방지하기 위해 마스크를 약간 늘리거나 축소하는 데 사용됩니다.

## 속성 {#section-b1c66d65168d4ea695e8662ea690bd4e}

현재 레이어 또는 `layer=comp`인 경우 `0` 레이어에 적용됩니다.

## 기본값 {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`(변경 없음).

## 참조 {#section-ad3e5cecfc3448a38ea06093e015c88a}

[레이어 효과](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
