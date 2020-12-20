---
description: javascript가 응답 형식으로 지정된 경우 응답 데이터의 형식이 JavaScript 포함 파일로 구문 분석됩니다.
seo-description: javascript가 응답 형식으로 지정된 경우 응답 데이터의 형식이 JavaScript 포함 파일로 구문 분석됩니다.
seo-title: JavaScript 속성
solution: Experience Manager
title: JavaScript 속성
topic: Scene7 Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# JavaScript 속성{#javascript-properties}

javascript가 응답 형식으로 지정된 경우 응답 데이터의 형식이 JavaScript 포함 파일로 구문 분석됩니다.

일반적인 JavaScript 속성 응답에는 다음과 같은 일반 구조가 있습니다.

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* 비어 있을 수 있습니다. 공백 문자는 각 행의 시작 및 끝과 = 구분 기호 앞/뒤에 선택 사항입니다. 모든 값은 작은 따옴표로 묶습니다. 문자열의 작은 따옴표는 연속해서 두 개의 작은 따옴표로 이스케이프됩니다.

JavaScript 속성 응답을 구문 분석하려면 속성 파일을 로드하기 전에 응답에서 참조되는 모든 객체를 만들어야 합니다. 다음은 `req=props`을 사용하여 JavaScript에서 응답 이미지 크기를 가져오는 예입니다.

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

