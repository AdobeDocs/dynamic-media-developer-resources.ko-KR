---
description: XML을 s7 elementID로 설정합니다.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---

# setElement{#setelement}

XML을 s7:elementID로 설정합니다.

`setElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID`이 정의된 경우 `<XML>` 값이 하위 요소로 대체됩니다. `<XML>`을 인코딩해야 합니다.

## 예 {#section-f23a998b18994dd3b5d4e1965718db9f}

`Group` 노드에 대해 `s7:elementID="group2"` 속성이 정의되어 있다고 가정하십시오. 그러면 다음 속성이 유효합니다.

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예에서는 `group2` 노드에서 모든 하위 노드를 제거하고 새 `TextGraphic` 하위 노드로 대체합니다.
