---
title: setVal
description: s7 elementID에 대한 텍스트 노드 값을 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
TQID: 'https://experienceleague.adobe.com/bwE12rWee56rVQDuctPsmq5TUwVJy39HNUff-ZYuybM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 1%

---

# setVal{#setval}

s7:elementID에 대한 텍스트 노드 값을 설정하십시오.

`setVal.elementID= *[!DNL value]*`

FXG 노드 요소에 `s7:elementID`이(가) 정의되어 있으면 해당 노드의 텍스트 값을 조작할 수 있습니다.

## 예 {#section-f574fd66dedd4a219aa537d7bdabea23}

`TextGraphic` 노드에 대해 `s7:elementID="paragraph1"` 특성이 정의된 경우 다음 특성이 유효합니다.

`&setVal.paragraph=Hello`

이 예에서는 단락 노드의 텍스트 값을 &quot;Hello&quot;로 설정합니다.
