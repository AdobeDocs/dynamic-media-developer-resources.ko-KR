---
description: 지정된 서버 디렉터리에서 파일을 정기적으로 업로드합니다.
solution: Experience Manager
title: 업로드 디렉터리 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a23f1bc2-aa6a-4c1d-aab5-7f6dbd08682c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---

# [!DNL UploadDirectoryJob]{#uploaddirectoryjob}

지정된 서버 디렉터리에서 파일을 정기적으로 업로드합니다.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>자동 이미지 자르기 옵션(색상 기준). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>업로드된 파일에 적용할 자동 집합 생성 스크립트의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>투명도에 따라 이미지 가장자리에서 공백을 제거합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>업로드 중에 지정할 수 있는 옵션입니다. 세트는 업로드에 대해 색상이 관리되는 방식에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>업로드할 때 마스크를 만들지 여부입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>파일에 대한 IPS 폴더. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>이메일 설정 선택. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Illustrator 파일을 이미지 서버에 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>업로드할 때 하위 폴더를 포함할지 여부입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:InDesignOptions</span> </td> 
   <td colname="col3"> <p>서버에 InDesign 파일을 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 녹아웃 배경</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:녹아웃 배경 옵션</span> </td> 
   <td colname="col3"> <p>선택한 이미지에 대해 배경을 마스크합니다. 이렇게 하면 피사체 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. </p> <p>선택적. </p> <p><a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>수동 이미지 자르기 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:MediaOptions</span> </td> 
   <td colname="col3"> <p>비디오에서 썸네일 이미지를 설정할 수 있는 옵션입니다. </p> <p><a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 덮어쓰기</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>파일 업로드 덮어쓰기 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:PDFOptions</span> </td> 
   <td colname="col3"> <p>이미지 서버에 PDF 파일을 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>Photoshop 파일을 이미지 서버에 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>파일 업로드 대상 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>작업 </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행되는 이미지 렌더링 게시 작업에 대한 세부 정보입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행되는 이미지 제공 게시 작업에 대한 세부 정보입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>파일만 업로드할지 여부입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>이미지 서버에 포스트 스크립트 파일을 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>업로드가 완료된 후 실행되는 비디오 게시 작업에 대한 세부 정보입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>기존 자르기 정의의 유지를 제어합니다. 기본값은 true입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>덮어쓸 때 기존 에셋의 게시 상태를 유지할지 여부를 제어합니다. 설정하지 않으면 회사 기본 설정이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>이 작업에 대해 별도의 메타데이터 XML 파일을 처리할지 여부입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 형식:HandleArray</span> </td> 
   <td colname="col3"> <p>프로젝트 핸들의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>파일을 게시할 준비가 된 것으로 표시할지 여부를 결정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Source 업로드 디렉터리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 형식:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>이러한 선택적 설정을 사용하여 업로드된 TAR/ZIP 파일의 컨텐츠를 추출하고 처리합니다. </p> <p><a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>최적화된 피라미드 TIF 파일을 만들 때 언샵 마스크 설정을 제어할 수 있는 옵션입니다. 이러한 설정을 사용하여 이미지 선명도를 개선합니다. </p> <p><a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>업로드 작업의 모든 항목에 대한 추가 메타데이터 옵션 </p> </td> 
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
