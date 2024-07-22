---
description: 텍스트가 응답 형식으로 지정된 경우, 응답 데이터는 Java 속성으로 읽을 수 있는 형식으로 지정됩니다.
solution: Experience Manager
title: 텍스트(Java) 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
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
