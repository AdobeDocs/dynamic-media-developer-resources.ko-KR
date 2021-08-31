---
description: jsonp가 응답 형식으로 지정된 경우, 응답 데이터는 JavaScript 함수 호출에 래핑된 JSONP(JavaScript 개체 표기법)를 사용하여 형식이 지정됩니다.
solution: Experience Manager
title: JSONP 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# JSONP 속성{#jsonp-properties}

jsonp가 응답 형식으로 지정된 경우, 응답 데이터는 JavaScript 함수 호출에 래핑된 JSONP(JavaScript 개체 표기법)를 사용하여 형식이 지정됩니다.

클라이언트는 응답에서 반환되고 클라이언트가 비동기식으로 수신한 여러 응답을 구분할 수 있도록 하는 선택적 고유 요청 식별자( *`reqId`*)를 지정할 수 있습니다. 일반적인 응답에는 다음과 같은 일반 구조가 있습니다.

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

`s7jsonResponse` JavaScript 함수는 클라이언트가 정의해야 합니다. 가장 간단한 형태로 함수는 다음과 같을 수 있습니다.

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 처리기의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 허용됩니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.

Dynamic Media Image Serving Viewers 패키지에는 이미지 제공에서 JSONP 형식의 데이터를 요청 및 구문 분석하는 유틸리티가 포함되어 있습니다.

JSONP 형식에 대한 자세한 내용은 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 을 참조하십시오.

JSON 형식에 대한 자세한 내용은 [www.json.org](https://www.json.org) 을 참조하십시오.

[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)도 참조하십시오.
