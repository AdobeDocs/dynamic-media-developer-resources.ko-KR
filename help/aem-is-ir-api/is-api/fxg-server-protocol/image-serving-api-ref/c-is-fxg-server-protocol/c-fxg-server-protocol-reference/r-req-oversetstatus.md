---
description: 요청 유형. 요청 유형을 지정합니다.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
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
   <td colname="col2"> <p> 제공된 URL 수정자를 사용하여 fxg를 렌더링할 때 발생하는 오류를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨텐트</span> </p> </td> 
   <td colname="col2"> <p> 가 있는 모든 요소의 xml 목록을 반환합니다. <span class="codeph"> s7:element</span> 속성 값 및 fxg 문서의 모든 페이지 목록 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>다음 위치의 XML 목록을 반환합니다. <span class="codeph"> &lt;richtext /&gt;</span> 요소가 과도하게 설정되었습니다. </p> <p>다음 XML 목록을 반환합니다. <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 클라이언트측에서 처리하기 위해 오버세트 된 요소입니다. 전용 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 넘치는 요소가 반환됩니다. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> 은(는) 필수입니다. <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 속성(을 사용할 때) <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. 임의 초과 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 가 없는 요소 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> 나열되지 않습니다. 각 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 목록의 요소에는 <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>오버세트 텍스트 프레임의 테두리 상자 다음 <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> 속성은 프레임에 텍스트를 맞출 수 있었던 스토리의 텍스트 인덱스를 나타냅니다. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> 에만 적용됩니다. <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 요청한 FXG의 요소입니다. 나열되지 않습니다 <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> 모든 포함된 FXG의 요소입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 존재</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=존재[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>reqId 고유 요청 식별자 </p> <p>catalogRecord.exists라는 단일 속성을 반환합니다. 지정된 카탈로그 항목이 이미지 또는 기본 카탈로그에 있는 경우 속성 값은 "1"로 설정되고, 그렇지 않은 경우 속성 값은 "0"으로 설정됩니다. /is/content 컨텍스트에 대한 req=exists 요청은 정적 콘텐츠 카탈로그에 지정된 레코드가 있는지 여부를 나타냅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
