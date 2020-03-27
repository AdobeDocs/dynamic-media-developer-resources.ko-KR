---
description: 지정된 자산과 연결된 자산 및 해당 관계에 대한 세부 정보를 가져옵니다.
seo-description: 지정된 자산과 연결된 자산 및 해당 관계에 대한 세부 정보를 가져옵니다.
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
topic: Scene7 Image Production System API
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssociatedAssets{#getassociatedassets}

지정된 자산과 연결된 자산 및 해당 관계에 대한 세부 정보를 가져옵니다.

구문

## 인증된 사용자 유형 {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-d11d0dab59e94e89b466123a0ebfa82e}

**입력(getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>자산을 소유한 회사에 대해 처리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 자산 <span class="varname"> 핸들</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>자산 핸들. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 응답 <span class="varname"> FieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>원하는 응답 필드의 배열입니다. introduction의 response- FieldArray/excludeFieldArray를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> excludeFieldArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>제외된 응답 필드의 배열입니다. introduction의 response- FieldArray/excludeFieldArray를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> containerArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 자산이 들어 있는 세트 및 템플릿 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> memberArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 세트 또는 템플릿 자산에 포함된 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> layerReferenceArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>레이어 또는 템플릿 URL에서 참조되는 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ownerArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 자산을 소유하는 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 파생 <span class="varname"> 배열</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 자산을 생성하는 데 사용된 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> generatorArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>생성기 <span class="codeph"> 배열은</span> 이 자산이 생성된 방식을 나열합니다. 예를 들어 assetHandler <span class="codeph"> 가</span> PDF의 이미지 페이지인 경우 PDF 프로세서 도구가 포함되고 PdfFile 에셋을 참조합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 생성된 <span class="varname"> 배열</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>생성된 <span class="codeph"> 배열은</span> 이 자산이 생성된 방식을 반전합니다. 예를 들어 <span class="codeph"> 생성된 배열은</span> 이 assetHandler에서 생성된 이미지 목록을 포함할 수 <span class="codeph"> 있습니다</span> (PdfFile 자산인 경우). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> thumb <span class="varname"> Asset</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:자산</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>요청 자산과 연결된 축소판 자산 정보. 축소판 자산이 할당되지 않은 경우 응답에서 필드가 생략됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

매개 변수를 `responseFieldArray` 사용하거나 응답 크기를 `excludeFieldArray` 제한할 수 있습니다. 특히, `GenerationInfo` 기본적으로 반환되는 항목은 작성자와 생성된 자산 레코드 모두를 포함하도록 `generatorArray` `generatedArray` 반환됩니다. PDF 에셋 유형의 경우 이 동작을 수행하면 응답에서 &quot;보낸 사람&quot; PDF 에셋 레코드의 원하지 않는 여러 사본이 나타납니다. 에 추가하여 이 문제를 제거할 `generatedArray/items/originator` 수 `excludeFieldArray`있습니다. 또는 포함할 명시적 응답 필드 목록을 지정할 수 `responseFieldArray`있습니다.

## 예제 {#section-8946ea4b9cb94912a8408249c897f192}

다음 기본 예는 PDF에서 추출된 이미지에 대한 생성기의 핸들에 대한 요청입니다. PDF `containerArray` 를 포함한 항목이 있는 길이가 1개입니다 `assetHandle` .

**요청**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**응답**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

위의 예제의 반대는 다음과 같습니다.

**요청**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**응답**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

다음 예에서는 그룹이 있는 회사에 추가됩니다 `groupHandleArray`. 이 예에서는 하나의 그룹만 사용합니다.

**요청**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**응답**

없음.
