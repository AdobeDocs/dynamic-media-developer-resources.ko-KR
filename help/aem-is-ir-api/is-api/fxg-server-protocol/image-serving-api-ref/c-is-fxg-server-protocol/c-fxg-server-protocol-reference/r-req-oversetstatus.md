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
   <td colname="col2"> <p> 제공된 url 수정자를 사용하여 fxg를 렌더링하는 동안 오류가 발생하면 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨텐트</span> </p> </td> 
   <td colname="col2"> <p> s7:element <span class="codeph"></span> 속성 값과 fxg 문서의 모든 페이지 목록이 있는 모든 요소의 xml 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 초과 상태</span> </p> </td> 
   <td colname="col2"> <p>&lt;RichText/&gt; <span class="codeph"></span> 요소가 넘치는 XML 목록을 반환합니다. </p> <p>클라이언트 쪽에서 처리할 수 있도록 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소 XML 목록을 반환합니다. 넘치는 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소만 반환됩니다. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> 는 <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span> 사용 시 필수 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span>속성입니다. s7: <span class="+ topic/ph pr-d/codeph codeph"> elementid가</span> 없는 넘치는 &lt;RichText/&gt; <span class="+ topic/ph pr-d/codeph codeph"> 요소는</span> 나열되지 않습니다. 목록에 있는 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 각 <span class="+ topic/ph pr-d/codeph codeph"> 요소에는</span>s7:elementid <span class="+ topic/ph pr-d/codeph codeph"> ,</span>s7:endCharIndex및 넘치는 텍스트 프레임의 경계 상자가 있습니다. s7: <span class="+ topic/ph pr-d/codeph codeph"> endCharIndex</span> 속성은 스토리의 텍스트 인덱스를 나타내며, 이 인덱스는 프레임에 텍스트를 맞출 수 있었습니다. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> 는 요청된 FXG의 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소에만 적용됩니다. 포함된 FXG의 <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> 요소는 나열되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 존재</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId 고유 요청 식별자 </p> <p>catalogRecord.exists라는 단일 속성을 반환합니다. 지정한 카탈로그 항목이 이미지 또는 기본 카탈로그에 있으면 속성 값이 "1"로 설정되고, 그렇지 않으면 "0"으로 설정됩니다. req=exists 요청은 정적 컨텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

