---
title: JavaScript 속성
description: JavaScript이 응답 형식으로 지정된 경우 응답 데이터는 JavaScript&trade; include 파일로 구문 분석되도록 형식이 지정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# JavaScript 속성{#javascript-properties}

JavaScript이 응답 형식으로 지정된 경우 응답 데이터는 JavaScript 포함 파일로 구문 분석되도록 형식이 지정됩니다.

일반적인 JavaScript 속성 응답에는 다음과 같은 일반적인 구조가 있습니다.

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`*&#x200B;은(는) 비워 둘 수 있습니다. 각 줄의 시작 부분과 끝 부분, = 구분 기호 앞뒤의 공백은 선택 사항입니다. 모든 값은 작은 따옴표로 묶여 있습니다. 문자열의 작은 따옴표는 두 개의 연속 작은 따옴표로 이스케이프됩니다.

JavaScript 속성 응답을 구문 분석하려면 속성 파일을 로드하기 전에 응답에서 참조되는 모든 개체를 만들어야 합니다. 다음은 `req=props`을(를) 사용하여 JavaScript에서 응답 이미지 크기를 가져오는 예제입니다.

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
