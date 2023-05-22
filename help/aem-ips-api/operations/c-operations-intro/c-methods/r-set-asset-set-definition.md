---
description: 기존 에셋 세트에 대한 집합 정의를 업데이트합니다.
solution: Experience Manager
title: setAssetDefinition
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 6%

---

# setAssetDefinition{#setassetsetdefinition}

기존 에셋 세트에 대한 집합 정의를 업데이트합니다.

구문

## 승인된 사용자 유형 {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**입력(setAssetDefinitionParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 자산 세트가 있는 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 자산 집합 핸들 |
| setDefinition | `xsd:string` | 예 | 정의 문자열. 아래를 참조하십시오. |

**출력(setAssetSetDefinitionReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## setDefinition 매개 변수: 정보 {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition 함수**

지정 `setDefinition` 대체 함수는 인라인입니다. 이러한 문제는 카탈로그 조회 또는 게시 중에 해결됩니다. 대체 문자열의 형식은 다음과 같습니다. `${<substitution_func>}`을 클릭하고 다음을 포함합니다.

>[!NOTE]
>
>매개 변수 목록에서 리터럴을 처리하려면 대괄호로 묶어야 합니다. `([])`. 대체 문자열 외부의 텍스트는 확인 중에 출력 문자열로 복사됩니다.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 대체 함수 </th> 
   <th colname="col2" class="entry"> 자산 반환 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_핸들 </span>]) </span> </td> 
   <td colname="col2"> 기본 파일 경로. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_핸들 </span>]) </span> </td> 
   <td colname="col2"> 카탈로그 ID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_핸들 </span>],[ <span class="varname"> metadata_field_핸들 </span>]) </span> </td> 
   <td colname="col2"> 메타데이터 값. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_핸들 </span>]) </span> </td> 
   <td colname="col2"> 카탈로그 ID. 이미지 기반 에셋(이미지, 조정된 보기, 레이어 보기)에 적용됩니다. <p>다른 에셋의 경우 썸네일 에셋의 카탈로그 ID(있는 경우)를 반환합니다. 자산과 연결된 썸네일 자산이 없으면 이 함수는 빈 문자열을 반환합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition 예**

이 미디어 집합 정의 문자열:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

조회 또는 게시 시간에 다음 문제를 해결합니다.

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## 예제 {#section-739b42eec3074cafae285ec015a2d088}

**요청**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**응답**

없음.
