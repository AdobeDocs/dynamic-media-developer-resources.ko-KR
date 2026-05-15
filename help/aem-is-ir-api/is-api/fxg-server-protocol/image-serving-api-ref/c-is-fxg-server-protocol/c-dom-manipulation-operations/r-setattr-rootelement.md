---
title: setAttr.rootElement
description: 속성을 FXG 루트 요소로 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47bd947f-c078-4fd3-99cb-5ef48ea3e05e
TQID: 'https://experienceleague.adobe.com/bx5ix9VcuynEb-Y8VJdFuMKmBMSBgTSa2L-sYAw9Do0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 48
ht-degree: 2%

---

# setAttr.rootElement{#setattr-rootelement}

속성을 FXG 루트 요소로 설정합니다.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

이 명령은 루트 요소의 속성을 조작할 수 있습니다.

## 예 {#section-2758a6e316c34b99b13b02147e5973bb}

다음 루트 요소가 있는 경우:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

다음 명령을 적용한 후:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

이제 루트 요소가 다음으로 변경되었습니다.

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
