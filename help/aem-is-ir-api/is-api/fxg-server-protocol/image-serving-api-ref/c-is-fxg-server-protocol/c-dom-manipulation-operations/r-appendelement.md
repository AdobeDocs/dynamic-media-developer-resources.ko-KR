---
description: s7 elementID에 XML을 추가합니다.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# appendElement{#appendelement}

s7:elementID에 XML을 추가합니다.

`appendElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID`이 정의된 경우 `<XML>` 값이 하위 요소로 추가됩니다. `<XML>`을 인코딩해야 합니다.

## 예 {#section-4368570aa198485d91b73b4d0741478f}

그룹 노드에 대해 `s7:elementID="group1"` 속성이 정의되어 있다고 가정하고, 그 다음 속성이 유효하다고 가정합니다.

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예제에서는 텍스트 그래픽 하위를 `group1`에 추가합니다.
