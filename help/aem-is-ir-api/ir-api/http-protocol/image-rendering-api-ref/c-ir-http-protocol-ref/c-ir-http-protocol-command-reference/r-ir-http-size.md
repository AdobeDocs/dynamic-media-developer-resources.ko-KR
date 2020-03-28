---
description: 100% 크기 십자 자료의 크기를 지정합니다.
seo-description: 100% 크기 십자 자료의 크기를 지정합니다.
seo-title: 크기
solution: Experience Manager
title: 크기
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 크기{#size}

100% 크기 십자 자료의 크기를 지정합니다.

` size= *`너비,높이`*[ *`,두께`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 너비, 높이 </span> </p> </td> 
  <td class="stentry"> <p>장면 좌표 단위(일반적으로 인치)(실제)의 십자 오브젝트의 크기입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 두께 </span> </p> </td> 
  <td class="stentry"> <p>장면 좌표 단위(일반적으로 인치)(실제)의 decal 개체 두께입니다. </p> </td> 
 </tr> 
</table>

너비와 높이가 모두 0이 아닌 경우, 이미지의 크기가 지정된 크기로 조정되고 이미지의 종횡비가 유지되지 않습니다. 두 값을 0으로 설정하면 이미지의 종횡비가 유지됩니다.

지정된 *`thickness`* 경우 비네팅 객체가 적절한 광원 벡터를 정의하면 그림자가 렌더링됩니다. 그림자 렌더링을 비활성화하려면 0으로 *`thickness`* 설정합니다.

## 속성 {#section-818e01e91fed4015951189c818ef28d8}

재료 속성. 10개 전용다른 모든 자료에 의해 무시됨 `res=` 가 0보다 큰 경우 값이 무시됩니다. 값은 음수일 수 없습니다.

## 기본값 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` 분류 자료가 카탈로그 항목을 기반으로 한 경우그렇지 `size=0,0,0`않은 경우 decal 크기는 `res=` 지정되지 *`wid`* 않았거나 0으로 설정된 *`hei`* 경우에 계산됩니다. 그림자를 지정하지 *`thickness`* 않았거나 0으로 설정하면 렌더링되지 않습니다.

## 예 {#section-04fdc2b60b9e4071b672bf6a913738ad}

적절한 그림자 효과를 위해 해상도에 따라 크기가 조절되고, 시계 방향으로 20도 회전하며, 두께가 2.5인치인 디캘의 MSS입니다.

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 참조 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[장면 좌표](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [속성::해상도](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
