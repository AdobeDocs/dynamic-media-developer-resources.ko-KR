---
description: 기존 PDF 에셋을 리플로우하는 프로세스입니다.
seo-description: 기존 PDF 에셋을 리플로우하는 프로세스입니다.
seo-title: RipPdfs작업
solution: Experience Manager
title: RipPdfs작업
topic: Scene7 Image Production System API
uuid: 95990d53-4baf-44a2-8d84-3cab2b5c9105
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RipPdfs작업{#rippdfsjob}

기존 PDF 에셋을 리플로우하는 프로세스입니다.

>[!NOTE]
>
>이 작업 유형은 더 이상 사용되지 않습니다. 모든 향후 통합을 위해 전환할 `ReprocessAssetsJob` 수 있습니다.

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
   <td colname="col1"> <p><span class="codeph"> pdf <span class="varname"> HandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>리핑할 PDF 파일의 배열을 처리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 마스크 <span class="varname"> 만들기</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>마스크를 만들지 여부를 결정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 수동 <span class="varname"> 자르기 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>수동 자르기 옵션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 자동 <span class="varname"> 색상 자르기 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>자동 자르기 옵션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 자동 <span class="varname"> 투명한 자르기 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postScript <span class="varname"> 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> pdf <span class="varname"> 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> illustrator <span class="varname"> 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 색상 <span class="varname"> 관리옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> projectHandleArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>프로젝트 핸들의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 이메일 <span class="varname"> 설정</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>이메일 설정. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postHttpUrl <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>파일이 업로드되는 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postImageServingPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행할 이미지 제공 게시 작업에 대한 작업 세부 정보입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postImageRenderingPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행할 이미지 렌더링 게시 작업에 대한 작업 세부 사항입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행할 비디오 게시 작업에 대한 작업 세부 정보입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> inDesign <span class="varname"> Options</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Adobe InDesign 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 녹아웃</span> 배경 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>선택한 이미지의 배경을 마스크합니다. 따라서 피사체 이미지 외부의 투명도와 함께 다른 레이어에 오버레이할 수 있습니다. </p> <p>선택 사항입니다. </p> <p>KnockoutBackgroundOptions<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 참조</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 주의 {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

선택 `*CropOptions` 사항은 다음과 같습니다.

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

선택 `*PublishJob` 사항은 다음과 같습니다.

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

