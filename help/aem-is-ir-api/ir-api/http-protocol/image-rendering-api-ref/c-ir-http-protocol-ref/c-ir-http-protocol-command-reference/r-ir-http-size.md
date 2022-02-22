---
title: 크기
description: 100% 크기 십진수 재료의 크기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%

---

# 크기{#size}

100% 크기 십진수 재료의 크기를 지정합니다.

` size= *`너비,높이`*[ *`,두께`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 너비, 높이 </span> </p> </td> 
  <td class="stentry"> <p>장면 좌표 단위(일반적으로 인치)의 십진수 개체 크기(실제, 실제)입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 두께 </span> </p> </td> 
  <td class="stentry"> <p>장면 좌표 단위(일반적으로 인치)(실수)의 십진수 객체의 두께입니다. </p> </td> 
 </tr> 
</table>

폭이나 높이가 0이 아니면 이미지가 정확히 지정된 크기로 조정되고 이미지의 종횡비는 유지되지 않습니다. 두 값을 0으로 설정하면 이미지의 종횡비가 유지됩니다.

If *`thickness`* 가 지정되면 비네팅 개체가 적절한 광벡터를 정의한 경우 그림자가 렌더링됩니다. 설정 *`thickness`* 그림자 렌더링을 비활성화하려면 0으로 설정합니다.

## 속성 {#section-818e01e91fed4015951189c818ef28d8}

재료 속성입니다. 데칼에서만 사용 다른 모든 자료에 의해 무시됨. `res=` 폭 또는 높이가 0보다 큰 경우 가 무시됩니다. 값은 음수가 아니어야 합니다.

## 기본값 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` 분류가 카탈로그 항목을 기반으로 하는 경우 그렇지 않음 `size=0,0,0`. decal 크기는 다음 위치에서 계산됩니다. `res=` if *`wid`* 및 *`hei`* 이 지정되지 않았거나 0으로 설정되어 있습니다. 그림자는 *`thickness`* 이 지정되지 않았거나 0으로 설정되었습니다.

## 예 {#section-04fdc2b60b9e4071b672bf6a913738ad}

해상도에 따라 크기가 조정되고, 시계 방향으로 20도 회전하며, 적절한 그림자 효과를 위해 두께가 2.5인치인 십진수 MSS입니다.

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 참조 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[장면 좌표](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
