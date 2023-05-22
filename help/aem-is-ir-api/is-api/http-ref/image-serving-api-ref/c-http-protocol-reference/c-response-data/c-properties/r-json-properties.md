---
title: JSONP 속성
description: jsonp가 응답 형식으로 지정된 경우, 응답 데이터는 JavaScript 함수 호출로 래핑된 JSONP(JavaScript Object Notation with Padding)를 사용하여 형식이 지정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# JSONP 속성{#jsonp-properties}

jsonp가 응답 형식으로 지정된 경우, 응답 데이터는 JavaScript 함수 호출로 래핑된 JSONP(JavaScript Object Notation with Padding)를 사용하여 형식이 지정됩니다.

클라이언트는 선택적 고유 요청 식별자 ( )를 지정할 수 있습니다. *`reqId`*) - 응답에서 반환되고 클라이언트가 비동기적으로 받은 여러 응답을 구분할 수 있습니다. 일반적인 응답은 다음과 같은 일반적인 구조를 가집니다.

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

다음 `s7jsonResponse` JavaScript 함수는 클라이언트가 정의해야 합니다. 가장 간단한 형식에서 함수는 다음과 같을 수 있습니다.

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP 응답 형식을 지원하는 요청을 사용하면 확장 구문을 사용하는 JS 콜백 핸들러의 이름을 지정할 수 있습니다. `req=` 매개 변수:

`req=...,json [&handler = reqHandler]`

다음 `<reqHandler>` 구문은 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0~9자만 허용됩니다. 선택적. 기본값은 입니다 `s7jsonResponse`.

Dynamic Media 이미지 제공 뷰어 패키지에는 이미지 제공에서 JSONP 형식 데이터를 요청하고 구문 분석하는 유틸리티가 포함되어 있습니다.

다음을 참조하십시오 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) jsonp 형식에 대한 자세한 정보입니다.

다음을 참조하십시오 [www.json.org](https://www.json.org/json-en.html) JSON 형식에 대한 자세한 정보입니다.

참조: [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
