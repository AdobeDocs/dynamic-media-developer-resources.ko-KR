---
title: 뒤집기
description: 레이어 뒤집기. crop= 및 rotate= 및 extend= 적용 후 레이어를 가로, 세로 또는 두 방향으로 뒤집습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 2%

---

# 뒤집기{#flip}

레이어 뒤집기. crop= 및 rotate= 및 extend= 적용 후 레이어를 가로, 세로 또는 두 방향으로 뒤집습니다.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>레이어를 가로로 뒤집습니다(왼쪽-오른쪽). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>레이어를 세로로 뒤집습니다(위아래로). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 기간 </span> </p> </td> 
  <td class="stentry"> <p>가로 및 세로 모두 뒤집습니다. </p> </td> 
 </tr> 
</table>

텍스트 레이어에도 적용할 수 있습니다.

`extend=`을(를) 포함한 일부 명령은 `layer=comp`을(를) 선택할 때 복합 계층 대신 계층 0에 암시적으로 적용됩니다. 이러한 시나리오에서는 레이어 0에 자동으로 할당된 모든 명령이 `layer=comp`에 적용되는 명령 앞에 적용됩니다. 따라서 `layer=comp`일 때 `extend=`이(가) `flip=` 앞에 적용됩니다.

>[!NOTE]
>
>대칭 이동된 레이어는 레이어 앵커를 기준으로 배치됩니다. 앵커가 레이어의 중앙에 있지 않으면 `flip=` 값이 다르면 레이어 위치가 달라집니다.

## 속성 {#section-294da2af7be746b5adfc35e29ee68217}

레이어 명령. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다. 효과 레이어에서 무시됨.

## 기본값 {#section-502044f81a89492198d5f12a738459ea}

없음.

## 참조 {#section-47f6484deccd420983df15ec163b4a83}

[회전=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [앵커=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
