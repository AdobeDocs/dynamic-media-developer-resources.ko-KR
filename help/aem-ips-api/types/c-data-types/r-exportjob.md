---
description: 이전에 업로드한 파일의 인증된 내보내기를 허용하는 작업 유형입니다.
solution: Experience Manager
title: 내보내기 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 11%

---

# [!DNL ExportJob]{#exportjob}

이전에 업로드한 파일의 인증된 내보내기를 허용하는 작업 유형입니다.

ExportJob은 다음 자산 유형을 지원하지 않습니다.

* Image Sets
* 렌더 집합
* 회전 집합
* 미디어 집합
* 다중 비트 전송률 집합
* 비디오 집합
* eCatalog
* 오퍼 집합

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 유형:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>목록 <span class="codeph"> assetHandle</span> 내보내야 합니다. 자세한 내용은 <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL fmt]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>형식을 지정합니다. <span class="codeph"> export.Possible Values</span>: [원본, 변환] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">If <span class="codeph"> fmt=orig</span>로 지정하는 경우 자산이 원본으로 내보내집니다 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">If <span class="codeph"> fmt=convert</span>를 설정하는 경우 자산은 <span class="codeph"> is_modifer</span> 또는 <span class="codeph"> 매크로</span> 입력 매개 변수 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL is_modifier]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>을(를) 지정합니다. <span class="codeph"> ImageServer</span> ExportJob에 추가된 렌더링 URL 문자열 <span class="codeph"> 전환</span> 요청. </p> <p>자세한 내용은 <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/homeisir.html" scope="external" format="html"> IS 설명서</a> is 수정자 전송에 대한 자세한 내용은 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL macro]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>이메일 설정 선택. 가능한 값: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> 모두</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> 오류</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> 작업 완료</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> 없음</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL clientId]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>내보내기 요청을 시작한 클라이언트 또는 고객의 IP 주소를 지정합니다. </p> <p> <p>참고: 이 매개 변수는 현재 적극적으로 채워지지 않으며 향후 사용에만 사용하도록 엄격히 예약되어 있습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

ExportJob 요청의 경우 `fmt=convert` 둘 다 `is_modifier` 및 `macro` 제공된 경우 대상 파일은 `macro`. For example:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
