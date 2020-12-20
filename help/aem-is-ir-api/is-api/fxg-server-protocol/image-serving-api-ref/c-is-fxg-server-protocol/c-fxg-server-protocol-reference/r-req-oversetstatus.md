---
description: 요청 유형. 요청 유형을 지정합니다.
seo-description: 요청 유형. 요청 유형을 지정합니다.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '249'
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
   <td colname="col2"> <p> 제공된 url 수정자로 fxg를 렌더링하는 오류를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨텐트</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7:element</span> 속성 값과 fxg 문서의 모든 페이지 목록이 포함된 모든 요소의 xml 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 초과 상태</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> &lt;RichText/&gt;</span> 요소가 넘치는 XML 목록을 반환합니다. </p> <p>클라이언트 쪽에서 처리하기 위해 넘치는 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소의 xml 목록을 반환합니다. 넘치는 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소만 반환됩니다. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidis는 req=oversetstatus를 사용할  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 때 필수  <span class="+ topic/ph pr-d/codeph codeph"> 속성입니다</span>. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>이(가) 없는 넘치는 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소는 모두 나열되지 않습니다. 목록에 있는 각 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소에는 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 및 넘치는 텍스트 프레임의 테두리 상자가 있습니다. <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 속성은 스토리의 텍스트 인덱스를 나타내며 프레임에 텍스트를 맞출 수 있습니다. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstateusonly는 요청된 FXG <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 의 요소에만 적용됩니다. 포함된 FXG의 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소는 나열되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 존재</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId 고유 요청 식별자 </p> <p>catalogRecord.exists라는 단일 속성을 반환합니다. 이미지 또는 기본 카탈로그에 지정된 카탈로그 항목이 있는 경우 속성 값은 "1"로 설정되며, 그렇지 않은 경우 "0"으로 설정됩니다. /is/content 컨텍스트에 대한 req=exists 요청은 정적 컨텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

