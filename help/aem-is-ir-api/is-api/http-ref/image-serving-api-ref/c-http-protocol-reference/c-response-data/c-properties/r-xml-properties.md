---
description: xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 파싱할 수 있는 XML 문서 형식으로 지정됩니다.
seo-description: xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 파싱할 수 있는 XML 문서 형식으로 지정됩니다.
seo-title: XML 속성
solution: Experience Manager
title: XML 속성
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# XML 속성{#xml-properties}

xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 파싱할 수 있는 XML 문서 형식으로 지정됩니다.

일반적인 속성 응답 문서에는 다음과 같은 일반 구조가 있습니다.

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

`<prop-group>` 요소는 가장 바깥쪽 컨테이너로 사용되고 속성을 그룹화하는 데 사용됩니다. 그룹 이름이 지정된 경우 이 이름은 Java/JavaScript 개체 이름에 해당합니다.

>[!NOTE]
>
>일부 `req=` 유형에 문자 인코딩을 지정할 수 있습니다. 자세한 내용은 특정 `req=` 명령의 설명을 참조하십시오.

