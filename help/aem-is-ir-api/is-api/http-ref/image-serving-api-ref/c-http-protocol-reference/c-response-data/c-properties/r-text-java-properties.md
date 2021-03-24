---
description: 텍스트를 응답 형식으로 지정하면 응답 데이터의 형식이 Java 속성으로 읽을 수 있습니다.
solution: Experience Manager
title: 텍스트(Java) 속성
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
