---
description: 폴더 계층의 개체 또는 컨테이너입니다.
solution: Experience Manager
title: 자산
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 943e653a-ed30-4c75-9bad-6ef5b72f5219
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---

# [!DNL Asset]{#asset}

폴더 계층의 개체 또는 컨테이너입니다.

구문

## 매개 변수 {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL acoInfo]</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL animatedGifInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AnimatedGifInfo</span> </td> 
   <td colname="col3"> 애니메이션 GIF 파일에 대한 세부 정보. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 에셋 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetSetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cabinetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:CabinetInfo</span> </td> 
   <td colname="col3"> 캐비닛 자산 유형에 대한 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL created]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 에셋이 업로드된 날짜 및 시간입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL createUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 에셋을 만든 사용자의 이메일 주소. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cssInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:CssInfo</span> </td> 
   <td colname="col3"> CSS 파일에 대한 세부 정보. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cuePointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL excelInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fileName]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">가상 파일 이름을 반환합니다. 전체 가상 파일 경로는 <span class="codeph"> 폴더</span>+<span class="codeph"> fileName</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL flashInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 에셋이 포함된 폴더입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folderHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 자산의 상위 폴더로 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fontInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> 글꼴 자산에 대한 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL iccProfileInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:IccProfileInfo</span> </td> 
   <td colname="col3"> ICC 프로파일 자산에 대한 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL illustratorInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL imageInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:이미지 정보</span> </td> 
   <td colname="col3"> 이미지 자산에 대한 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL inDesignInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL ipsImageUrl]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 에셋의 썸네일 보기를 나타내는 상대 URL입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL javascriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:JavascriptInfo</span> </td> 
   <td colname="col3"> JavaScript 파일에 대한 세부 정보. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModified]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 에셋을 마지막으로 수정한 날짜 및 시간입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModifyUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 에셋을 마지막으로 수정한 사용자의 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL layerViewInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:LayerViewInfo</span> </td> 
   <td colname="col3"> 레이어 보기 자산에 대한 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL masterVideoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL metadataArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:MetadataArray</span> </td> 
   <td colname="col3"> 자산과 연결된 메타데이터 값의 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL name]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 에셋 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfSettingsInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF 설정 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL permissions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL postScriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL powerPointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL premiereExpressInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL projects]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 프로젝트 이름 목록입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL psdInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3"> 자산을 게시할지 여부를 나타내는 플래그를 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL renderSceneInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:RenderSceneInfo</span> </td> 
   <td colname="col3"> 렌더링 장면 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL rtfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL subType]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">하위 유형 값을 지원하는 일반 자산 하위 유형(예: <span class="codeph"> 자산 집합</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL svgInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:SvgInfo</span> </td> 
   <td colname="col3"> SVG 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL swcInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:SwcInfo</span> </td> 
   <td colname="col3"> SWC 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL templateInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:TemplateInfo</span> </td> 
   <td colname="col3"> 템플릿 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL trashState]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 자산이 휴지통에 있는지 또는 라이브에 있는지 여부를 나타냅니다(값은 "휴지통 상태" 참조). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL type]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">자산 유형. 다음을 참조하십시오 <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> 자산 유형</a> 값. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoCaptionInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>비디오 캡션 자산의 속성입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> <p>비디오 자산의 속성입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerPresetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ViewerPresetInfo</span> </td> 
   <td colname="col3"> 뷰어 사전 설정 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerSwfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ViewerSwfInfo</span> </td> 
   <td colname="col3"> 뷰어 SWf 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL vignetteInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:비네팅 정보</span> </td> 
   <td colname="col3"> 비네팅 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL watermarkInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:WatermarkInfo</span> </td> 
   <td colname="col3"> 워터마크 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL windowCoveringInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:창 커버링 정보</span> </td> 
   <td colname="col3"> 자산을 포함하는 창의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL wordInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL xmlInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:XmlInfo</span> </td> 
   <td colname="col3"> XML 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:XslInfo</span> </td> 
   <td colname="col3"> XSL 자산 속성. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>
