---
description: searchAssets에 사용할 검색어를 추가합니다.
seo-description: searchAssets에 사용할 검색어를 추가합니다.
seo-title: MetadataCondition
solution: Experience Manager
title: MetadataCondition
topic: Scene7 Image Production System API
uuid: 9d65b8ce-86a5-4730-af84-a87134fd7db6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MetadataCondition{#metadatacondition}

searchAssets에 사용할 검색어를 추가합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 필드 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 문자열 비교 연산자 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 값</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 테스트할 값입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 벌</span> 발 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 부울 비교 값(부울 형식의 필드에만 해당) </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 긴</span> 발 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 긴 비교 값(int 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 최소</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 범위 비교의 최소 긴 값(int 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 최대 <span class="varname"> 긴</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 범위 비교의 최대 긴 값(int 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> 이중 비교 값(부동 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 최소</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> 범위 비교의 최소 이중 값(부동 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 최대</span> 이중 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> 범위 비교의 최대 이중 값(부동 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 날짜 <span class="varname"> 값</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 날짜 비교 값(날짜 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 최소</span> 날짜 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 범위 비교의 최소 날짜 값(날짜 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 최대 <span class="varname"> 날짜</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 범위 비교의 최대 날짜 값(날짜 입력 필드에만 해당). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 대/ <span class="varname"> 소문자 구분</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p> 메타데이터 서버의 대/소문자 구분 설정 searchAssetsByMetadata <span class="codeph"> 호출에</span> 사용됩니다. </p> <p>searchAssetsBy <a href="../../operations/c-operations-intro/c-methods/r-search-assets-by-metadata.md#reference-609ec73944a34ce49b152389fbb40414" format="dita" scope="local"> Metadata를 참조하십시오</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

