---
description: 이미지를 파일에 저장합니다.
seo-description: 이미지를 파일에 저장합니다.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# saveToFile{#savetofile}

이미지를 파일에 저장합니다.

`req=saveToFile&name= *``*[&timeout= *`파일`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 파일</span> </p> </td> 
  <td class="stentry"> <p>대상 이미지 파일의 상대 경로입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>시간 초과 간격(밀리초). </p></td> 
 </tr> 
</table>

응답 이미지를 클라이언트에 반환하는 대신 서버의 파일에 저장합니다.

저장 요청이 성공적으로 완료되면 다음을 포함하여 여러 Java 형식 속성을 반환합니다.

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
   <td> <p>파일 생성 시간(1970년 1월 1일 자정 이후 UTC/GMT 이후 밀리초) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 정수 </p> </td> 
   <td> <p> 저장된 이미지의 픽셀 수입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 성공 </span> 시 </p> </td> 
  </tr> 
 </tbody> 
</table>

HTTP 응답 상태 200은 성공한 경우 반환하고 요청이 실패하거나 시간 초과된 경우 403을 반환합니다. 응답에 MIME 유형 `text/plain`이(가) 있으며 액세스할 수 없습니다.

`attribute::SavePath`에 기존 쓰기 가능 폴더에 대한 경로를 지정하여 파일에 저장을 활성화해야 합니다. `saveToFile=` 가  `attribute::SavePath` 비어 있으면 실패합니다.

*`file`* 은 필수이며 와 결합된 상대 경로여야 합니다 `attribute::SavePath`. 이미지 제공은 폴더를 만들지 않습니다. 대상 폴더가 서버에 있어야 하며 파일을 만들려면 이미지 제공을 위한 적절한 권한 설정이 있어야 합니다.

`timeout=` 은 선택 사항입니다. 기본 시간 제한은 60,000초 또는 `PS::SaveTimeout`으로 구성된 값 중 어느 것이든 입니다.
