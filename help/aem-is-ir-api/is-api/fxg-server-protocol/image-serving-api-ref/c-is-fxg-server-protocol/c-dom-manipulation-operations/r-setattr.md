---
title: setAttr
description: 지정된 s7 elementID에 대한 속성을 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

지정된 s7:elementID에 대한 속성을 설정합니다.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

FXG 노드 요소에 `s7:elementID` 정의된 경우 해당 노드의 속성을 조작할 수 있습니다. 속성/값 쌍을 원하는 만큼 설정할 수 있습니다. 특성은 FXG에 이미 정의되어 있지 않아도 되지만 노드 요소에 대해 유효해야 합니다. 다음 사이 의 모든 값 `{}` 이스케이프 처리되어야 합니다.

## 예 {#section-9c37470d5f0349e5b0a97291782cb7a6}

가정: `s7:elementID="Group1"` 속성이 다음에 대해 정의됨 `BitmapGraphic` 노드를 참조한다면 다음 항목이 유효합니다.

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

이 예에서는 *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, 및 *[!DNL scaleY]* 대상: `BitmapGraphic` 기존 값을 무시합니다.
