---
description: IPS API v4.0의 새로운 변경 사항 및 구현된 변경 사항에 대해 설명합니다.
seo-description: IPS API v4.0의 새로운 변경 사항 및 구현된 변경 사항에 대해 설명합니다.
seo-title: 새로운 추가 및 변경 사항
solution: Experience Manager
title: 새로운 추가 및 변경 사항
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 2%

---


# 새 추가 및 변경 사항{#new-additions-and-changes}

IPS API v4.0의 새로운 변경 사항 및 구현된 변경 사항에 대해 설명합니다.

별도의 WSDL 및 스키마 네임스페이스로 API 버전을 나란히 구현했습니다.

* 이전 API 버전:`IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0 버전:`IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

`PostScriptOptions/alpha` 필드를 추가했습니다.

`getProperty` 작업에 대해 `VideoRootUrl` 및 `SwfRootUrl` 속성을 추가했습니다.

호출 응용 프로그램을 추적하기 위해 선택적 `appName` 및 `appVersion` 매개 변수를 `authHeader`에 추가했습니다. `ipsApiService.log`에 로깅을 추가했습니다.

선택적 `serviceUrl` 매개 변수를 WSDL 생성 서블릿에 추가했습니다. 이 기능은 디버그 프록시에 특히 유용합니다. 예: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

`getZipEntries` 작업을 구현했습니다.

시스템 필드 조건에 대한 검색 범위 및 입력된 비교 값을 구현했습니다.

상호 자산 메타데이터 필드를 허용하도록 `'Asset'` 자산 유형 문자열 상수를 추가했습니다.

`searchAssets`에 대해 `trashState` 매개 변수를 구현했습니다.

`getAssetPublishHistory` 작업을 구현했습니다.

Flex에서 오류 처리를 활성화하기 위해 선택적 `faultHttpStatusCode` SOAP 헤더를 추가했습니다. Flex의 경우 `<faultHttpStatusCode>200</faultHttpStatusCode>`을(를) 사용합니다. 오류 응답에 대한 기본 상태 코드는 `500 (Internal Server Error)`입니다.

휴지통에서 자산 및 휴지통에서 빈 자산을 복원하는 작업을 추가했습니다.

CRUD 작업을 구현했습니다.

`ImageMap` 유형 및 `saveImageMap` 작업에 활성화된 플래그가 추가되었습니다.

나머지 파일 최적화 작업에 대한 지원을 추가했습니다.

벌크 게시 상태 업데이트를 위해 `setAssetsPublishState`을(를) 추가했습니다.

`ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`가 추가되었습니다.

새 `createMetadataField` 및 `updateMetadataField` 작업 대신 `saveMetadataField` 작업이 사용되지 않습니다.

`deleteAssetsParam` 일괄 삭제 작업을 구현했습니다.

`moveAssetsParam` 일괄 이동 작업을 구현했습니다.

`deleteMetadataField` 작업을 구현했습니다.

`get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` 작업을 구현했습니다.

`getAssetCounts`을(를) 구현했습니다.

`ImageSet` 자산에 `RenderSet` 멤버를 포함하기 위한 지원을 `setImageSetMembers`에 추가했습니다.

`replaceImage` 작업이 추가되었습니다.

`copyImage` 작업이 추가되었습니다.

`LayerViewInfo`, `TemplateInfo` 및 `WatermarkInfo`에 대한 `setUrlModifier` 작업 및 `urlModifier/urlPostApplyModifier` 필드를 추가했습니다.

`createDerivedAsset` 작업이 추가되었습니다. 현재 `ownerHandle`은(는) 이미지 자산을 참조해야 하며 유형은 `AdjustedView` 또는 `LayerView`일 수 있습니다.

`createTemplate` 작업이 추가되었습니다. 현재 이 매개 변수를 호출하여 템플릿 또는 워터마크 자산을 만들 수 있습니다.

IPS 회사 설정 `CompanySettings`은(는) 웹 서비스 API로 포팅되었습니다.

`excludeByproducts` 필터 플래그가 `searchAssets` 작업에 추가되었습니다. 이 플래그를 true로 설정하면 `PSDlayer` 이미지와 PDF 리래핑된 이미지가 실행됩니다.

`getGenerationInfo` 작업이 추가되었습니다.

`SystemMessage` 속성 이름을 `getProperty` 작업에 추가했습니다.

해당 자산 정보 필드와 일치하도록 일부 자산 유형 문자열 상수를 수정했습니다.

* WordDoc:Word
* ExcelDoc:Excel
* PowerPoint 문서:PowerPoint
* RTFDoc:Rtf

성공, 경고 및 오류를 요약하기 위해 일괄 처리 작업의 결과 형식을 수정했습니다.

