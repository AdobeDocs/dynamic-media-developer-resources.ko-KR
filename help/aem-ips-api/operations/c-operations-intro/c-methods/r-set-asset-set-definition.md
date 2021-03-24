---
description: 기존 자산 집합에 대한 세트 정의를 업데이트합니다.
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,자산 관리
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 6%

---


# setAssetSetDefinition{#setassetsetdefinition}

기존 자산 집합에 대한 세트 정의를 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-9d4ca3a8cfe74934b89971de01a2143c}

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
| `*`companyHandle`*` | `xsd:string` | 예 | 자산 세트가 있는 회사의 핸들입니다. |
| `*`assetHandle`*` | `xsd:string` | 예 | 자산 집합 핸들 |
| `*`setDefinition`*` | `xsd:string` | 예 | 정의 문자열. 아래를 참조하십시오. |

**출력(setAssetSetDefinitionReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## setDefinition 매개 변수:{#section-f88e066bf5294b4f8c12d5d652a5c94c} 정보

**setDefinition 함수**

`setDefinition` 대체 함수를 인라인 형식으로 지정합니다. 이러한 문제는 카탈로그 조회 또는 게시 중에 해결됩니다. 대체 문자열에는 `${<substitution_func>}` 형식이 있으며 다음을 포함합니다.

>[!NOTE]
>
>매개 변수 목록의 핸들 리터럴은 대괄호 `([])`로 둘러싸야 합니다. 대체 문자열 외부의 텍스트는 해상도 동안 출력 문자열에 복사됩니다.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 대체 함수 </th> 
   <th colname="col2" class="entry"> 자산의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> 기본 파일 경로. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalygd([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> 카탈로그 ID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([  <span class="varname"> asset_handle  </span>],[  <span class="varname"> metadata_field_handle  </span>])  </span> </td> 
   <td colname="col2"> 메타데이터 값. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> 카탈로그 ID. 이미지 기반 자산(이미지, 조정된 보기, 레이어 보기)에 적용됩니다. <p>다른 자산에 대해서는 thumb 자산의 카탈로그 ID(있는 경우)를 반환합니다. 축소판 자산이 자산과 연결되어 있지 않으면 이 함수는 빈 문자열을 반환합니다. </p> </td> 
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

조회 또는 게시 시간에 다음 사항을 해결합니다.

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
