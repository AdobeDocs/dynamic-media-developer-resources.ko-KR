---
description: 지정된 서버 디렉토리에서 반복적으로 파일을 업로드합니다.
seo-description: 지정된 서버 디렉토리에서 반복적으로 파일을 업로드합니다.
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Scene7 Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# UploadDirectoryJob{#uploaddirectoryjob}

지정된 서버 디렉토리에서 반복적으로 파일을 업로드합니다.

구문

## 매개 변수 {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자동 <span class="varname"> 색상 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>자동 이미지 자르기 옵션(색상 기반). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>업로드된 파일에 적용할 자동 세트 생성 스크립트 배열 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자동 <span class="varname"> 투명한 자르기 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>투명도를 기반으로 이미지 가장자리에서 공백을 제거합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 색상 <span class="varname"> 관리옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>업로드 중에 지정할 수 있는 옵션입니다. 이 설정은 업로드에 대한 색상 관리 방식에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 마스크 <span class="varname"> 만들기</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>업로드할 때 마스크를 만들지 여부를 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dest</span> 폴더 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>파일의 IPS 폴더 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 이메일 <span class="varname"> 설정</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>이메일 설정 선택 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> illustrator <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>이미지 서버에 Illustrator 파일을 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 하위 폴더 <span class="varname"> 포함</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>업로드할 때 하위 폴더를 포함할지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> inDesign <span class="varname"> Options</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:InDesignOptions</span> </td> 
   <td colname="col3"> <p>서버에 InDesign 파일을 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 녹아웃</span> 배경 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>선택한 이미지의 배경을 마스크합니다. 따라서 피사체 이미지 외부의 투명도와 함께 다른 레이어에 오버레이할 수 있습니다. </p> <p>선택 사항입니다. </p> <p>KnockoutBackgroundOptions <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 수동 <span class="varname"> 자르기 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>수동 이미지 자르기 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 미디어 <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:MediaOptions</span> </td> 
   <td colname="col3"> <p>비디오에서 축소판 이미지를 설정할 수 있는 옵션입니다. </p> <p>MediaOptions <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 덮어쓰기</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>파일 업로드 덮어쓰기 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> pdf <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PDFOptions</span> </td> 
   <td colname="col3"> <p>PDF 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> photoshop <span class="varname"> Options</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>이미지 서버에 Photoshop 파일을 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postHttpUrl <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>파일 업로드 대상의 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postImageRendering게시 <span class="varname"></span> </span>작업 </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행되는 이미지 렌더링 게시 작업에 대한 세부 사항입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postImageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행되는 이미지 제공 게시 작업에 대한 세부 정보입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postJobOnlyIfFiles <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>파일만 업로드할지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScript <span class="varname"> 옵션</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Post Script 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행되는 비디오 게시 작업에 대한 세부 사항입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자르기 <span class="varname"> 보존</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>기존 자르기 정의의 보존을 제어합니다. 기본값은 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> PublishState <span class="varname"> 유지</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>덮어쓸 때 기존 자산의 게시 상태가 유지되는지 여부를 제어합니다. 설정하지 않으면 회사 기본 설정이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 프로세스 <span class="varname"> 메타데이터</span> 파일 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>이 작업에 대해 별도의 메타데이터 XML 파일을 처리할지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> projectHandleArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>프로젝트 핸들의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 게시 <span class="varname"> 준비</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>파일을 게시할 준비가 되었는지 확인합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> server <span class="varname"> Dir</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>소스 업로드 디렉토리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 압축 <span class="varname"> 해제</span> 옵션 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>이러한 선택적 설정을 사용하여 업로드된 TAR/ZIP 파일의 컨텐츠를 추출하고 처리할 수 있습니다. </p> <p>UnCompressOptions <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> unsharpMaskOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>최적화된 피라미드 TIF 파일을 만들 때 언샵 마스크 설정을 제어할 수 있는 옵션. 이러한 설정을 사용하여 이미지 선명도를 향상시킬 수 있습니다. </p> <p>UnsharpMaskOptions <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>업로드 작업의 모든 항목에 대한 추가 메타데이터 옵션 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 주의 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

의 `CropOptions`경우 다음 중 하나만 선택할 수 있습니다.

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

의 `PublishJob`경우 다음 중 하나만 선택할 수 있습니다.

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

