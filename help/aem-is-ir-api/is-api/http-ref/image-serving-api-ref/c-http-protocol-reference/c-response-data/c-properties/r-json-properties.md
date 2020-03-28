---
description: jsonp가 응답 형식으로 지정된 경우 응답 데이터는 JavaScript 함수 호출로 래핑된 JSONP(패딩이 있는 JavaScript 개체 표기법)를 사용하여 형식이 지정됩니다.
seo-description: jsonp가 응답 형식으로 지정된 경우 응답 데이터는 JavaScript 함수 호출로 래핑된 JSONP(패딩이 있는 JavaScript 개체 표기법)를 사용하여 형식이 지정됩니다.
seo-title: JSONP 속성
solution: Experience Manager
title: JSONP 속성
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JSONP 속성{#jsonp-properties}

jsonp가 응답 형식으로 지정된 경우 응답 데이터는 JavaScript 함수 호출로 래핑된 JSONP(패딩이 있는 JavaScript 개체 표기법)를 사용하여 형식이 지정됩니다.

클라이언트는 응답에서 반환되는 선택적 고유 요청 식별자( *`reqId`*)를 지정할 수 있으며 클라이언트는 비동기적으로 수신한 여러 응답을 구분할 수 있습니다. 일반적인 응답에는 다음과 같은 일반 구조가 있습니다.

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

JavaScript `s7jsonResponse` 함수는 클라이언트가 정의해야 합니다. 가장 간단한 형식으로 이 함수는 다음과 같이 표시될 수 있습니다.

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

JSONP 응답 형식을 지원하는 요청을 사용하면 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 처리기의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. Default is `s7jsonResponse`.

Scene7 Image Serving Viewers 패키지에는 이미지 제공에서 JSONP 형식 데이터를 요청 및 구문 분석하는 유틸리티가 포함되어 있습니다.

JSONP [포맷에](http://en.wikipedia.org/wiki/JSONP) 대한 자세한 내용은 http://en.wikipedia.org/wiki/JSONP을 참조하십시오.

JSON [포맷에](http://www.json.org) 대한 자세한 내용은 www.json.org을 참조하십시오.

또한 [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
