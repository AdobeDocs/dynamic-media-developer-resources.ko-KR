---
description: 이미지 서버에 게시할 원시 세트 정의 문자열로 일반 자산 세트를 만듭니다.
seo-description: 이미지 서버에 게시할 원시 세트 정의 문자열로 일반 자산 세트를 만듭니다.
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 6%

---


# createAssetSet{#createassetset}

이미지 서버에 게시할 원시 세트 정의 문자열로 일반 자산 세트를 만듭니다.

구문

## 공인 사용자 유형 {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-3580b586296e42a5b21426085b1bb72d}

**입력(createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 필수 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 자산 세트를 포함할 회사의 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 새 자산 세트가 생성될 폴더의 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 자산 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 자산 집합 유형에 대해 클라이언트가 만든 고유 식별자입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 설정 정의 문자열의 매개 변수입니다. <p>대상 뷰어에서 지정한 형식으로 확인되어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 새 이미지 세트의 축소판으로 사용되는 자산의 핸들입니다. 지정하지 않으면 IPS는 세트에서 참조하는 첫 번째 이미지 자산을 사용하려고 합니다. </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition에 대한 대체 함수**

카탈로그 조회 또는 게시 중에 해결되는 대체 함수를 라인에 지정할 수 있습니다. 대체 문자열에는 형식이 있습니다 `${<substitution_func>}`. 사용 가능한 함수는 아래에 열거됩니다.

>[!NOTE]
>
>매개 변수 목록의 핸들 리터럴은 대괄호로 둘러싸야 합니다 `([])`. 대체 문자열 외부에 있는 모든 텍스트는 해상도 동안 출력 문자열에 축어를 복사합니다.

| **대체 함수** | **반환** |
|---|---|
| `getFilePath([asset_handle>])` | 자산의 기본 소스 파일 경로입니다. |
| `getCatalogId([<asset_handle>])` | 자산의 카탈로그 ID. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | 자산에 대한 메타데이터 값. |
| `getThumbCatalogId([<asset_handle>])` | 자산의 카탈로그 ID(이미지 기반 자산에만 해당).연결된 thumb 자산의 카탈로그 ID(다른 자산에 대해). 연결된 thumb 자산을 사용할 수 없는 경우 함수는 빈 문자열을 반환합니다. |

**샘플 미디어 setDefinition 문자열**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

카탈로그 조회 또는 게시 시간에 이것은 다음과 유사한 문자열로 확인됩니다.

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**출력(createAssetSet)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 예 | 자산 세트의 핸들입니다. |

## 예제 {#section-fed53089de824d67ab96cd9103d384b4}

**요청**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**응답**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```

