---
title: setAttr
description: 지정된 s7 elementID에 대한 속성을 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# setAttr{#setattr}

지정된 s7:elementID에 대한 특성을 설정합니다.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXG 노드 요소에 `s7:elementID`이(가) 정의되어 있으면 해당 노드의 특성을 조작할 수 있습니다. 속성/값 쌍을 원하는 만큼 설정할 수 있습니다. 특성은 FXG에 이미 정의되어 있지 않아도 되지만 노드 요소에 대해 유효해야 합니다. `{}` 사이의 모든 값은 이스케이프해야 합니다.

## 예 {#section-9c37470d5f0349e5b0a97291782cb7a6}

`s7:elementID="Group1"` 노드에 대해 `BitmapGraphic` 특성이 정의되어 있다고 가정할 경우 올바른 특성은 다음과 같습니다.

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

이 예제에서는 *[!DNL x]*&#x200B;에 대해 *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, *[!DNL scaleY]* 및 `BitmapGraphic`을(를) 설정하고 기존 값을 무시합니다.
