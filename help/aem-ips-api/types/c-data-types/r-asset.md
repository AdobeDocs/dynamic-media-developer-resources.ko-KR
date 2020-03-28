---
description: 폴더 계층 구조의 개체 또는 컨테이너입니다.
seo-description: 폴더 계층 구조의 개체 또는 컨테이너입니다.
seo-title: 자산
solution: Experience Manager
title: 자산
topic: Scene7 Image Production System API
uuid: 758ac593-98d8-4366-a723-a06435c7fd3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 자산{#asset}

폴더 계층 구조의 개체 또는 컨테이너입니다.

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
   <td colname="col1"> <span class="codeph"> Aco <span class="varname"> Info</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 애니메이션 <span class="varname"> GifInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AnimatedGifInfo</span> </td> 
   <td colname="col3"> 애니메이션 GIF 파일에 대한 세부 사항. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자산 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> assetSetInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 캐비닛</span> 정보 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:CabinetInfo</span> </td> 
   <td colname="col3"> 캐비닛 자산 유형의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 작성일</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 자산이 업로드된 날짜 및 시간입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 사용자 <span class="varname"> 만들기</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산을 만든 사용자의 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cssInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:CssInfo</span> </td> 
   <td colname="col3"> CSS 파일에 대한 세부 사항. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> cuePointInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excelInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 파일 <span class="varname"> 이름</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">가상 파일 이름을 반환합니다. 전체 가상 파일 경로는 <span class="codeph"> 폴더</span>+<span class="codeph"> fileName입니다</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> flashInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 폴더</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산이 포함된 폴더. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 폴더 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산의 상위 폴더를 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> fontInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> 글꼴 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> icc <span class="varname"> ProfileInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:IccProfileInfo</span> </td> 
   <td colname="col3"> ICC 프로필 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> illustrator <span class="varname"> 정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageInfo</span> </td> 
   <td colname="col3"> 이미지 자산에 대한 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> inDesign <span class="varname"> Info</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ips <span class="varname"> ImageUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산의 축소판 보기를 나타내는 상대적 URL입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:JavascriptInfo</span> </td> 
   <td colname="col3"> JavaScript 파일에 대한 세부 사항. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 마지막 <span class="varname"> 수정</span> 날짜 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 자산을 마지막으로 수정한 날짜 및 시간입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 마지막 <span class="varname"> 수정</span> 사용자 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산을 마지막으로 수정한 사용자의 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> layerViewInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:LayerViewInfo</span> </td> 
   <td colname="col3"> 레이어 보기 에셋의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 마스크 <span class="varname"> 정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> masterVideoInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> metadataArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:MetadataArray</span> </td> 
   <td colname="col3"> 자산과 연결된 메타데이터 값의 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> pdf <span class="varname"> 정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> pdf <span class="varname"> SettingsInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF 설정 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 권한</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScriptInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> PowerPoint <span class="varname"> Info</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> premiereExpressInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 프로젝트</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 프로젝트 이름 목록입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> psdInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 게시 <span class="varname"> 준비</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 자산을 게시할지 여부를 나타내는 플래그를 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> renderSceneInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:RenderSceneInfo</span> </td> 
   <td colname="col3"> 렌더링 장면 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> rtf <span class="varname"> 정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 하위 <span class="varname"> 유형</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">하위 유형 값(예: AssetSet)을 지원하는 일반 자산 하위 <span class="codeph"> 유형입니다</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> svgInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:SvgInfo</span> </td> 
   <td colname="col3"> SVG 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:SwcInfo</span> </td> 
   <td colname="col3"> SWC 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 템플릿 <span class="varname"> 정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:TemplateInfo</span> </td> 
   <td colname="col3"> 템플릿 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 휴지통 <span class="varname"> 상태</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 자산이 휴지통 또는 live에 있는지 여부를 나타냅니다(값은 "휴지통 상태" 참조). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 유형</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">자산 유형. 값은 <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> 자산</a> 유형을 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 비디오 <span class="varname"> 캡션</span> 정보 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>비디오 캡션 자산의 속성입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 비디오 <span class="varname"> 정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> <p>비디오 자산의 속성입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> viewerPresetInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ViewerPresetInfo</span> </td> 
   <td colname="col3"> 뷰어 사전 설정 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> viewer <span class="varname"> SwfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ViewerSwfInfo</span> </td> 
   <td colname="col3"> 뷰어 SWFf 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vignetteInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VignetteInfo</span> </td> 
   <td colname="col3"> 비네팅 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> watermarkInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:WatermarkInfo</span> </td> 
   <td colname="col3"> 워터마크 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 창 <span class="varname"> 덮기정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:WindowCoveringInfo</span> </td> 
   <td colname="col3"> 자산을 포함하는 창의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Word <span class="varname"> Info</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:XmlInfo</span> </td> 
   <td colname="col3"> XML 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> xslInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:XslInfo</span> </td> 
   <td colname="col3"> XSL 자산의 속성입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> zip <span class="varname"> 정보</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

