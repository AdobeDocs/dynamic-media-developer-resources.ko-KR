---
description: 파일에 이미지를 저장합니다.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# saveToFile{#savetofile}

파일에 이미지를 저장합니다.

`req=saveToFile&name= *`파일`*[&timeout= *`val`*]`

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

저장 요청이 성공적으로 완료되면 요청은 다음을 포함하여 여러 Java 형식 속성을 반환합니다.

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
   <td> <p> <span class="codeph"> 마지막 업데이트 날짜</span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p>파일 생성 시간(1970년 1월 1일 자정 이후 밀리초 수 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> 픽셀 합계</span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 저장된 이미지의 픽셀 수. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 완료</span> 성공하면 </p> </td> 
  </tr> 
 </tbody> 
</table>

요청이 실패하거나 시간 초과되면 HTTP 응답 상태 200 및 403을 반환합니다. 응답에 MIME 유형이 있습니다. `text/plain` 및 는 캐시 불가능 입니다.

중요 파일에 저장을 사용하려면 의 쓰기 가능한 기존 폴더에 대한 경로를 지정해야 합니다. `attribute::SavePath`. `saveToFile=` 다음과 같은 경우 실패 `attribute::SavePath` 은(는) 비어 있습니다.

*`file`* 는 필수이며 와 결합된 상대 경로여야 합니다. `attribute::SavePath`. 이미지 제공에서는 폴더를 만들지 않습니다. 대상 폴더는 서버에 있어야 하며 이미지 제공에서 파일을 만들 수 있는 적절한 권한 설정이 있어야 합니다.

`timeout=` 는 선택 사항입니다. 기본 시간 제한은 60,000밀리초 또는 어느 값이든 구성된 값입니다. `PS::SaveTimeout`.
