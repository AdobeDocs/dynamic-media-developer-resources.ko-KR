---
title: setElement
description: XML을 s7 elementID로 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
TQID: 'https://experienceleague.adobe.com/bLej-B1yRcTdFFXhaigx4Zf9ubwx9LkR31a9Rqdr0Zs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 62
ht-degree: 1%

---

# setElement{#setelement}

XML을 s7:elementID(으)로 설정합니다.

`setElement.elementID=<XML>`

FXG 노드 요소에 `s7:elementID`이(가) 정의되어 있으면 `<XML>` 값이 자식 요소로 대체됩니다. `<XML>`을(를) 인코딩해야 합니다.

## 예 {#section-f23a998b18994dd3b5d4e1965718db9f}

`Group` 노드에 대해 `s7:elementID="group2"` 특성이 정의된 경우 다음 특성이 유효합니다.

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

이 예제에서는 `group2`노드의 모든 하위 노드를 제거하고 새 `TextGraphic` 하위 노드로 대체합니다.
