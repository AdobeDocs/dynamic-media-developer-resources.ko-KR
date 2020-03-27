---
description: 새 이미지 맵을 만들거나 기존 맵을 편집합니다.
seo-description: 새 이미지 맵을 만들거나 기존 맵을 편집합니다.
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
topic: Scene7 Image Production System API
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageMap{#saveimagemap}

새 이미지 맵을 만들거나 기존 맵을 편집합니다.

구문

## 인증된 사용자 유형 {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-64f7f5fd8f954fba9fa30eeee556863a}

**입력(saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col1"> <span class="codeph"> 회사 <span class="varname"> 핸들 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 저장할 이미지 맵이 있는 회사 핸들 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 자산 <span class="varname"> 핸들 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 맵이 속하는 이미지 자산의 핸들 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageMapHandle <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 이미지 맵의 핸들입니다. NULL인 경우 이미지 맵을 만듭니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 만들거나 저장한 이미지 맵의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 모양 <span class="varname"> 유형 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 영역 모양 선택. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 지역 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 지역을 정의하는 쉼표로 구분된 포인트 목록. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 작업 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p>IPS 인터페이스에 지정된 이미지 맵과 연결된 <span class="codeph"> href </span> 값. </p> <p>href <span class="codeph"> </span> 값을 얻으려면 IPS 인터페이스에서 이미지를 클릭하고 URL을 복사하여 이 요소에 붙여 넣은 다음 IPS URL의 형식을 적절한 URL로 지정합니다. 예를 들어 <span class="codeph"> &amp;는 &amp;amp; </span> <span class="codeph"> 가 됩니다. </span>Adobe </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 위치 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 맵 목록(Z 축)의 순서. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 활성화됨 </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**출력(saveImageMapReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | 예 | 새 이미지 맵이나 편집된 이미지 맵의 핸들입니다. |

## 예제 {#section-fdac488b640f427c8aa3d549c5032851}

이 코드 샘플은 자산에 대한 새 이미지 맵을 만듭니다. 영역 모양 문자열 상수로 결정된 모양 유형을 사용하고 핸들을 새 이미지 맵으로 반환합니다.

**요청**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**응답**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```

