---
description: 지정된 자산과 연결된 자산 및 해당 관계의 세부 정보를 가져옵니다.
solution: Experience Manager
title: getAssociatedAssets
feature: Dynamic Media Classic,SDK/API,자산 관리
role: Developer,Admin
exl-id: cf49719f-5d79-4e64-a785-bf3b2fe200c7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 7%

---

# getAssociatedAssets{#getassociatedassets}

지정된 자산과 연결된 자산 및 해당 관계의 세부 정보를 가져옵니다.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>자산을 소유한 회사에 처리합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>자산 핸들. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:StringArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>원하는 응답 필드의 배열입니다. 소개에서 response- FieldArray/excludeFieldArray 를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 유형:StringArray</span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>제외된 응답 필드의 배열입니다. 소개에서 response- FieldArray/excludeFieldArray 를 참조하십시오. </p> </td> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 자산이 포함된 세트 및 템플릿 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 세트 또는 템플릿 자산에 포함된 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>레이어 또는 템플릿 URL에서 참조되는 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 자산을 소유한 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:AssetArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>지정된 자산을 생성하는 데 사용된 자산의 배열입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p><span class="codeph"> generatorArray</span> 는 이 자산이 생성된 방법을 나열합니다. 예를 들어 <span class="codeph"> assetHandler</span>가 PDF의 이미지 페이지인 경우 PDF 프로세서 도구가 포함되고 PdfFile 자산을 참조합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p><span class="codeph"> generatedArray</span>는 이 자산이 생성된 방식을 반전합니다. 예를 들어 <span class="codeph"> generatedArray</span>은(는) 이 <span class="codeph"> assetHandler</span>에서 생성된 이미지 목록이 PdfFile 자산인 경우 포함할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:자산</span> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>요청 자산과 연관된 경험 자산 정보입니다. 엄지손가락 자산이 할당되지 않은 경우 응답에서 필드가 생략됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

매개 변수 `responseFieldArray` 또는 `excludeFieldArray`을 사용하여 응답 크기를 제한할 수 있습니다. 특히 `generatorArray` 또는 `generatedArray`에서 반환되는 `GenerationInfo` 항목은 기본적으로 작성자와 생성된 자산 레코드를 모두 포함합니다. PDF 자산 유형의 경우, 이 동작으로 응답에 &quot;작성자&quot; PDF 자산 레코드의 여러 복사본이 원치 않게 됩니다. `excludeFieldArray`에 `generatedArray/items/originator`을 추가하여 이 문제를 제거할 수 있습니다. 또는 `responseFieldArray`에 포함할 명시적 응답 필드 목록을 지정할 수 있습니다.

## 예제 {#section-8946ea4b9cb94912a8408249c897f192}

다음은 PDF에서 추출된 이미지에 대한 생성기 핸들의 요청입니다. 여기에는 PDF의 `assetHandle`을 포함하는 항목이 있는 길이 1의 `containerArray`이 포함됩니다.

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

위의 예제의 역수는 다음과 같습니다.

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

다음 예에서는 그룹이 `groupHandleArray` 을 사용하는 회사에 추가됩니다. 이 예제에서는 하나의 그룹만 사용합니다.

**요청**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**응답**

없음.
