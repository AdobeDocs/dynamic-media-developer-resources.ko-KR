---
description: 레이어 대칭 이동. crop= 및 before rotate= and extend= 를 적용한 후 레이어를 수평, 수직 또는 둘 다 대칭 이동합니다.
solution: Experience Manager
title: 뒤집기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# 뒤집기{#flip}

레이어 대칭 이동. crop= 및 before rotate= and extend= 를 적용한 후 레이어를 수평, 수직 또는 둘 다 대칭 이동합니다.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>레이어를 가로로 뒤집습니다(왼쪽). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>레이어를 세로로 뒤집습니다(위로). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>수평과 수직으로 모두 뒤집습니다. </p> </td> 
 </tr> 
</table>

텍스트 레이어에 적용할 수도 있습니다.

`extend=`을 포함한 일부 명령은 `layer=comp`을 선택하면 합성 레이어 대신 암시적으로 레이어 0에 적용됩니다. 이러한 시나리오에서는 `layer=comp`에 적용되는 명령 앞에 레이어 0에 자동으로 할당된 모든 명령이 적용됩니다. 따라서 `layer=comp` 이 `flip=` 앞에 적용되면 `extend=` 이 적용됩니다.

>[!NOTE]
>
>대칭 레이어는 레이어 앵커를 기반으로 배치됩니다. 다른 flip= 값은 앵커가 레이어의 중심에 있지 않을 때 서로 다른 레이어 위치를 생성합니다.

## 속성 {#section-294da2af7be746b5adfc35e29ee68217}

레이어 명령. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-502044f81a89492198d5f12a738459ea}

없음.

## 참조 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
