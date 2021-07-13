---
description: s7 elementID에 대한 텍스트 노드 값을 설정합니다.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---

# setVal{#setval}

s7:elementID에 대한 텍스트 노드 값을 설정합니다.

`setVal.elementID= *[!DNL value]*`

FXG 노드 요소에 `s7:elementID`이(가) 정의된 경우 해당 노드의 텍스트 값을 조작할 수 있습니다.

## 예 {#section-f574fd66dedd4a219aa537d7bdabea23}

`TextGraphic` 노드에 대해 `s7:elementID="paragraph1"` 속성이 정의되어 있다고 가정하십시오. 그러면 다음 속성이 유효합니다.

`&setVal.paragraph=Hello`

이 예제에서는 단락 노드의 텍스트 값을 &quot;Hello&quot;로 설정합니다.
