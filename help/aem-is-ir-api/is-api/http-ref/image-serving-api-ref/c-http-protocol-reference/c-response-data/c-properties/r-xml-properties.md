---
description: xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 구문 분석할 수 있는 XML 문서 형식으로 지정됩니다.
solution: Experience Manager
title: XML 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# XML 속성{#xml-properties}

xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 구문 분석할 수 있는 XML 문서 형식으로 지정됩니다.

일반적인 속성 응답 문서에는 다음과 같은 일반적인 구조가 있습니다.

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

`<prop-group>` 요소는 가장 바깥쪽 컨테이너로 사용되고 속성을 그룹화하는 데 사용됩니다. 그룹 이름이 지정되면 이 이름은 Java/JavaScript 개체 이름에 해당합니다.

>[!NOTE]
>
>일부 `req=` 유형에 대해 문자 인코딩을 지정할 수 있습니다. 자세한 내용은 특정 `req=` 명령에 대한 설명을 참조하십시오.
