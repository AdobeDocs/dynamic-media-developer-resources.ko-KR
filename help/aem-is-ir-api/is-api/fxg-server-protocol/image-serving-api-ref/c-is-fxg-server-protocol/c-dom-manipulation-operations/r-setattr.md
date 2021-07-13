---
description: 지정된 s7 elementID에 대한 속성을 설정합니다.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# setAttr{#setattr}

지정된 s7:elementID에 대한 속성을 설정합니다.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXG 노드 요소에 `s7:elementID`이 정의된 경우 해당 노드의 속성을 조작할 수 있습니다. 속성/값 쌍을 원하는 만큼 설정할 수 있습니다. 속성은 FXG에서 이미 정의할 필요가 없지만 노드 요소에 대해 유효해야 합니다. `{}` 사이의 모든 값은 이스케이프되어야 합니다.

## 예 {#section-9c37470d5f0349e5b0a97291782cb7a6}

`BitmapGraphic` 노드에 대해 `s7:elementID="Group1"` 속성이 정의되어 있다고 가정하고, 다음 속성이 유효하다고 가정합니다.

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

이 예에서는 `BitmapGraphic`에 대해 *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* 및 *[!DNL scaleY]*&#x200B;를 설정하고 기존 값을 무시합니다.
