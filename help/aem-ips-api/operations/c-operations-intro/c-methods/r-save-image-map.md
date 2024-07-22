---
description: 새 이미지 맵을 만들거나 기존 맵을 편집합니다.
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 8%

---

# saveImageMap{#saveimagemap}

새 이미지 맵을 만들거나 기존 맵을 편집합니다.

구문

## 승인된 사용자 유형 {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자에게 에셋에 대한 읽기 및 쓰기 권한이 있어야 합니다.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 저장할 이미지 맵이 있는 회사의 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 맵이 속한 이미지 에셋에 대한 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 이미지 맵에 대한 핸들입니다. NULL인 경우 이미지 맵을 만듭니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 생성되거나 저장된 이미지 맵의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 지역 셰이프 선택. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 지역 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 영역을 정의하는 쉼표로 구분된 포인트 목록입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 작업 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p>IPS 인터페이스에 지정된 대로 이미지 맵과 연결된 <span class="codeph"> href </span> 값입니다. </p> <p><span class="codeph"> href </span> 값을 가져오려면 IPS 인터페이스에서 이미지를 클릭하고 URL을 복사하여 이 요소에 붙여 넣은 다음 IPS URL의 형식을 적절한 URL로 지정하십시오. 예를 들어 <span class="codeph"> 및 </span>은(는) <span class="codeph"> &amp;amp; </span>이(가) 됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 위치 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 맵 목록의 순서(Z축)입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 사용 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**출력(saveImageMapReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 이미지 맵 핸들 | `xsd:string` | 예 | 새 이미지 맵 또는 편집된 이미지 맵에 대한 핸들입니다. |

## 예제 {#section-fdac488b640f427c8aa3d549c5032851}

이 코드 샘플은 자산에 대한 새 이미지 맵을 만듭니다. 영역 모양 문자열 상수로 결정된 모양 유형을 사용하고 새 이미지 맵에 핸들을 반환합니다.

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
