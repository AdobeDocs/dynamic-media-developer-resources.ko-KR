---
description: 태그 필드의 태그 사전 값을 업데이트합니다.
seo-description: 태그 필드의 태그 사전 값을 업데이트합니다.
seo-title: updateTagFieldValues
solution: Experience Manager
title: updateTagFieldValues
topic: Scene7 Image Production System API
uuid: 21689469-a0dd-480b-82ba-ebd12956ff8f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 12%

---


# updateTagFieldValues{#updatetagfieldvalues}

태그 필드의 태그 사전 값을 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-0a3a4bab026746238c9d4009caf42e94}

**입력(updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 회사 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 태그 필드 핸들입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagValueUpdateArray</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4">업데이트할 태그 필드 값의 배열입니다. <p>참고: 태그 문자열 값만 업데이트합니다. 자산 연결에 영향을 주지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(updateTagFieldValuesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | 성공적으로 태그 필드 업데이트 수입니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | 작업이 태그 필드를 업데이트하려고 할 때 생성된 경고 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | 작업이 태그 필드를 업데이트하려고 할 때 생성되는 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | 아니요 | 작업이 태그 필드를 업데이트하려고 할 때 경고를 생성한 자산과 연결된 세부 사항의 배열입니다. |
| ` *`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | 아니요 | 작업이 태그 필드를 업데이트하려고 할 때 오류를 생성한 자산과 연결된 세부 사항의 배열입니다. |

## 예제 {#section-bb4dcf97044c4675974c9b8d27674001}

**요청**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**응답**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

