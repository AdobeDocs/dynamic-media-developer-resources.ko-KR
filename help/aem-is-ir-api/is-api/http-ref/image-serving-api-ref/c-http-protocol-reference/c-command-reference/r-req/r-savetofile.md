---
description: 이미지를 파일에 저장합니다.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---

# saveToFile{#savetofile}

이미지를 파일에 저장합니다.

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 파일</span> </p> </td> 
  <td class="stentry"> <p>대상 이미지 파일의 상대 경로입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>시간 제한 간격(밀리초). </p></td> 
 </tr> 
</table>

응답 이미지를 클라이언트에 반환하지 않고 서버의 파일에 저장합니다.

저장 요청이 성공적으로 완료되면, 요청은 다음을 포함하여 몇 가지 Java 형식 속성을 반환합니다.

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 속성</b> </th> 
   <th class="entry"> <b> 유형</b> </th> 
   <th class="entry"> <b> 설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p>파일 생성 시간(1970년 1월 1일 자정 이후 밀리초 수 UTC/GMT ) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 저장된 이미지의 픽셀 수. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> </span> doneif successful. </p> </td> 
  </tr> 
 </tbody> 
</table>

성공하면 HTTP 응답 상태 200을 반환하고, 요청이 실패하거나 시간이 초과되면 403을 반환합니다. 응답에 MIME 유형 `text/plain`이(가) 있으며 캐시할 수 없습니다.

중요 `attribute::SavePath`에 기존 쓰기 가능 폴더의 경로를 지정하여 파일에 저장을 사용하도록 설정해야 합니다. `saveToFile=` 가 비어  `attribute::SavePath` 있으면 실패합니다.

*`file`* 는 필수이며 와 결합되는 상대 경로여야 합니다 `attribute::SavePath`. 이미지 제공에서 폴더를 만들지 않습니다. 대상 폴더가 서버에 있어야 하며, 파일을 만들려면 이미지 제공 서비스에 대한 적절한 권한 설정이 있어야 합니다.

`timeout=` 은 선택 사항입니다. 기본 시간 제한은 60,000밀리초 또는 `PS::SaveTimeout`로 구성된 값
