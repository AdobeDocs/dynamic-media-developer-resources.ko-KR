---
description: 이미지 자산의 속성입니다.
seo-description: 이미지 자산의 속성입니다.
seo-title: ImageInfo
solution: Experience Manager
title: ImageInfo
topic: Scene7 Image Production System API
uuid: 89138f10-c80b-49b8-886f-45b0960038b8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageInfo{#imageinfo}

이미지 자산의 속성입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 원본 <span class="varname"> 경로</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>원본 파일의 상대 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> originalFile</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>파일 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> optimizedPath</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>IPS에 최적화된 이미지 파일의 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 최적화된 <span class="varname"> 파일</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>IPS에 최적화된 이미지 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskPath</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>이미지의 마스크 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 마스크 <span class="varname"> 파일</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>마스크의 파일 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> width</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>이미지 너비(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> height</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>이미지 높이(픽셀 단위) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 파일 <span class="varname"> 크기</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>이미지 크기(바이트)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 해상도</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> <p>인치당 픽셀 수 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sku</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>제품 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 설명</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>이미지 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 댓글</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>댓글(더 이상 사용되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 사용자 <span class="varname"> 데이터</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>이미지와 연결된 사용자 정보(더 이상 사용되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 앵커 <span class="varname"> X</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>가로 기준점(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Y <span class="varname"> 앵커</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> <p>픽셀의 수직 고정점 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> url <span class="varname"> 수정자</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>이미지 서버 URL 매개 변수. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> url <span class="varname"> PostApplyModifier</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>url 수정자의 끝에 연결된 매개 <span class="codeph"> 변수입니다</span>. 이미지 서버에 대한 명령인 매개 변수의 쿼리 문자열 형식 목록입니다. 값은 이미지 서버 프로토콜 안내서에 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 확대/축소</span> 대상 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ZoomTargetArray</span> </td> 
   <td colname="col3"> <p>확대/축소 대상 배열(최대 5개). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 마스크</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:MaskArray</span> </td> 
   <td colname="col3"> <p>마스크 배열. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 이미지 <span class="varname"> 맵</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageMapsArray</span> </td> 
   <td colname="col3"> <p>이미지 맵 배열. </p> </td> 
  </tr> 
 </tbody> 
</table>

