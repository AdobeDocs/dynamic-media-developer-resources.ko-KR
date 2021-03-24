---
description: XML을 s7 elementID로 설정합니다.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

---


# setElement{#setelement}

XML을 s7:elementID로 설정합니다.

`setElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID`이(가) 정의된 경우 `<XML>` 값이 하위 요소로 바뀝니다. `<XML>`은(는) 인코딩되어야 합니다.

## 예 {#section-f23a998b18994dd3b5d4e1965718db9f}

`s7:elementID="group2"` 속성이 `Group` 노드에 정의되면 다음 속성이 유효하다고 가정합니다.

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예에서는 `group2` 노드에서 모든 하위 노드를 제거하고 새 `TextGraphic` 하위 노드로 대체합니다.
