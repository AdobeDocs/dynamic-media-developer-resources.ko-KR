---
description: 작업 유형을 사용하여 PDF 리핑 및 이미지 재최적화를 포함하여 이전에 업로드한 마스터 파일을 재처리할 수 있습니다.
seo-description: 작업 유형을 사용하여 PDF 리핑 및 이미지 재최적화를 포함하여 이전에 업로드한 마스터 파일을 재처리할 수 있습니다.
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
topic: Scene7 Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ReprocessAssetsJob{#reprocessassetsjob}

작업 유형을 사용하여 PDF 리핑 및 이미지 재최적화를 포함하여 이전에 업로드한 마스터 파일을 재처리할 수 있습니다.

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
   <td colname="col1"> <p><span class="codeph"> assetHandleArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>자산 핸들. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 게시 <span class="varname"> 준비</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>파일을 게시할 준비가 되었는지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> PublishState <span class="varname"> 유지</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>덮어쓸 때 기존 자산의 게시 상태가 유지되는지 여부를 제어합니다. 설정하지 않으면 회사 기본 설정이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 마스크 <span class="varname"> 만들기</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>마스크를 만들지 여부를 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 자르기 <span class="varname"> 보존</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3">기존 자르기 정의의 보존을 제어합니다. 기본값은 <span class="codeph"> true입니다</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 수동 <span class="varname"> 자르기 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>수동 자르기 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 자동 <span class="varname"> 색상 자르기 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>색상을 기반으로 한 이미지 자동 자르기 옵션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 자동 <span class="varname"> 투명한 자르기 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>투명도를 기반으로 이미지 가장자리에서 공백을 제거합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> photoshop <span class="varname"> Options</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PhotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Photoshop 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postScript <span class="varname"> 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>PostScript 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> pdf <span class="varname"> 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>PDF 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 미디어 <span class="varname"> 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V 미디어 파일 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Illustrator <span class="varname"> 옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Illustrator 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 색상 <span class="varname"> 관리옵션</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>업로드 중에 지정할 수 있는 옵션입니다. 이 설정은 업로드에 대한 색상 관리 방식에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>업로드된 파일에 적용할 자동 세트 생성 스크립트 배열 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> projectHandleArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>프로젝트 핸들의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 이메일 <span class="varname"> 설정</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>이메일 설정 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postJobOnlyIfFiles <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>파일만 업로드할지 여부. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postHttpUrl <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>파일 업로드 위치에 대한 URL. </p> </td> 
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
   <td colname="col3"> <p>InDesign 파일을 이미지 서버에 업로드하기 위한 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 녹아웃</span> 배경 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>선택한 이미지의 배경을 마스크합니다. 따라서 피사체 이미지 외부의 투명도와 함께 다른 레이어에 오버레이할 수 있습니다. </p> <p>선택 사항입니다. </p> <p>KnockoutBackgroundOptions<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 참조</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> unsharpMaskOptions <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>최적화된 피라미드 TIF 파일을 만들 때 언샵 마스크 설정을 제어할 수 있는 옵션. 이러한 설정을 사용하여 이미지 선명도를 향상시킬 수 있습니다. </p> <p>UnsharpMaskOptions <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> 를 참조하십시오</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**주의**

선택 `*CropOptions` 사항은 다음과 같습니다.

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

선택 `*PublishJob` 사항은 다음과 같습니다.

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

