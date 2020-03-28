---
description: XML을 s7 elementID로 설정합니다.
seo-description: XML을 s7 elementID로 설정합니다.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

XML을 s7:elementID로 설정합니다.

`setElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID` 정의된 값이 있으면 `<XML>` 값이 하위 요소로 대체됩니다. The `<XML>` must be encoded.

## 예 {#section-f23a998b18994dd3b5d4e1965718db9f}

노드에 대해 `s7:elementID="group2"` 속성이 정의된 경우 `Group` 다음 속성이 유효하다고 가정합니다.

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예에서는 `group2`노드에서 모든 하위 노드를 제거하고 새 `TextGraphic` 하위 노드로 대체합니다.
