---
title: 새 추가 및 변경 사항
description: IPS API v4.0의 새로운 변경 사항과 구현된 변경 사항에 대해 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 2%

---

# 새 추가 및 변경 사항{#new-additions-and-changes}

IPS API v4.0의 새로운 변경 사항과 구현된 변경 사항에 대해 설명합니다.

별도의 WSDL 및 스키마 네임스페이스를 사용하여 병렬 API 버전을 구현했습니다.

* 이전 API 버전: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0 버전: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

추가됨 `PostScriptOptions/alpha` 필드.

추가됨 `VideoRootUrl` 및 `SwfRootUrl` 속성 `getProperty` 작업.

옵션 추가됨 `appName` 및 `appVersion` 매개 변수를으로 지정합니다. `authHeader` 호출 응용 프로그램을 추적합니다. 에 로깅을 추가했습니다. `ipsApiService.log`.

선택 사항이 추가됨 `serviceUrl` WSDL 생성 서블릿에 대한 매개 변수 이 매개 변수는 디버그 프록시에 유용합니다. 예: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

구현됨 `getZipEntries` 작업.

시스템 필드 조건에 대한 검색 범위 및 입력된 비교 값을 구현했습니다.

추가됨 `'Asset'` 자산 유형 문자열 상수(주로 자산 간 메타데이터 필드 허용)

구현됨 `trashState` 매개 변수 `searchAssets`.

구현됨 `getAssetPublishHistory` 작업.

옵션 추가됨 `faultHttpStatusCode` Flex에서 오류 처리를 활성화하는 SOAP 헤더입니다. Flex의 경우 다음을 사용합니다. `<faultHttpStatusCode>200</faultHttpStatusCode>`. 오류 응답에 대한 기본 상태 코드는 다음과 같습니다. `500 (Internal Server Error)`.

휴지통에서 자산을 복원하고 휴지통에서 자산을 비우는 작업이 추가되었습니다.

CRUD 작업을 구현했습니다.

에 활성화 플래그가 추가되었습니다. `ImageMap` 및 유형 `saveImageMap` 작업.

나머지 파일 최적화 작업에 대한 지원을 추가했습니다.

추가됨 `setAssetsPublishState` 벌크 게시 상태 업데이트용

