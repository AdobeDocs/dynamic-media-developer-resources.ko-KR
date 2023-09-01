---
title: RipPdf작업
description: 기존 PDF 에셋을 다시 가져오는 프로세스입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---

# [!DNL RipPdfsJob]{#rippdfsjob}

기존 PDF 에셋을 다시 가져오는 프로세스입니다.

>[!NOTE]
>
>이 작업 유형은 더 이상 사용되지 않습니다. 다음으로 전환 `ReprocessAssetsJob` 모든 향후 통합.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>리핑할 PDF 파일 배열에 대해 처리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:부울</span> </p> </td> 
   <td colname="col3"> <p>마스크를 만들지 여부를 결정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>수동 자르기 옵션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 자동 색상 자르기 옵션</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:자동 색상 자르기 옵션</span> </p> </td> 
   <td colname="col3"> <p>자동 자르기 옵션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 자동 투명 자르기 옵션</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScript 옵션</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:색상 관리 옵션</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>프로젝트 핸들의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSettings</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>이메일 설정. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>파일을 업로드할 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행할 이미지 제공 게시 작업에 대한 작업 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행할 이미지 렌더링 게시 작업에 대한 작업 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행할 비디오 게시 작업에 대한 작업 세부 정보. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignoptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Adobe InDesign 파일을 이미지 서버에 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 녹아웃 배경</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:녹아웃BackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>선택한 이미지에 대해 배경을 마스크합니다. 이 기능을 사용하면 대상 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. </p> <p>선택적. </p> <p>다음을 참조하십시오<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> 녹아웃 배경 옵션</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 주의 {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

다음에 대한 선택 사항: `*CropOptions` 포함:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

다음에 대한 선택 사항: `*PublishJob` 포함:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
