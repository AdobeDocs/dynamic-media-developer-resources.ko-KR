---
title: JSONP 속성
description: jsonp가 응답 형식으로 지정된 경우, 응답 데이터는 JavaScript 함수 호출로 래핑된 JSONP(JavaScript Object Notation with Padding)를 사용하여 형식이 지정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# JSONP 속성{#jsonp-properties}

jsonp가 응답 형식으로 지정된 경우, 응답 데이터는 JavaScript 함수 호출로 래핑된 JSONP(JavaScript Object Notation with Padding)를 사용하여 형식이 지정됩니다.

클라이언트가 응답에서 반환되고 클라이언트가 비동기적으로 수신된 여러 응답을 구분할 수 있도록 하는 선택적 고유 요청 식별자(*`reqId`*)를 지정할 수 있습니다. 일반적인 응답은 다음과 같은 일반적인 구조를 가집니다.

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

`s7jsonResponse` JavaScript 함수는 클라이언트가 정의해야 합니다. 가장 간단한 형식에서 함수는 다음과 같을 수 있습니다.

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 구문은 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

Dynamic Media 이미지 제공 뷰어 패키지에는 이미지 제공에서 JSONP 형식 데이터를 요청하고 구문 분석하는 유틸리티가 포함되어 있습니다.

JSONP 형식에 대한 자세한 내용은 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP)을(를) 참조하십시오.

JSON 형식에 대한 자세한 내용은 [www.json.org](https://www.json.org/json-en.html)을(를) 참조하십시오.

[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)도 참조하세요.
