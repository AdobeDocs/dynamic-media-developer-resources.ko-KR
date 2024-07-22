---
title: req
description: 요청 유형. 요청 유형을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

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
   <td colname="col1"> <p> <span class="codeph"> 유효성 검사</span> </p> </td> 
   <td colname="col2"> <p> 제공된 URL 수정자를 사용하여 fxg를 렌더링할 때 발생하는 오류를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 내용</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7:element</span> 특성 값이 있는 모든 요소의 xml 목록과 fxg 문서의 모든 페이지 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> &lt;RichText/&gt;</span> 요소가 넘치는 XML 목록을 반환합니다. </p> <p>클라이언트측에서 처리할 수 있도록 과도하게 설정된 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소의 xml 목록을 반환합니다. 초과 설정된 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>개의 요소만 반환됩니다. <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>을(를) 사용할 때 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>은(는) 필수 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 특성입니다. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>이(가) 없는 초과 집합 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소가 나열되지 않습니다. 목록에 있는 각 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소에는 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 및 넘치는 텍스트 프레임의 테두리 상자가 있습니다. <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 특성은 프레임에 텍스트를 맞출 수 있었던 스토리의 텍스트 인덱스를 나타냅니다. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span>은(는) 요청된 FXG의 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소에만 적용됩니다. 포함된 FXG의 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소가 나열되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">이(가) 있음</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId 고유 요청 식별자 </p> <p>catalogRecord.exists라는 단일 속성을 반환합니다. 지정된 카탈로그 항목이 이미지 또는 기본 카탈로그에 있는 경우 속성 값은 "1"로 설정되고, 그렇지 않은 경우 속성 값은 "0"으로 설정됩니다. /is/content 컨텍스트에 대한 req=exists 요청은 정적 콘텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
