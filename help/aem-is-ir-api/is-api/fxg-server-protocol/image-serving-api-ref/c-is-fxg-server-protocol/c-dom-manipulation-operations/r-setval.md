---
description: s7 elementID에 대한 텍스트 노드 값을 설정합니다.
seo-description: s7 elementID에 대한 텍스트 노드 값을 설정합니다.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

s7:elementID에 대한 텍스트 노드 값을 설정합니다.

`setVal.elementID= *[!DNL value]*`

FXG 노드 요소에 `s7:elementID`이(가) 정의된 경우 해당 노드의 텍스트 값을 조작할 수 있습니다.

## 예 {#section-f574fd66dedd4a219aa537d7bdabea23}

`s7:elementID="paragraph1"` 속성이 `TextGraphic` 노드에 정의되면 다음 속성이 유효하다고 가정합니다.

`&setVal.paragraph=Hello`

이 예제에서는 단락 노드의 텍스트 값을 &quot;Hello&quot;로 설정합니다.