`batchSetAssetMetadata` 일괄 메타데이터 작업을 구현했습니다.

앱별 데이터에 대한 지원을 구현했습니다.

Photoshop 처리 프로세스를 제어하기 위해 업로드 작업에 대한 부울 플래그(파일 업로드 추가에 대한 변경과 유사)에 대한 지원이 구현되었습니다.`createTemplate``extendLayers``extractText`

`setImageMaps` 및 `setZoomTargets` 작업을 구현했습니다.

`ViewerPreset` 작업을 구현했습니다. 인식된 유형은 다음과 같습니다.

* `VideoPlayer` (비디오는 이러한 뷰어만 게시합니다.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

뷰어 스킨은 두 개의 매개 변수를 지원합니다.`skinFg` 및 `skinBg`. 백엔드 코드는 이전 버전과의 호환성을 유지하는 데 필요한 모든 처리를 수행합니다.

`getAssociatedAssets` 작업을 구현했습니다.

PDF 리핑 및 이미지 재최적화를 포함하여 이전에 업로드한 기본 소스 파일을 재처리할 수 있도록 `ReprocessAssets` 작업 유형을 추가했습니다.

`PropertySetType` 필드 유형의 이름을 `propertyType`으로 변경했습니다. 이것은 `createPropertySetType` 매개 변수와 `getPropertySetType/getPropertySetTypes` 응답에 영향을 줍니다.

이미지 사용자 데이터 및 기타 편집 가능한 이미지 필드 설정을 지원하기 위해 `batchSetImageFields` 작업을 구현했습니다.

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

`getActivePublishContexts` 작업을 구현했습니다. 이 작업은 지정된 회사에 대해 활성 게시 서버가 있는 게시 컨텍스트 이름 배열을 반환합니다. 현재 게시 컨텍스트 이름:

* `ImageServing`
* `ImageRendering`
* `Video`

`getSearchStrings` 작업을 구현했습니다. 지정된 자산에 대한 검색 문자열 배열을 반환합니다.

작업 및 API 작업의 로케일을 설정하는 메커니즘에 대한 로케일 매개 변수를 추가했습니다. 로케일 문자열은 `<language_code>[-<country_code>]` 형식이어야 합니다. 언어 코드는 ISO-639에서 지정한 소문자 2자 코드이고, 선택적 국가 코드는 ISO-3166에서 지정한 대문자 2자 코드입니다.

API 작업의 로케일을 설정하기 위해 `authHeader` SOAP 헤더에 선택적 로케일 매개 변수를 추가했습니다. 이 매개 변수가 없으면 HTTP 헤더 `Accept-Language`이 사용됩니다. 이 헤더가 없는 경우 IPS 서버의 기본 로케일이 사용됩니다.

강력한 형식의 메타데이터 필드에 대한 get/set 지원을 추가했습니다.

gzip 응답 제어에 대한 SOAP 및 HTTP 헤더 지원을 구현했습니다.

`authHeader`에 `gzipResponse` 플래그를 추가했습니다. 없는 경우 API는 HTTP `Accept-Encoding` 헤더도 확인합니다.

강력한 형식의 메타데이터 필드 조건에 대한 searchAssets 지원을 추가했습니다.

* 모든 필드 유형의 경우 문자열 비교 연산자( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)로 값을 전달할 수 있습니다.
* 부울 필드의 경우 `boolVal`이(가) `Equals` 연산으로 전달될 수 있습니다.
* int 필드의 경우 `longVal`을(를) 숫자 비교 연산자( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)와 함께 전달하거나 `minLong/maxLong`를 숫자 범위 작업( `Between, NotBetween`)과 함께 전달할 수 있습니다.
* 부동 필드의 경우 `doubleVal`을(를) 숫자 비교 연산자( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)와 함께 전달하거나 `minDouble/maxDouble`를 숫자 범위 작업( `Between, NotBetween`)과 함께 전달할 수 있습니다.
* 날짜 필드의 경우 숫자 비교 연산자( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`)를 사용하여 `dateVal`을(를) 전달하거나 숫자 범위 작업( `Between, NotBetween`)을 사용하여 minDate/maxDate를 전달할 수 있습니다.

`JobLog` 유형에 설명, `jobSubType` 및 `originalJobName` 필드를 추가했습니다.

* `originalJobName` 은 (고유성  `submitJob` 접미사나 후속 작업 이름 없이) 제출되는 작업 이름입니다.
* `jobSubType` 은 현재  `ImageServingPublishJob` 작업(작업 중 하나  `full` `increment, fullwithsearch,` 또는  `fulloverride`작업)에서만 사용됩니다.
* `description` 은 현재 모든 작업 유형에 대해 빈 문자열이지만, 결국 업로드 경로와 같은 요약 작업 정보가 포함됩니다.

또한 다음 필드는 `getJobLogs` 및 `getJobLogDetails` 모두에 포함되지 않습니다. 이전 버전에서는 `getJobLogDetails`에서만 사용할 수 있었습니다.

* `endDate` (작업이 완료된 경우)
* `fileDuplicateCount` (이전에는 항상  `0` 함께  `getJobLogs`)
* `fileUpdateCount` (이전에는 항상  `0` 함께  `getJobLogs` 있고 여기에  `fileSuccessCount`포함되었습니다.이제 별도의 필드로 분할됩니다.)

`JobLogDetail` 유형에 assetHandle 필드를 추가했습니다.

선택적 description 매개 변수를 `submitJob`에 추가했습니다. 이 값은 `getScheduledJobs`, `getActiveJobs` 및 `getJobLogs`에서 검색하기 위해 전달됩니다.

SKU 시스템 필드를 사용하지 않습니다. 필드가 `SystemFieldCondition`으로 `searchAssets`에 전달되면 무시됩니다.

`excludeAssetTypeArray` 필터를 `searchAssets`에 추가했습니다.

`MaskInfo` 유형을 `Asset`에 추가했습니다.

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>.doc로 끝나는 파일을 위한 Microsoft Word 문서입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>.xls로 끝나는 파일을 위한 Microsoft Excel 문서 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>.ppt로 끝나는 파일을 위한 Microsoft PowerPoint 문서 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>.rtf로 끝나는 파일을 위한 RTF 파일. </p> </td> 
  </tr> 
 </tbody> 
</table>

Postscript, Illustrator 및 PDF 파일의 처리를 독립적으로 제어하는 추가 옵션을 `UploadDirectoryJob` 및 `UploadUrlsJob`에 추가했습니다. 모든 기존 작업은 필요한 매개 변수를 3개의 처리 파이프라인 각각에 제공하여 오늘처럼 정확히 작동하도록 합니다. 원래 `PostScriptOptions` 블록은 Illustrator 및 EPS/PS 파일의 처리를 설정하는 데 사용됩니다. 선택적으로 처리를 지정하기 위해 특정 파일 옵션 블록을 제공할 수 있습니다. 변경 사항 목록은 다음과 같습니다.

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 없음 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 래스터화  </span>(기본값) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>에셋만 관리하고 업로드할 때 파생물을 만들지 마십시오. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPS 및 PostScript 파일을 지정된 해상도 및 색상 공간에서 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>선택 사항입니다. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>파일을 이미지로 래스터화할 때 적용됩니다. 로고를 오버레이할 때 원본 파일이 이 방식으로 정의된 경우 투명한 뒷면이 생성됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 없음 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 래스터화  </span> (기본값) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>에셋만 관리하고 업로드할 때 파생물을 만들지 마십시오. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>지정된 해상도 및 색상 공간에서 파일을 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;정수&gt; </span> </p> </td> 
   <td colname="col4"> <p>해상도 래스터화 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 색상 공간 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>렌더링을 위한 Target 색상 공간. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 알파  </span> </p> <p>선택 사항입니다. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>파일을 이미지로 래스터화할 때 영향을 줍니다. 오버레이 로고를 만들 때 원본 파일이 이러한 방식으로 정의된 경우 투명한 배경을 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 없음 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 래스터화  </span> (기본값) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>에셋만 관리하고 업로드할 때 파생물을 만들지 마십시오. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>지정된 해상도 및 색상 공간에서 파일을 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;정수&gt; </span> </p> </td> 
   <td colname="col4"> <p>해상도 래스터화 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> 색상 공간 </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>렌더링을 위한 Target 색상 공간. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>렌더링 후 여러 페이지 PDF를 eCatalog로 결합할지 여부를 정의합니다(기본값은 true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>나중에 검색 서버에 제공하기 위해 PDF의 단어가 DB에 추출되는지 여부를 정의합니다(기본값: false). </p> </td> 
  </tr> 
 </tbody> 
</table>

`getScheduledJobs`에서 쿼리할 수도 있습니다.

다음 값 중 하나를 취하도록 `webservice.gzip.response` 구성 속성을 수정했습니다.

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
   <td colname="col2"> <p>응답을 gzip으로 채우지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse가 true인 경우에만 gzip 응답이 반환됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 승인 </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse가 true이거나, gzipResponse 헤더가 없거나, HTTP Accept-Encoding 헤더에 gzip이 포함되어 있는 경우 gzip을 반환합니다. (기본값). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상 </span> </p> </td> 
   <td colname="col2"> <p>헤더 값에 관계 없이 항상 응답합니다. 이 값은 디버깅 용도로만 사용하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

