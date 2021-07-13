---
description: 요청 유형. 요청 유형을 지정합니다.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 2%

---

# req{#req}

요청 유형. 요청 유형을 지정합니다.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 값 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 유효성 확인</span> </p> </td> 
   <td colname="col2"> <p> 제공된 url 수정자로 fxg를 렌더링할 때 모든 오류를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨텐트</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7:element</span> 속성 값과 fxg 문서에 있는 모든 페이지의 목록을 포함하는 모든 요소의 xml 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> &lt;RichText/&gt;</span> 요소가 오버셋된 XML 목록을 반환합니다. </p> <p>클라이언트 측에서 처리하기 위해 오버셋된 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소의 xml 목록을 반환합니다. 과잉설정된 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소만 반환됩니다. <span class="+ topic/ph pr-d/codeph codeph"> s7: </span> elementidies는  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> req=oversetstatus <span class="+ topic/ph pr-d/codeph codeph"> 를 사용할 때 필요한 속성입니다</span>. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>이 없는 오버세트 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소가 나열되지 않습니다. 목록에 있는 각 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소에는 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 및 넘치는 텍스트 프레임의 테두리 상자가 있습니다. <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 특성은 스토리의 텍스트 인덱스를 최대 텍스트 프레임에 맞출 수 있도록 나타냅니다. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstateususly는  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 요청된 FXG의 요소에만 적용됩니다. 포함된 FXG의 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소가 나열되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 존재</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId 고유 요청 식별자 </p> <p>catalogRecord.exists라는 단일 속성을 반환합니다. 지정된 카탈로그 항목이 이미지 또는 기본 카탈로그에 있으면 속성 값이 "1"로 설정되어 있고 그렇지 않으면 "0"으로 설정됩니다. /is/content 컨텍스트에 대한 req=exists 요청은 정적 콘텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
