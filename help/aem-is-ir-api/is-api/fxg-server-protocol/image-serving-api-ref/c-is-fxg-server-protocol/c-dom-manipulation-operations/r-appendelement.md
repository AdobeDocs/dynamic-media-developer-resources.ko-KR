---
description: s7 elementID에 XML을 추가합니다.
seo-description: s7 elementID에 XML을 추가합니다.
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# appendElement{#appendelement}

s7:elementID에 XML을 추가합니다.

`appendElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID` 정의된 값이 있으면 `<XML>` 값이 하위 요소로 추가됩니다. The `<XML>` must be encoded.

## 예 {#section-4368570aa198485d91b73b4d0741478f}

그룹 노드에 대해 속성이 정의된 `s7:elementID="group1"` 경우 다음 속성이 유효하다고 가정합니다.

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예제에서는 텍스트 그래픽 하위 항목을 에 추가합니다 `group1`.
