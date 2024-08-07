---
title: 속성
description: 속성 데이터는 다음 req= 유형 imageprop 및 prop에 응답하여 반환됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 속성{#properties}

속성 데이터는 req= 유형 imageprop 및 prop에 대한 응답으로 반환됩니다.

응답 데이터는 Java™ 속성으로 읽을 수 있는 형식으로 되어 있습니다. 일반적인 텍스트 속성 응답에는 다음과 같은 일반적인 구조가 있습니다.

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*`은(는) 비워 둘 수 있습니다. 공백은 각 줄의 시작과 끝, &#39;=&#39; 구분 기호 전후에 선택 사항입니다. 문자열 값을 묶는 데 작은 따옴표나 큰 따옴표를 사용할 수 있지만 필수는 아닙니다.

문자열 값에는 `\n`, `\t`, `\:` 또는 `\\`과(와) 같은 JAVA 스타일 이스케이프 문자가 포함될 수 있습니다.

**참고 항목**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
