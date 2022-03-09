---
description: 태그 필드의 태그 사전 값을 업데이트합니다.
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 13%

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
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 회사 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 태그 필드 핸들. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:TagValueUpdateArray</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4">업데이트할 태그 필드 값의 배열입니다. <p>참고: 태그 문자열 값만 업데이트합니다. 자산 연결에는 영향을 주지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(updateTagFieldValuesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| successCount | `xsd:int` | 예 | 태그 필드를 성공적으로 업데이트했습니다. |
| warningCount | `xsd:int` | 예 | 작업에서 태그 필드를 업데이트하려고 할 때 생성된 경고 수입니다. |
| errorCount | `xsd:int` | 예 | 작업에서 태그 필드를 업데이트하려고 할 때 생성된 오류 수입니다. |
| warningDetailArray | `types:TagValueUpdateFaultArray` | 아니요 | 작업에서 태그 필드를 업데이트하려고 할 때 경고를 생성한 자산과 연관된 세부 정보의 배열입니다. |
| errorDetailArray | `types:TagValueUpdateFaultArray` | 아니요 | 작업에서 태그 필드를 업데이트하려고 할 때 오류를 생성한 자산과 연관된 세부 정보의 배열입니다. |

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

```java {.line-numbers}
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
