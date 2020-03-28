---
description: getActiveJobs를 사용하여 데스크톱 업로드를 추적합니다.
seo-description: getActiveJobs를 사용하여 데스크톱 업로드를 추적합니다.
seo-title: UploadPostJob
solution: Experience Manager
title: UploadPostJob
topic: Scene7 Image Production System API
uuid: 172f47c7-685a-4014-9c30-dacd78733655
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UploadPostJob{#uploadpostjob}

getActiveJobs를 사용하여 데스크톱 업로드를 추적합니다.

HTTP [POST를 통해 업로드에 자산 업로드...를 참조하십시오.](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>업로드 작업에 대한 모든 POST 요청은 동일한 IP 주소에서 발생해야 합니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col03" class="entry"> <p>필수? </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자동 <span class="varname"> 색상 자르기 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoColorCropOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>색상을 기반으로 한 이미지 자동 자르기 옵션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoSetCreateOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>업로드된 파일에 적용할 자동 세트 생성 스크립트 배열 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자동 <span class="varname"> 투명한 자르기 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoTransparentCropOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>투명도를 기반으로 이미지 가장자리에서 공백을 제거합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 색상 <span class="varname"> 관리옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ColorManagementOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>업로드 중에 지정할 수 있는 옵션입니다. 이 설정은 업로드에 대한 색상 관리 방식에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 마스크 <span class="varname"> 만들기</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>예</b> </p> </td> 
   <td colname="col3"> <p>마스크를 만들지 여부를 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 이메일 <span class="varname"> 설정</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col03"> <p><b>예</b> </p> </td> 
   <td colname="col3"> <p>이메일 설정 선택 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> inDesign <span class="varname"> Options</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:InDesignOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>InDesign 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Illustrator <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:IllustratorOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>Illustrator 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 녹아웃</span> 배경 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:KnockoutBackgroundOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>선택한 이미지의 배경을 마스크합니다. 따라서 피사체 이미지 외부의 투명도와 함께 다른 레이어에 오버레이할 수 있습니다. 선택 사항입니다. </p> <p>KnockoutBackgroundOptions를<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 수동 <span class="varname"> 자르기 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ManualCropOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>수동 이미지 자르기 옵션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 미디어 <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:MediaOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>비디오에서 축소판 이미지를 설정할 수 있는 옵션입니다. </p> <p>MediaOptions <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 덮어쓰기</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>예</b> </p> </td> 
   <td colname="col3"> <p>업로드할 때 파일을 덮어쓸지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> pdf <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PDFOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>PDF 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> photoshop <span class="varname"> Options</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PhotoshopOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>Photoshop 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postHttpUrl <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>파일이 업로드되는 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScript <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PostScriptOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>Post Script 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자르기 <span class="varname"> 보존</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>기존 자르기 정의의 보존을 제어합니다. 기본값은 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> PublishState <span class="varname"> 유지</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>예</b> </p> </td> 
   <td colname="col3"> <p>덮어쓸 때 기존 자산의 게시 상태가 유지되는지 여부를 제어합니다. 설정하지 않으면 회사 기본 설정이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> projectHandleArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>프로젝트 핸들의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 게시 <span class="varname"> 준비</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col03"> <p><b>예</b> </p> </td> 
   <td colname="col3"> <p>파일을 게시할 준비가 되었는지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 압축 <span class="varname"> 해제</span> 옵션 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UnCompressOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>이러한 선택적 설정을 사용하여 업로드된 TAR/ZIP 파일의 컨텐츠를 추출하고 처리할 수 있습니다. </p> <p>UnCompressOptions <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> unsharpMaskOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UnsharpMaskOptions</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>최적화된 피라미드 TIF 파일을 만들 때 언샵 마스크 설정을 제어할 수 있는 옵션. 이러한 설정을 사용하여 이미지 선명도를 향상시킬 수 있습니다. </p> <p>UnsharpMaskOptions <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col03"> <p>아니요 </p> </td> 
   <td colname="col3"> <p>업로드 작업의 모든 항목에 대한 추가 메타데이터 옵션입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

