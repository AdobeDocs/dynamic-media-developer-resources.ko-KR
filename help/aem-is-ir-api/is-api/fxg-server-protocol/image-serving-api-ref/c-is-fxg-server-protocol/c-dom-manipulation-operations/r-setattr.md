---
description: 지정된 s7 elementID에 대한 속성을 설정합니다.
seo-description: 지정된 s7 elementID에 대한 속성을 설정합니다.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAttr{#setattr}

지정된 s7:elementID에 대한 속성을 설정합니다.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXG 노드 요소에 `s7:elementID` 정의된 속성이 있으면 해당 노드의 속성을 조작할 수 있습니다. 원하는 만큼 속성/값 쌍을 설정할 수 있습니다. FXG에 속성을 이미 정의할 필요는 없지만 노드 요소에 대해 유효해야 합니다. 그 사이에 있는 모든 값은 이스케이프되어야 `{}` 합니다.

## 예 {#section-9c37470d5f0349e5b0a97291782cb7a6}

노드에 대해 `s7:elementID="Group1"` 속성이 정의된 경우 `BitmapGraphic` 다음 속성이 유효하다고 가정합니다.

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

이 예에서는 에 대한 *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]**[!DNL scaleX]*&#x200B;및 *[!DNL scaleY]* 를 설정하고 `BitmapGraphic` 기존 값을 무시합니다.
