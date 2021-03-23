---
description: 지정된 s7 elementID에 대한 속성을 삭제합니다.
seo-description: 지정된 s7 elementID에 대한 속성을 삭제합니다.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

지정된 s7:elementID에 대한 속성을 삭제합니다.

`deleteAttr.elementID={attributeName%26attributeName}`

FXG 노드 요소에 `s7:elementID`이(가) 정의된 경우 해당 노드의 속성을 이 명령으로 삭제할 수 있습니다.

## 예 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

이 예에서는 원래 FXG 노드에서 *[!DNL x]*, *[!DNL y]* 및 *[!DNL visible]* 속성을 제거합니다.
