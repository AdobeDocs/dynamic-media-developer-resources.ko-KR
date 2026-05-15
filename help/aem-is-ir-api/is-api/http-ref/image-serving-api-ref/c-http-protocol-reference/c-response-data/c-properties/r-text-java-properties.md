---
description: 텍스트가 응답 형식으로 지정된 경우, 응답 데이터는 Java 속성으로 읽을 수 있는 형식으로 지정됩니다.
solution: Experience Manager
title: 텍스트(Java) 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# 텍스트(Java) 속성{#text-java-properties}

텍스트가 응답 형식으로 지정된 경우, 응답 데이터는 Java 속성으로 읽을 수 있는 형식으로 지정됩니다.

일반적인 텍스트 속성 응답에는 다음과 같은 일반적인 구조가 있습니다.

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`*&#x200B;은(는) 비어 있을 수 있습니다. 각 줄의 시작 부분과 끝 부분, = 구분 기호 앞뒤의 공백은 선택 사항입니다. 문자열 값을 묶는 데 작은 따옴표나 큰 따옴표를 사용할 수 있지만 필수는 아닙니다.

문자열 값에는 `\n`, `\t`, `\:` 또는 `\\`과(와) 같은 JAVA 스타일 이스케이프 문자가 포함될 수 있습니다.
