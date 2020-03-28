---
description: xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 구문 분석할 수 있는 XML 문서로 형식이 지정됩니다.
seo-description: xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 구문 분석할 수 있는 XML 문서로 형식이 지정됩니다.
seo-title: XML 속성
solution: Experience Manager
title: XML 속성
topic: Scene7 Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# XML 속성{#xml-properties}

xml이 응답 형식으로 지정된 경우 응답 데이터는 표준 XML 파서에서 구문 분석할 수 있는 XML 문서로 형식이 지정됩니다.

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

요소는 가장 바깥쪽 컨테이너로 사용되고 속성을 그룹화하는 데 사용됩니다. `<prop-group>` 그룹 이름을 지정하면 Java/JavaScript 개체 이름에 해당합니다.

>[!NOTE]
>
>일부 `req=` 유형의 경우 문자 인코딩을 지정할 수 있습니다. 자세한 내용은 특정 `req=`명령에 대한 설명을 참조하십시오.