추가됨 `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

더 이상 사용되지 않음 `saveMetadataField` 신입 사원 모집 작전 `createMetadataField` 및 `updateMetadataField` 작업.

구현됨 `deleteAssetsParam` 일괄 삭제 작업.

구현됨 `moveAssetsParam` 일괄 이동 작업.

구현됨 `deleteMetadataField` 작업.

구현됨 `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` 작업.

구현됨 `getAssetCounts`.

에 지원이 추가됨 `setImageSetMembers` 포함용 `RenderSet` 의 구성원 `ImageSet` 에셋.

추가됨 `replaceImage` 작업.

추가됨 `copyImage` 작업.

추가됨 `setUrlModifier` 작업 및 `urlModifier/urlPostApplyModifier` 필드 `LayerViewInfo`, `TemplateInfo`, 및 `WatermarkInfo`.

추가됨 `createDerivedAsset` 작업. 현재 `ownerHandle` 이미지 자산을 참조해야 하며 형식은 다음과 같을 수 있습니다. `AdjustedView` 또는 `LayerView`.

추가됨 `createTemplate` 작업. 템플릿 또는 워터마크 자산을 만들려면 를 호출하십시오.

IPS 회사 설정, `CompanySettings`웹 서비스 API로 포팅되었습니다.

추가됨 `excludeByproducts` 플래그 필터링 대상 `searchAssets` 작업. 이 플래그를 true 실행으로 설정 `PSDlayer` 이미지 및 PDF 리핑된 이미지.

추가됨 `getGenerationInfo` 작업.

추가됨 `SystemMessage` 속성 이름 `getProperty` 작업.

해당 에셋 정보 필드와 일치하도록 일부 에셋 유형 문자열 상수를 수정했습니다.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

성공, 경고 및 오류를 요약하는 일괄 처리 작업의 결과 형식을 수정했습니다.

구현됨 `batchSetAssetMetadata` 일괄 처리 메타데이터 작업.

앱별 데이터에 대한 지원을 구현했습니다.

에 대한 부울 플래그에 대한 지원이 구현되었습니다. `createTemplate`, `extendLayers`, 및 `extractText` Photoshop 처리 프로세스를 제어하기 위한 업로드 작업(파일 업로드 추가에 대한 변경 사항과 유사)

구현됨 `setImageMaps` 및 `setZoomTargets` 작업.

구현됨 `ViewerPreset` 작업. 인식되는 유형은 다음과 같습니다.

* `VideoPlayer` (비디오는 이러한 뷰어만 게시합니다.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

뷰어 스킨은 다음 두 가지 매개 변수를 지원합니다. `skinFg` 및 `skinBg`. 백엔드 코드는 이전 버전과의 호환성을 유지하는 데 필요한 모든 처리를 수행합니다.

구현됨 `getAssociatedAssets` 작업.

추가됨 `ReprocessAssets` PDF 리핑 및 이미지 재최적화를 포함하여 이전에 업로드한 기본 소스 파일을 재처리할 수 있도록 하는 작업 유형입니다.

이름이 변경됨 `PropertySetType` 필드 유형 대상 `propertyType`. 이 이름 변경은 다음 항목에 영향을 줍니다. `createPropertySetType` 매개 변수 및 `getPropertySetType/getPropertySetTypes` 응답.

구현됨 `batchSetImageFields` 이미지 사용자 데이터 및 기타 편집 가능한 이미지 필드 설정을 지원하는 작업입니다.

47 다양한 에셋 정보 유형에 fileSize 필드를 추가했습니다.

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

구현됨 `getActivePublishContexts` 작업. 이 작업은 지정된 회사에 대해 활성 게시 서버가 있는 게시 컨텍스트 이름의 배열을 반환합니다. 현재 게시 컨텍스트 이름은 다음과 같습니다.

* `ImageServing`
* `ImageRendering`
* `Video`

구현됨 `getSearchStrings` 작업. 지정된 자산에 대한 검색 문자열 배열을 반환합니다.

작업에 대한 로케일 매개 변수와 API 작업에 대한 로케일을 설정하는 메커니즘을 추가했습니다. 로케일 문자열의 형식은 다음과 같아야 합니다. `<language_code>[-<country_code>]`. 언어 코드는 ISO-639에 지정된 소문자 두 자리 코드이며, 선택적 국가 코드는 ISO-3166에 지정된 대문자 두 자리 코드입니다.

선택적 로케일 매개 변수가 `authHeader` API 작업의 로케일을 설정하는 SOAP 헤더입니다. 이 매개 변수가 없으면 HTTP 헤더가 `Accept-Language` 를 사용합니다. 이 헤더도 없으면 IPS 서버에 대한 기본 로케일이 사용됩니다.

강력한 형식의 메타데이터 필드에 대한 get/set 지원을 추가했습니다.

gzip 응답 제어에 대한 SOAP 및 HTTP 헤더 지원을 구현했습니다.

추가됨 `gzipResponse` 플래그 지정 대상 `authHeader`. 존재하지 않는 경우 API는 HTTP를 확인합니다 `Accept-Encoding` 머리글입니다.

강력한 형식의 메타데이터 필드 조건에 대한 searchAssets 지원이 추가되었습니다.

* 모든 필드 유형의 경우 문자열 비교 연산자()를 사용하여 값을 전달할 수 있습니다. `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* 부울 필드의 경우, `boolVal` 를 사용하여 전달할 수 있습니다. `Equals` op.
* Int 필드의 경우, `longVal` 숫자 비교 연산자( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) 또는 `minLong/maxLong` 숫자 범위 작업( `Between, NotBetween`).
* 부동 필드의 경우, `doubleVal` 숫자 비교 연산자( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) 또는 `minDouble/maxDouble` 숫자 범위 작업( `Between, NotBetween`).
* 날짜 필드의 경우 `dateVal` 숫자 비교 연산자 사용( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) 또는 숫자 범위 작업( )으로 minDate/maxDate를 전달할 수 있습니다. `Between, NotBetween`).

설명 추가됨, `jobSubType`, 및 `originalJobName` 필드 대상 `JobLog` 유형.

* `originalJobName` 은(는) 작업 이름이에 제출되었습니다. `submitJob` (고유성 접미사 또는 후속 작업 이름 제외)
* `jobSubType` 다음에만 사용됨: `ImageServingPublishJob` 작업(다음 중 하나) `full`, `increment, fullwithsearch,` 또는 `fulloverride`).
* `description` 는 모든 작업 유형에 대해 빈 문자열이지만 업로드 경로와 같은 요약 작업 정보를 포함합니다.

또한 다음 필드는 두 필드 모두에 포함되지 않습니다 `getJobLogs` 및 `getJobLogDetails`. 이전 버전에서는 `getJobLogDetails`.

