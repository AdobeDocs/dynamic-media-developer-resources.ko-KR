---
title: 크기
description: 데칼 크기. 데칼 자료의 크기를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 2%

---

# 크기{#size}

데칼 크기. 데칼 자료의 크기를 지정합니다.

` size= *`너비, 높이`*[ *`, 두께`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 너비, 높이 </span> </p> </td> 
  <td class="stentry"> <p>장면 좌표 단위의 데칼 오브젝트 크기(일반적으로 인치)(실수, 실수). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 두께 </span> </p> </td> 
  <td class="stentry"> <p>장면 좌표 단위의 데칼 객체의 두께입니다(일반적으로 인치)(실수). </p> </td> 
 </tr> 
</table>

너비와 높이 모두 0이 아니면 이미지가 지정된 치수로 정확하게 조정되며 이미지의 종횡비가 유지되지 않습니다. 두 값 중 하나를 0으로 설정하면 이미지의 종횡비가 유지됩니다.

*`thickness`*&#x200B;을(를) 지정하면 비네팅 개체가 적절한 조명 벡터를 정의하는 경우 그림자가 렌더링됩니다. 그림자 렌더링을 비활성화하려면 *`thickness`*&#x200B;을(를) 0으로 설정합니다.

## 속성 {#section-818e01e91fed4015951189c818ef28d8}

재질 속성입니다. 데칼에서만 사용되고 다른 모든 재료에서는 무시됩니다. 너비 또는 높이가 0보다 크면 `res=`이(가) 무시됩니다. 값은 음수일 수 없습니다.

## 기본값 {#section-f91f516c6af54f0eb4d8c964b923cae0}

데칼 자료가 카탈로그 항목을 기반으로 하는 경우 `catalog::Size`, 그렇지 않은 경우 `size=0,0,0`. *`wid`* 및 *`hei`*&#x200B;이(가) 지정되지 않았거나 0으로 설정된 경우 `res=`에서 십진수 크기가 계산됩니다. *`thickness`*&#x200B;이(가) 지정되지 않았거나 0으로 설정된 경우 그림자 효과를 렌더링하지 않습니다.

## 예 {#section-04fdc2b60b9e4071b672bf6a913738ad}

해상도에 따라 크기가 조정되고 시계 방향으로 20도 회전되며 두께가 2.5인치인 데칼용 MSS를 사용하여 적절한 그림자 효과를 얻을 수 있습니다.

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 참조 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[장면 좌표](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [특성::해상도](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
