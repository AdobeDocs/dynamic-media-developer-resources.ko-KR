---
title: createAsset
description: 이미지 서버에 게시할 원시 집합 정의 문자열로 일반 자산 집합을 만듭니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 5%

---

# createAsset{#createassetset}

이미지 서버에 게시할 원시 집합 정의 문자열로 일반 자산 집합을 만듭니다.

구문

## 승인된 사용자 유형 {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-3580b586296e42a5b21426085b1bb72d}

**입력(createAsset)**

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
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 자산 세트가 포함된 회사에 대한 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 새 자산 세트가 생성되는 폴더에 대한 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 에셋 이름. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 하위 유형 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 에셋 세트 유형에 대해 클라이언트가 생성한 고유 식별자. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 집합 정의 문자열의 매개 변수입니다. <p>이러한 매개 변수는 대상 뷰어에서 지정한 형식으로 확인해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 새 이미지 세트의 썸네일 역할을 하는 에셋의 핸들입니다. 지정하지 않으면 IPS는 집합에 의해 참조되는 첫 번째 이미지 자산을 사용하려고 합니다. </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition에 대한 대체 함수**

카탈로그 조회 또는 게시 중에 해결되는 대체 함수를 인라인으로 지정할 수 있습니다. 대체 문자열의 형식은 `${<substitution_func>}`입니다. 사용 가능한 기능은 아래에 요약되어 있습니다.

>[!NOTE]
>
>매개 변수 목록의 핸들 리터럴은 대괄호 `([])`(으)로 둘러싸야 합니다. 대체 문자열 외부에 있는 모든 텍스트는 확인 중에 출력 문자열에 축어적으로 복사됩니다.

| **대체 함수** | **반환** |
|---|---|
| `getFilePath([asset_handle>])` | 자산의 기본 소스 파일 경로입니다. |
| `getCatalogId([<asset_handle>])` | 자산의 카탈로그 ID입니다. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | 에셋의 메타데이터 값. |
| `getThumbCatalogId([<asset_handle>])` | 자산의 카탈로그 ID(이미지 기반 자산만 해당). 연결된 썸네일 자산의 카탈로그 ID(다른 자산의 경우). 연결된 썸네일 자산을 사용할 수 없는 경우 이 함수는 빈 문자열을 반환합니다. |

**샘플 미디어 집합 정의 문자열**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

카탈로그 조회 또는 게시 시 이 프로세스는 다음과 유사한 문자열로 확인됩니다.

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**출력(createAsset)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetHandle | `xsd:string` | 예 | 자산 세트에 대한 핸들입니다. |

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
