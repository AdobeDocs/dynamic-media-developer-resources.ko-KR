---
description: 파일을 가져올 위치에서 URL을 업로드합니다.
seo-description: 파일을 가져올 위치에서 URL을 업로드합니다.
seo-title: UploadUrlJob
solution: Experience Manager
title: UploadUrlJob
topic: Scene7 Image Production System API
uuid: 6140e969-bf61-4b62-9a60-29609626b0b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 1%

---


# UploadUrlsJob{#uploadurlsjob}

파일을 가져올 위치에서 URL을 업로드합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoColorCropOptions</span> </td> 
   <td colname="col3"> 색상을 기반으로 이미지를 자동으로 자르는 옵션 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoSetCreationOptions</span> </td> 
   <td colname="col3"> 업로드된 파일에 적용할 자동 집합 생성 스크립트 배열. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> 투명도를 기반으로 이미지 가장자리에서 공백을 제거합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 마스크를 만들지 여부. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ColorManagementOptions</span> </td> 
   <td colname="col3"> 업로드 중에 지정할 수 있는 옵션입니다. 이 세트는 업로드에 대한 색상이 관리되는 방식에 영향을 줍니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 이메일 설정 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:IllustratorOptions</span> </td> 
   <td colname="col3"> 이미지 서버에 Illustrator 파일을 업로드하기 위한 옵션. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:InDesignOptions</span> </td> 
   <td colname="col3"> 서버에 InDesign 파일을 업로드하기 위한 옵션입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">선택한 이미지의 배경을 마스크합니다. 따라서 대상 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. 선택 사항입니다. <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>을(를) 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ManualCropOptions</span> </td> 
   <td colname="col3"> 수동으로 이미지 자르기를 위한 옵션. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:MediaOptions</span> </td> 
   <td colname="col3">비디오에서 축소판 이미지를 설정할 수 있는 옵션입니다. <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">작업에서 제출된 URL 수를 반환합니다. <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> 및 <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>에서 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 덮어쓰기</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 업로드할 때 파일을 덮어쓸지 여부. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PDFOptions</span> </td> 
   <td colname="col3"> 이미지 서버에 PDF 파일을 업로드하기 위한 옵션. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PhotoshopOptions</span> </td> 
   <td colname="col3"> 이미지 서버에 Photoshop 파일을 업로드하기 위한 옵션. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 파일이 업로드되는 URL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> 업로드가 완료된 후 실행되는 이미지 렌더링 게시 작업에 대한 세부 사항. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageServingPublishJob</span> </td> 
   <td colname="col3"> 모든 미디어 옵션. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PostScriptOptions</span> </td> 
   <td colname="col3"> 이미지 서버에 게시물 스크립트 파일을 업로드하기 위한 옵션. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VideoPublishJob</span> </td> 
   <td colname="col3"> 업로드가 완료된 후 실행되는 비디오 게시 작업에 대한 세부 정보입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 기존 자르기 정의의 보존을 제어합니다. 기본값은 true입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 덮어쓸 때 기존 에셋의 게시 상태가 유지되는지 여부를 제어합니다. 설정하지 않으면 회사 기본 설정이 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:HandleArray</span> </td> 
   <td colname="col3"> 프로젝트 핸들의 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 파일을 게시할 준비가 되었는지 여부. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UnCompressOptions</span> </td> 
   <td colname="col3">이러한 선택적 설정을 사용하여 업로드된 TAR/ZIP 파일의 내용을 추출하고 처리할 수 있습니다. <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UnsharpMaskOptions</span> </td> 
   <td colname="col3">최적화된 피라미드 TIF 파일을 만들 때 언샵 마스크 설정을 제어할 수 있는 옵션. 이 설정을 사용하여 이미지 선명도를 향상시킬 수 있습니다. <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> 업로드할 URL 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>업로드 작업의 모든 항목에 대한 추가 메타데이터 옵션입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 주의 {#section-637405ff7e0b4a71b83fd359b92fa0c2}

`CropOptions`의 경우 다음 중 하나만 선택할 수 있습니다.

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

`PublishJob`의 경우 다음 중 하나만 선택할 수 있습니다.

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

