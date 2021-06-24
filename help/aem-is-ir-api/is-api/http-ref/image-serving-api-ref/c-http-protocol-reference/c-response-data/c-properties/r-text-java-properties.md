---
description: 텍스트가 응답 형식으로 지정된 경우 회신 데이터는 Java 속성으로 읽을 수 있도록 서식이 지정됩니다.
solution: Experience Manager
title: 텍스트(Java) 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 텍스트(Java) 속성{#text-java-properties}

텍스트가 응답 형식으로 지정된 경우 회신 데이터는 Java 속성으로 읽을 수 있도록 서식이 지정됩니다.

일반적인 텍스트 속성 응답에는 다음과 같은 일반 구조가 있습니다.

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

*`propertyValue`* 비어 있을 수 있습니다. 공백은 각 줄의 시작 및 끝과 = 구분 기호 앞 및 뒤에서 선택 사항입니다. 문자열 값을 묶는 데에는 작은 따옴표나 큰 따옴표를 사용할 수 있지만, 필수는 아닙니다.

문자열 값에는 `\n`, `\t`, `\:` 또는 `\\`와 같은 JAVA 스타일의 이스케이프 문자가 포함될 수 있습니다.
