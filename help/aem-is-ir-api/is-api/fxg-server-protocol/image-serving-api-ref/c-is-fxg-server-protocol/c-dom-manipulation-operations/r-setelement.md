---
title: setElement
description: XML을 s7 elementID로 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

XML을 s7:elementID로 설정합니다.

`setElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID`이(가) 정의되어 있으면 `<XML>` 값이 자식 요소로 대체됩니다. `<XML>`을(를) 인코딩해야 합니다.

## 예 {#section-f23a998b18994dd3b5d4e1965718db9f}

`Group` 노드에 대해 `s7:elementID="group2"` 특성이 정의된 경우 다음 특성이 유효합니다.

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예제에서는 `group2`노드의 모든 하위 노드를 제거하고 새 `TextGraphic` 하위 노드로 대체합니다.
