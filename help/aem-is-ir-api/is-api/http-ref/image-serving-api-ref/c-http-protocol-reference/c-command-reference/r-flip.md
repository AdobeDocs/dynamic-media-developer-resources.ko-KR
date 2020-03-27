---
description: 레이어 뒤집기를 참조하십시오. crop= 및 before rotate= 및 extend= 적용 후 레이어를 수평, 수직 또는 둘 다 뒤집습니다.
seo-description: 레이어 뒤집기를 참조하십시오. crop= 및 before rotate= 및 extend= 적용 후 레이어를 수평, 수직 또는 둘 다 뒤집습니다.
seo-title: furm
solution: Experience Manager
title: furm
topic: Scene7 Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# flip{#flip}

레이어 뒤집기를 참조하십시오. crop= 및 before rotate= 및 extend= 적용 후 레이어를 수평, 수직 또는 둘 다 뒤집습니다.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>레이어를 가로로 뒤집습니다(왼쪽 오른쪽). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>레이어를 세로로 뒤집습니다(위로). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>가로와 세로로 모두 뒤집습니다. </p> </td> 
 </tr> 
</table>

텍스트 레이어에도 적용할 수 있습니다.

선택 시 합성 레이어 대신 레이어 0에 암시적으로 `extend=`적용되는 명령을 비롯하여 일부 `layer=comp` 명령도 있습니다. 이러한 시나리오에서는 레이어 0에 자동으로 할당된 모든 명령이 적용되는 명령 앞에 적용됩니다 `layer=comp`. 따라서, `layer=comp`언제, `extend=` 그 전에 적용이 가능합니다 `flip=`.

>[!NOTE]
>
>대칭 레이어는 레이어 앵커를 기준으로 배치됩니다.서로 다른 flip= 값은 앵커가 레이어의 중심에 없으면 서로 다른 레이어 위치를 생성합니다.

## 속성 {#section-294da2af7be746b5adfc35e29ee68217}

레이어 명령. 현재 레이어 또는 합성 이미지에 적용됩니다( `layer=comp`경우). 효과 레이어에서 무시됩니다.

## 기본값 {#section-502044f81a89492198d5f12a738459ea}

없음.

## 참조 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
