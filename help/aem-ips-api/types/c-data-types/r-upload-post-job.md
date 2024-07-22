---
description: getActiveJobs를 사용하여 데스크탑 업로드를 추적합니다.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 5%

---

# [!DNL UploadPostJob]{#uploadpostjob}

getActiveJobs를 사용하여 데스크탑 업로드를 추적합니다.

[HTTP POST를 통해 자산을 업로드에 업로드하는 중...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d)도 참조하세요.

>[!NOTE]
>
>업로드 작업에 대한 모든 POST 요청은 동일한 IP 주소에서 가져와야 합니다.

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수? </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>색상을 기반으로 이미지 자동 자르기에 대한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>업로드된 파일에 적용할 자동 집합 생성 스크립트의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>투명도에 따라 이미지 가장자리에서 공백을 제거합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>업로드 중에 지정할 수 있는 옵션입니다. 세트는 업로드에 대해 색상이 관리되는 방식에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>예</b> </p> </td> 
   <td colname="col4"> <p>마스크 만들기 여부입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>예</b> </p> </td> 
   <td colname="col4"> <p>이메일 설정 선택. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:InDesignOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>이미지 서버에 InDesign 파일을 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>Illustrator 파일을 이미지 서버에 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 녹아웃 배경</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:녹아웃 배경 옵션</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>선택한 이미지에 대해 배경을 마스크합니다. 이렇게 하면 피사체 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. 선택적. </p> <p><a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>수동 이미지 자르기 옵션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:MediaOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>비디오에서 썸네일 이미지를 설정할 수 있는 옵션입니다. </p> <p><a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 덮어쓰기</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>예</p> </td> 
   <td colname="col4"> <p>업로드할 때 파일을 덮어쓸지 여부입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:PDFOptions</span> </td> 
   <td colname="col3"> <p>아니요</p> </td> 
   <td colname="col4"> <p>이미지 서버에 PDF 파일을 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:PhotoshopOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>Photoshop 파일을 이미지 서버에 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>파일을 업로드하는 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>이미지 서버에 사후 스크립트 파일을 업로드하기 위한 옵션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>기존 자르기 정의의 유지를 제어합니다. 기본값은 true입니다.</p> <p>manualCropOptions 매개 변수와 해당 값을 제공하면 preserveCrop 값에 관계없이 새 값(0,0,0,0 제외)이 자산에 적용됩니다.</p><p><i>not</i>에서 manualCropOptions 매개 변수를 제공하면 preserveCrop의 값이 유지됩니다. 그리고 true인 경우에는 기존 preserveCrop 값이 유지되고, false인 경우에는 preserveCrop 값이 제거됩니다.</p><p>예:</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>예</b> </p> </td> 
   <td colname="col4"> <p>덮어쓸 때 기존 에셋의 게시 상태를 유지할지 여부를 제어합니다. 설정하지 않으면 회사 기본 설정이 사용됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 형식:HandleArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>프로젝트 핸들의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>예</b> </p> </td> 
   <td colname="col4"> <p>파일을 게시할 준비가 되었다고 표시할지 여부입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 형식:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>이러한 선택적 설정을 사용하여 업로드된 TAR/ZIP 파일의 컨텐츠를 추출하고 처리합니다. </p> <p><a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph">개 유형:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>최적화된 피라미드 TIF 파일을 만들 때 언샵 마스크 설정을 제어할 수 있는 옵션입니다. 이러한 설정을 사용하여 이미지 선명도를 개선합니다. </p> <p><a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname">개의 xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>업로드 작업의 모든 항목에 대한 추가 메타데이터 옵션입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
