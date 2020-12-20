---
description: 텍스트를 응답 형식으로 지정하면 응답 데이터의 형식이 Java 속성으로 읽을 수 있습니다.
seo-description: 텍스트를 응답 형식으로 지정하면 응답 데이터의 형식이 Java 속성으로 읽을 수 있습니다.
seo-title: 텍스트(Java) 속성
solution: Experience Manager
title: 텍스트(Java) 속성
topic: Scene7 Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# 텍스트(Java) 속성{#text-java-properties}

텍스트를 응답 형식으로 지정하면 응답 데이터의 형식이 Java 속성으로 읽을 수 있습니다.

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

*`propertyValue`* 비어 있을 수 있습니다. 공백 문자는 각 행의 시작 및 끝과 = 구분 기호 앞/뒤에 선택 사항입니다. 문자열 값을 묶는 데 작은따옴표 또는 큰따옴표를 사용할 수 있지만 필수는 아닙니다.

문자열 값에는 `\n`, `\t`, `\:` 또는 `\\` 등의 JAVA 스타일 이스케이프 문자가 포함될 수 있습니다.
