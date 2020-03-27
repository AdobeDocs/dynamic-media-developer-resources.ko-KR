---
description: 이전에 업로드한 파일의 인증된 내보내기를 허용하는 작업 유형입니다.
seo-description: 이전에 업로드한 파일의 인증된 내보내기를 허용하는 작업 유형입니다.
seo-title: 내보내기 작업
solution: Experience Manager
title: 내보내기 작업
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# 내보내기 작업{#exportjob}

이전에 업로드한 파일의 인증된 내보내기를 허용하는 작업 유형입니다.

ExportJob은 다음 자산 유형을 지원하지 않습니다.

* 이미지 집합
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
   <td colname="col1"> <p> <span class="codeph"> assetHandleArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>내보내야 <span class="codeph"> 하는</span> 자산 핸들 목록입니다. HandleArray <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열 </span> </p> </td> 
   <td colname="col3"> <p>내보내기 유형을 지정합니다.가능한 <span class="codeph"> 값</span>:[방향, 변환] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">fmt <span class="codeph"> =orig</span>경우 에셋이 원본으로 내보내집니다 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">fmt=convert <span class="codeph"> 인</span>경우 자산은 <span class="codeph"> is_modifer</span> 또는 <span class="codeph"> 매크로</span> 입력 매개 변수에 지정된 형식으로 변환됩니다 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열 </span> </p> </td> 
   <td colname="col3"> <p>ExportJob <span class="codeph"> 변환</span> 요청에 추가되는 ImageServer 렌더링 URL 문자열을 지정합니다 <span class="codeph"></span> . </p> <p>IS 수정자 <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/" scope="external" format="html"> 전송에 대한 자세한 내용은 IS 설명서를</a> 참조하십시오. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 매크로</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열 </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 이메일 <span class="varname"> 설정</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열 </span> </p> </td> 
   <td colname="col3"> <p>이메일 설정 선택 가능한 값: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> 모두</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> 오류</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> 작업 완료</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> 없음</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열 </span> </p> </td> 
   <td colname="col3"> <p>내보내기 요청을 시작한 클라이언트 또는 고객의 IP 주소를 지정합니다. </p> <p> <p>참고: 이 매개 변수는 현재 적극적으로 채워지지 않으며 향후 사용으로만 엄격하게 예약됩니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

ExportJob 요청의 경우 `fmt=convert` 및 `is_modifier` 둘 다 `macro` 제공되면 대상 파일은 에서 `macro`제공하는 형식을 따릅니다. 예:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

