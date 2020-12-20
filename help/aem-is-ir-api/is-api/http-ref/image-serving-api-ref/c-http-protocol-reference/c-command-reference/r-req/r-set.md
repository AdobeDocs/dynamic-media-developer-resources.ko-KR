---
description: 미디어 세트 정보.
seo-description: 미디어 세트 정보.
seo-title: 설정
solution: Experience Manager
title: 설정
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---


# 설정{#set}

미디어 세트 정보.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 인코딩</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>고유 요청 식별자 </p></td> 
 </tr> 
</table>

URL 경로에 지정된 이미지 카탈로그 항목에 대해 카탈로그와 연결된 이미지, 비디오, 견본 및 다양한 메타데이터에 대한 정보를 반환합니다.::ImageSet 이 응답은 제공된 집합 유형에 따라 결정되는 계층 구조입니다. &#39;xml&#39; 또는 &#39;json&#39; 형식이 요청되면 적절한 서식이 적용됩니다.

HTTP 응답은 `catalog::NonImgExpiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.

>[!NOTE]
>
>req=set 요청에서는 콜론 문자를 사용할 수 없습니다.

JSON 응답 형식을 지원하는 요청에서는 `req=` 매개 변수의 확장 구문을 사용하여 JS 콜백 핸들러의 이름을 지정할 수 있습니다.

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 는 JSONP 응답에 있는 JS 핸들러의 이름입니다. a-z, A-Z 및 0-9자만 사용할 수 있습니다. 선택 사항입니다. 기본값은 `s7jsonResponse`입니다.
