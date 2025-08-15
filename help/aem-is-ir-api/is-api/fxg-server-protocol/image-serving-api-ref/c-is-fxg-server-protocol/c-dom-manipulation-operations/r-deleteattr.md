---
description: 지정된 s7 elementID에 대한 속성을 삭제합니다.
solution: Experience Manager
title: 삭제 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---

# 삭제 속성{#deleteattr}

지정된 s7:elementID에 대한 특성을 삭제합니다.

`deleteAttr.elementID={attributeName%26attributeName}`

FXG 노드 요소에 `s7:elementID`이(가) 정의되어 있으면 이 명령을 사용하여 해당 노드의 특성을 삭제할 수 있습니다.

## 예 {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

이 예제에서는 원래 FXG 노드에서 *[!DNL x]*, *[!DNL y]* 및 *[!DNL visible]* 특성을 제거합니다.