* `endDate` (작업이 완료된 경우).
* `fileDuplicateCount` (이전에는 항상 `0` 포함 `getJobLogs`)
* `fileUpdateCount` (이전에는 항상 `0` 포함 `getJobLogs` 및 포함 `fileSuccessCount`: 이제 별도의 필드로 분할됩니다.

에 assetHandle 필드가 추가되었습니다. `JobLogDetail` 유형.

선택적 설명 매개 변수가에 추가됨 `submitJob`. 이 매개변수는에서 검색하기 위해 전달됩니다. `getScheduledJobs`, `getActiveJobs`, 및 `getJobLogs`.

SKU 시스템 필드를 사용하지 않습니다. 필드가 로 전달되면 무시됩니다. `SystemFieldCondition` 끝 `searchAssets`.

추가됨 `excludeAssetTypeArray` 필터링 대상 `searchAssets`.

추가됨 `MaskInfo` 입력 대상 `Asset`.

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
   <td colname="col2"> <p>Microsoft® .doc으로 끝나는 파일용 Word 문서. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>.xls로 끝나는 파일용 Microsoft® Excel 문서. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPoint 문서 </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® .ppt로 끝나는 파일용 PowerPoint 문서. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>.rtf로 끝나는 업로드된 파일에 대한 RTF 파일입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

에 추가 옵션 추가됨 `UploadDirectoryJob` 및 `UploadUrlsJob` Postscript, Illustrator 및 PDF 파일의 처리를 독립적으로 제어합니다. 기존의 모든 작업은 세 개의 처리 파이프라인 각각에 필요한 매개 변수를 제공하므로 오늘날과 같이 정확하게 작동합니다. 원본 `PostScriptOptions` 블록은 Illustrator 및 EPS/PS 파일에 대한 처리를 설정하는 데 사용됩니다. 선택적으로, 특정 파일 옵션 블록이 처리를 지정하기 위해 제공될 수 있다. 변경 사항 목록에는 다음이 포함됩니다.

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> 없음 </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> 래스터화 </span>(기본값) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>에셋만 관리하고 업로드 시 파생상품을 생성하지 않습니다. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>EPS 및 PostScript 파일을 지정된 해상도 및 색상 공간의 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>선택적. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>파일을 이미지로 래스터화할 때 적용됩니다. 로고를 오버레이하기 위해 원본 파일이 이러한 방식으로 정의된 경우 투명한 배경이 만들어집니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> 없음 </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> 래스터화 </span> (기본값) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>에셋만 관리하고 업로드 시 파생상품을 생성하지 않습니다. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>지정된 해상도 및 색상 공간에서 파일을 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;정수&gt; </span> </p> </td> 
   <td colname="col4"> <p>해상도 래스터화. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>렌더링을 위한 Target 색상 공간. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>선택적. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>파일을 이미지로 래스터화할 때 적용됩니다. 원본 파일이 오버레이 로고를 만들기 위해 이러한 방식으로 정의된 경우 투명한 배경을 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDF 옵션 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 프로세스 </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> 없음 </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> 래스터화 </span> (기본값) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>에셋만 관리하고 업로드 시 파생상품을 생성하지 않습니다. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>지정된 해상도 및 색상 공간에서 파일을 이미지로 렌더링합니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;정수&gt; </span> </p> </td> 
   <td colname="col4"> <p>해상도 래스터화. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>렌더링을 위한 Target 색상 공간. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>렌더링 후 여러 페이지 PDF을 eCatalog에 결합할지 여부를 정의합니다(기본값은 true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchwords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;부울&gt; </span> </p> </td> 
   <td colname="col4"> <p>나중에 검색 서버에 제공하기 위해 PDF의 단어를 DB로 추출할지 여부를 정의합니다(기본값은 false임). </p> </td> 
  </tr> 
 </tbody> 
</table>

다음에서 쿼리할 수도 있습니다. `getScheduledJobs`.

수정됨 `webservice.gzip.response` 구성 속성을 사용하여 다음 값 중 하나를 사용합니다.

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>값 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>응답을 gzip으로 표시하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Gzip 응답은 authHeader/gzipResponse가 true인 경우에만 해당됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>authHeader/gzipResponse가 true이거나 gzipResponse 헤더가 없고 HTTP Accept-Encoding 헤더에 gzip이 포함된 경우, Gzip입니다. (기본값). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>헤더 값에 관계없이 항상 gzip 응답 이 값은 디버깅 목적으로만 사용하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>
