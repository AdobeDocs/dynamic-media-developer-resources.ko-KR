---
title: appendElement
description: XML을 s7 elementID에 추가합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# appendElement{#appendelement}

s7:elementID에 XML을 추가합니다.

`appendElement.elementID=<XML>`

FXG 노드 요소에 정의된 `s7:elementID`이(가) 있는 경우 `<XML>` 값이 자식 요소로 추가됩니다. `<XML>`을(를) 인코딩해야 합니다.

## 예 {#section-4368570aa198485d91b73b4d0741478f}

Group 노드에 대해 `s7:elementID="group1"` 특성이 정의되어 있다고 가정할 경우 올바른 특성은 다음과 같습니다.

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예제에서는 텍스트 그래픽 자식 요소를 `group1`에 추가합니다.
