---
description: IPS API v4.0의 새로운 변경 사항 및 구현된 변경 사항에 대해 설명합니다.
seo-description: IPS API v4.0의 새로운 변경 사항 및 구현된 변경 사항에 대해 설명합니다.
seo-title: 새로운 추가 및 변경 사항
solution: Experience Manager
title: 새로운 추가 및 변경 사항
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 새로운 추가 및 변경 사항{#new-additions-and-changes}

IPS API v4.0의 새로운 변경 사항 및 구현된 변경 사항에 대해 설명합니다.

별도의 WSDL 및 스키마 네임스페이스로 API 버전을 나란히 구현했습니다.

* 이전 API 버전: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`Adobe
* SPS 4.0 버전: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`Adobe

필드가 `PostScriptOptions/alpha` 추가되었습니다.

작업에 대한 `VideoRootUrl` 및 `SwfRootUrl` 속성이 `getProperty` 추가되었습니다.

호출 응용 프로그램을 추적할 선택적 `appName` 및 `appVersion` 매개 변수를 `authHeader` 추가했습니다. 로깅이 `ipsApiService.log`추가되었습니다.

WSDL 생성 서블릿에 선택적 `serviceUrl` 매개 변수를 추가했습니다. 특히 디버그 프록시에 유용합니다. 예: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

구현된 `getZipEntries` 작업.

시스템 필드 조건에 대한 검색 범위 및 입력 비교 값을 구현했습니다.

자산 유형 문자열 상수를 추가했습니다. 이 상수는 주로 자산 간 메타데이터 필드를 허용합니다. `'Asset'`

에 대한 `trashState` 매개 변수를 구현했습니다 `searchAssets`.

구현된 `getAssetPublishHistory` 작업.

선택적 SOAP `faultHttpStatusCode` 헤더를 추가하여 Flex에서 오류 처리를 활성화합니다. Flex의 경우 를 `<faultHttpStatusCode>200</faultHttpStatusCode>`사용하십시오. 오류 응답에 대한 기본 상태 코드는 `500 (Internal Server Error)`입니다.

휴지통에서 자산 및 휴지통에서 빈 자산을 복원하는 작업을 추가했습니다.

CRUD 작업을 구현했습니다.

유형 및 작업에 활성화된 플래그를 `ImageMap` 추가했습니다 `saveImageMap` .

나머지 파일 최적화 작업에 대한 지원이 추가되었습니다.

일괄 게시 상태 업데이트에 `setAssetsPublishState` 대해 추가되었습니다.

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

사용되지 않는 `saveMetadataField` 작업 대신 새 `createMetadataField` 및 `updateMetadataField` 작업을 수행합니다.

일괄 `deleteAssetsParam` 삭제 작업을 구현했습니다.

일괄 `moveAssetsParam` 이동 작업을 구현했습니다.

구현된 `deleteMetadataField` 작업.

구현된 `get/setImageRenderingPublishSettings`작업 `get/set/create/updateVignettePublishFormat` .

Implemented `getAssetCounts`.

자산에 구성원을 `setImageSetMembers` 포함하기 위한 지원이 `RenderSet` `ImageSet` 추가되었습니다.

작업이 `replaceImage` 추가되었습니다.

작업이 `copyImage` 추가되었습니다.

및 에 대한 `setUrlModifier` 작업 및 `urlModifier/urlPostApplyModifier` 필드를 `LayerViewInfo``TemplateInfo``WatermarkInfo`추가했습니다.

작업이 `createDerivedAsset` 추가되었습니다. 현재 `ownerHandle` 는 이미지 자산을 참조해야 하며 유형은 `AdjustedView` 또는 `LayerView`이어야 합니다.

작업이 `createTemplate` 추가되었습니다. 현재 이 매개 변수를 호출하여 템플릿 또는 워터마크 자산을 만들 수 있습니다.

IPS 회사 설정, `CompanySettings`웹 서비스 API로 포팅

작업에 `excludeByproducts` 필터 플래그를 `searchAssets` 추가했습니다. 이 플래그를 true로 설정하면 `PSDlayer` 이미지와 PDF 리플로우 이미지가 실행됩니다.

작업이 `getGenerationInfo` 추가되었습니다.

작업에 `SystemMessage` 속성 이름을 `getProperty` 추가했습니다.

해당 자산 정보 필드와 일치하도록 일부 자산 유형 문자열 상수를 수정했습니다.

* WordDoc:Word
* ExcelDoc:Excel
* PowerPointDoc:PowerPoint
* RTFDoc:Rtf

성공, 경고 및 오류를 요약하기 위해 일괄 처리 작업의 결과 형식을 수정했습니다.

일괄 `batchSetAssetMetadata` 메타데이터 작업을 구현했습니다.

앱별 데이터에 대한 지원을 구현했습니다.

Photoshop 처리 과정을 제어하기 위해 업로드 작업에 대한 부울 플래그 `createTemplate``extendLayers`및 `extractText` 에 대한 지원을 구현했습니다(파일 업로드 추가에 대한 변경과 유사).

구현 `setImageMaps` 및 `setZoomTargets` 운영

구현된 `ViewerPreset` 작업. 인식된 유형은 다음과 같습니다.

* `VideoPlayer` (비디오는 이러한 뷰어만 게시합니다.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

뷰어 스킨은 두 개의 매개 변수를 지원합니다. `skinFg` 및 `skinBg`Adobe 백엔드 코드는 이전 버전과의 호환성을 유지하는 데 필요한 모든 처리를 수행합니다.

구현된 `getAssociatedAssets` 작업.

PDF 리핑 및 이미지 재최적화를 포함하여 이전에 업로드한 마스터 파일의 재처리를 허용하도록 `ReprocessAssets` 작업 유형을 추가했습니다.

필드 `PropertySetType` 유형을 (으)로 `propertyType`변경했습니다. 이는 `createPropertySetType` 매개 변수 및 `getPropertySetType/getPropertySetTypes` 응답에 영향을 줍니다.

이미지 사용자 데이터 및 기타 편집 가능한 이미지 필드 설정을 지원하기 위한 `batchSetImageFields` 작업을 구현했습니다.

47 다양한 자산 정보 유형에 fileSize 필드를 추가했습니다.

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

구현된 `getActivePublishContexts` 작업. 이 작업은 지정된 회사에 대해 활성 게시 서버가 있는 게시 컨텍스트 이름의 배열을 반환합니다. 현재 게시 컨텍스트 이름은 다음과 같습니다.

* `ImageServing`
* `ImageRendering`
* `Video`

구현된 `getSearchStrings` 작업. 지정된 자산에 대한 검색 문자열 배열을 반환합니다.

작업 및 API 작업의 로케일을 설정하는 메커니즘에 대한 로케일 매개 변수가 추가되었습니다. 로케일 문자열은 포맷으로 지정해야 합니다 `<language_code>[-<country_code>]`. 언어 코드는 ISO-639에서 지정한 소문자, 두 문자 코드이며, 선택적 국가 코드는 ISO-3166에서 지정한 대문자, 두 문자 코드입니다.

API 작업의 로케일을 설정하기 위해 SOAP `authHeader` 헤더에 선택적 로케일 매개 변수를 추가했습니다. 이 매개 변수가 없으면 HTTP 헤더가 `Accept-Language` 사용됩니다. 이 헤더가 없는 경우 IPS 서버의 기본 로케일이 사용됩니다.

강력한 형식의 메타데이터 필드에 대한 get/set 지원을 추가했습니다.

gzip 응답 제어를 위한 SOAP 및 HTTP 헤더 지원을 구현했습니다.

에 `gzipResponse` 플래그를 `authHeader`추가했습니다. API가 없는 경우 HTTP `Accept-Encoding` 헤더도 확인합니다.

강력한 형식의 메타데이터 필드 조건에 대한 searchAssets 지원이 추가되었습니다.

* 모든 필드 유형의 경우 문자열 비교 연산자( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)로 값을 전달할 수 있습니다.
* 부울 필드의 경우 `boolVal` 연산과 함께 `Equals` 전달될 수 있습니다.
* int 필드의 `longVal` 경우 숫자 비교 연산자()와 함께 전달되거나 숫자 범위 작업( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)과 함께 전달될 `minLong/maxLong` `Between, NotBetween`수 있습니다.
* 부동 필드의 `doubleVal` 경우 숫자 비교 연산자()와 함께 전달되거나 숫자 범위 작업( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)과 함께 전달될 `minDouble/maxDouble` `Between, NotBetween`수 있습니다.
* 날짜 필드의 경우 숫자 비교 연산자() `dateVal` 와 함께 전달하거나 minDate/maxDate를 숫자 범위 작업( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals``Between, NotBetween`)과 함께 전달할 수 있습니다.

유형에 설명, `jobSubType`및 `originalJobName` 필드를 `JobLog` 추가했습니다.

* `originalJobName` 은 에 제출되는 작업 이름입니다(고유성 `submitJob` 접미어나 후속 작업 이름 없음).
* `jobSubType` 은 현재 `ImageServingPublishJob` 작업(작업 중 하나 `full``increment, fullwithsearch,` 또는 `fulloverride`인 경우)에서만 사용됩니다.
* `description` 은 현재 모든 작업 유형에 대해 빈 문자열이지만, 결국 업로드 경로와 같은 요약 작업 정보가 포함됩니다.

또한 다음 필드는 `getJobLogs` 및 `getJobLogDetails`모두에 포함되지 않습니다. 이전 버전에서는 를 사용할 수 `getJobLogDetails`있었습니다.

* `endDate` (작업이 완료된 경우)
* `fileDuplicateCount` (이전에는 항상 `0` 함께 `getJobLogs`)
* `fileUpdateCount` (이전에는 항상 `0` 함께 `getJobLogs` 포함되었으며 `fileSuccessCount`포함되었습니다.이제 별도의 필드로 분할됩니다.)

자산에 assetHandle 필드를 `JobLogDetail` 추가했습니다.

선택적 설명 매개 변수를 에 `submitJob`추가했습니다. 이것은 검색하기 위해 `getScheduledJobs``getActiveJobs`그리고 `getJobLogs`통과됩니다.

SKU 시스템 필드를 사용하지 않습니다. 필드를 to로 전달하면 해당 필드가 무시됩니다. `SystemFieldCondition` The field is ignored in a `searchAssets`.

필터를 `excludeAssetTypeArray` 추가했습니다 `searchAssets`.

에 `MaskInfo` 유형을 `Asset`추가했습니다.

IPS로 관리할 새 자산 유형 추가:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>자산 유형 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator 파일. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS 및 PostScript 파일. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>.doc로 끝나는 파일을 위한 Microsoft Word 문서입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>.xls로 끝나는 파일을 위한 Microsoft Excel 문서 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>.ppt로 끝나는 파일을 위한 Microsoft PowerPoint 문서 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>.rtf로 끝나는 파일을 위한 RTF 파일. </p> </td> 
  </tr> 
 </tbody> 
</table>

Postscript, Illustrator `UploadDirectoryJob` 및 PDF 파일의 처리를 독립적으로 제어하는 추가 옵션을 `UploadUrlsJob` 추가했습니다. 모든 기존 작업은 필요한 매개 변수를 3개의 처리 파이프라인에 제공하여 현재 수행했던 대로 정확히 작동합니다. 원본 `PostScriptOptions` 블록은 Illustrator 및 EPS/PS 파일의 처리를 설정하는 데 사용됩니다. 선택적으로 특정 파일 옵션 블록을 제공하여 처리를 지정할 수 있습니다. 변경 사항 목록은 다음과 같습니다.

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>필드 </p> </th> 
   <th colname="col2" class="entry"> <p>매개 변수 </p> </th> 
   <th colname="col3" class="entry"> <p>값 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 없음 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 래스터화 </span>(기본값) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>자산만 관리하고 업로드 시 파생물을 만들지 않습니다. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPS 및 PostScript 파일을 지정된 해상도와 색상 공간에서 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>선택 사항입니다. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>파일을 이미지로 래스터화할 때 적용됩니다. 원본 파일이 로고를 오버레이할 때 이 방식으로 정의된 경우 투명한 뒷면이 생성됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> Illustrator옵션 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 없음 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 래스터화 </span> (기본값) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>자산만 관리하고 업로드 시 파생물을 만들지 않습니다. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>정해진 해상도와 색상 공간에서 파일을 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;정수&gt; </span> </p> </td> 
   <td colname="col4"> <p>해상도 래스터화 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 색상 공간 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>렌더링을 위한 대상 색상 공간 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>선택 사항입니다. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>파일을 이미지로 래스터화할 때 영향을 줍니다. 원본 파일이 오버레이 로고를 만들 때 이렇게 정의된 경우 투명한 배경을 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 없음 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 래스터화 </span> (기본값) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>자산만 관리하고 업로드 시 파생물을 만들지 않습니다. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>정해진 해상도와 색상 공간에서 파일을 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;정수&gt; </span> </p> </td> 
   <td colname="col4"> <p>해상도 래스터화 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 색상 공간 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>렌더링을 위한 대상 색상 공간 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>렌더링 후 여러 페이지 PDF를 eCatalog로 결합할지 여부를 정의합니다(기본값은 true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>나중에 검색 서버에 제공하기 위해 PDF의 단어를 DB로 추출할지 여부를 정의합니다(기본값: false). </p> </td> 
  </tr> 
 </tbody> 
</table>

쿼리를 보낼 수도 `getScheduledJobs`있습니다.

다음 값 중 하나를 가져오도록 `webservice.gzip.response` 구성 속성을 수정했습니다.

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>값 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 안 함 </span> </p> </td> 
   <td colname="col2"> <p>응답에 gzip을 추가하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse가 true인 경우에만 Gzip 응답을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 승인 </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse가 true이거나 gzipResponse 헤더가 없거나 HTTP Accept-Encoding 헤더에 gzip이 포함된 경우 Gzip입니다. (기본값). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상 </span> </p> </td> 
   <td colname="col2"> <p>헤더 값에 상관없이 항상 gzip 응답을 표시합니다. 이 값은 디버깅용으로만 사용하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

