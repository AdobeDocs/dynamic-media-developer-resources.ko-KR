---
description: 속성 데이터는 다음 req= 유형 imageprop 및 prop에 대한 응답으로 반환됩니다.
seo-description: 속성 데이터는 다음 req= 유형 imageprop 및 prop에 대한 응답으로 반환됩니다.
seo-title: 속성
solution: Experience Manager
title: 속성
topic: Scene7 Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 5%

---


# 속성{#properties}

속성 데이터는 다음 req= 유형에 대한 응답으로 반환됩니다.imageprop 및 prop.

응답 데이터는 Java 속성으로 읽을 수 있도록 형식이 지정됩니다. 일반적인 텍스트 속성 응답에는 다음과 같은 일반 구조가 있습니다.

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 비어 있을 수 있습니다. 공백 문자는 각 행의 시작 및 끝과 &#39;=&#39; 구분 기호 앞/뒤에 선택 사항입니다. 문자열 값을 묶는 데 작은따옴표 또는 큰따옴표를 사용할 수 있지만 필수는 아닙니다.

문자열 값에는 `\n`, `\t`, `\:` 등의 JAVA 스타일 이스케이프 문자가 포함될 수 있습니다. 또는 `\\`.

**참조**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
