---
description: 지정된 기준에 따라 자산을 검색합니다.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 7%

---


# searchAssets{#searchassets}

지정된 기준에 따라 자산을 검색합니다.

구문

## searchAssets:{#section-4ad74f12eb754768bf85bd235a7e25f0} 정보

`searchAssets` 는 IPS 자산을 검색하는 기본 방법입니다. 이 메서드는 폴더 계층 구조를 탐색하거나 이름으로 특정 자산을 찾는 등 다양한 목적으로 사용됩니다.

**응답 크기**

`searchAssets` 단일 호출에서 최대 1,000개의 자산을 반환합니다. 호출당 최대 10,000개의 에셋을 반환하려면 응답 데이터를 `totalRows`, `name`, `handle`, `type` 및 `subType` 필드의 하위 집합으로 제한합니다. 큰 세트를 반환하려면 `resultPage` 매개 변수로 페이징 설정을 설정합니다.

**responseFieldArray 또는 excludeFieldArray로 결과 파일 크기 제한**

데이터 세트의 크기를 `responseFieldArray` 또는 `excludFieldArray` 매개 변수로 제한합니다. 이러한 매개 변수는 메모리 사용 및 대역폭을 줄이고 서버 응답 시간을 개선하는 데 도움이 됩니다.

## 인증된 사용자 유형 {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 자산 반환 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-49aabc0600764f55a8b7017d86ded44f}

**입력(searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 필수? </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 검색할 자산이 있는 회사의 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 관리자가 다른 사용자로 작업할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 관리자가 다른 그룹의 일부로 작업할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 폴더</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 자산 검색을 위한 루트 경로입니다. 생략하면 회사 루트 폴더가 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">하위 폴더를 검색하려면 <span class="codeph"> true</span>로 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 게시 상태 선택. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">휴지통 상태 선택. 기본값은 <span class="codeph"> NotInTrash</span>입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p><span class="codeph"> keywordArray</span> 결과를 결합할 검색 일치 모드 선택, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span> 및  <span class="codeph"> metadataConditionArray</span>. 기본값은 <span class="codeph"> MatchAll</span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p> <p>참고: 사용되지 않는 매개 변수입니다. 그것을 사용하지 않는 것이 좋다. </p> </p> <p>일치시킬 키워드의 문자열 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p><span class="codeph"> systemFieldCondition</span>과 일치하는 검색 일치 모드 선택 기본값은 <span class="codeph"> MatchAll</span>입니다. </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 시스템 필드 조건의 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">검색 일치 모드 문자열 상수입니다. 기본값은 <span class="codeph"> MatchAll</span>입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagConditionArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> <p>태그 필드 검색의 배열입니다. </p> <p>예측자는 <span class="codeph"> tagMatchMode</span> 설정에 따라 결합된 다음 <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span> 및 <span class="codeph"> metadataConditionArray</span>에 있는 모든 용어와 결합합니다. <span class="codeph"> conditionMatch 모드</span> 설정. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">검색 일치 모드를 사용하여 <span class="codeph"> metadataCondition</span> 일치 항목을 결합합니다. 기본값은 <span class="codeph"> MatchAll</span>입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 메타데이터 필드 검색 조건 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 검색에 포함할 자산 유형 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 검색에서 제외할 자산 유형 배열입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 필터링할 하위 유형 이름 목록입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"><span class="codeph"> true</span> 및 <span class="codeph"> assetSubTypeArray</span>이(가) 비어 있지 않으면 하위 유형이 <span class="codeph"> assetSubTypeArray</span>에 있는 자산만 반환됩니다. <span class="codeph"> false</span>(기본값)이면 정의된 하위 유형이 없는 자산이 반환됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> true인 경우 리핑된 PDF 페이지 이미지와 같은 기본 자산을 수집하는 동안 생성된 부산물 자산은 검색 결과에서 제외됩니다. 기본값은 false입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludMozillaArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:ExcludeMozillaArray</span> </p> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 검색 결과에서 제외할 부산물 자산 생성 조건의 배열입니다. 이 매개 변수가 있으면 excludeByproducts 설정을 무시합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 검색할 에셋이 포함된 프로젝트를 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 반환할 최대 결과 수입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"><span class="codeph"> recordsPerPage</span> 페이지 크기를 기준으로 반환할 결과 페이지를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 자산 정렬 필드 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 정렬 방향 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 응답에 포함할 필드 및 하위 필드 목록을 포함합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 응답에서 제외하기 위한 필드 및 하위 필드 목록을 포함합니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(searchAssetsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | 아니요 | 페이지당 레코드가 제한되지 않을 때 검색이 반환하는 행 수입니다. |
| `*`assetArray`*` | `types:AssetArray` | 아니요 | 검색이 반환하는 자산. |

## 예제 {#section-725484cc09b54772a838ad2cc930b94b}

이 코드 샘플은 특정 회사에 속하는 이미지 자산을 검색합니다. 잠시 동안 응답이 잘립니다.

**요청**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**응답**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```

