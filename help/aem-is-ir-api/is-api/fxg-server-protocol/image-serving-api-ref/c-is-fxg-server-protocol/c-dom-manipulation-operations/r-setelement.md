---
description: XML을 s7 elementID로 설정합니다.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

XML을 s7:elementID로 설정합니다.

`setElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID` 정의됨, `<XML>` 값이 하위 요소로 대체됩니다. 다음 `<XML>` 을(를) 인코딩해야 합니다.

## 예 {#section-f23a998b18994dd3b5d4e1965718db9f}

가정: `s7:elementID="group2"` 속성이 다음에 대해 정의됨 `Group` 그러면 다음 노드가 유효합니다.

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예제는 `group2`노드를 추가하고 새 노드로 대체합니다. `TextGraphic` 하위 노드.
