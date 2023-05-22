---
description: getPublishContexts
solution: Experience Manager
title: getPublishContexts
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7b26e659-71b9-40c4-9df4-94e78c3e4baf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 20%

---

# getPublishContexts{#getpublishcontexts}

구문

## 승인된 사용자 유형 {#section-1a3a50349b5640dd8e498ff9e9c37340}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* 에셋을 반환하려면 사용자에게 읽기 권한이 있어야 합니다.
>* 모든 사용자는 공유 회사에 액세스할 수 있습니다.
>


## 매개 변수 {#section-d08e2175d3f84774b55b91bc590b8b3f}

**입력(getPublishContextsParam)**

<table id="table_4A505A067586464B99F8F68E3B1BE75E"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> company핸들</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 회사를 위해 처리하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> contextType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4">반환할 게시 컨텍스트의 유형입니다. 포함 사항: 
    <ul id="ul_21EDF8F0026E402EAE8226A0CADEE652">
     <li id="li_06DB502952D943198F16C06C59816268"><span class="codeph"> 이미지 제공</span></li>
     <li id="li_E67A42934E8F4689A148CE125F7372AE"><span class="codeph"> 이미지 렌더링</span></li>
     <li id="li_3CB3A9C4E7AB4A71819567A9566E396C"><span class="codeph"> 비디오</span></li>
     <li id="li_27E3DB89B53B4B50B2231622A157A228"><span class="codeph"> ServerDirectory</span></li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

**출력(getPublishContextsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| publishContextArray | 유형:PublishContextArray | 예 | 필요한 경우 컨텍스트 유형으로 필터링된 회사의 게시 컨텍스트 배열. |

## 예제 {#section-23fb7d6a15004b7eb4c3d3bcb37ceb04}

**요청**

```java
<getPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
</getPublishContextsParam>
```

**응답**

```java
<getPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
  <publishContextArray>
    <items>
      <contextHandle>pc|3001</contextHandle>
      <contextName>ImageRendering</contextName>
      <contextType>ImageRendering</contextType>
    </items>
    <items>
      <contextHandle>pc|3002</contextHandle>
      <contextName>ImageServing</contextName>
      <contextType>ImageServing</contextType>
    </items>
    <items>
      <contextHandle>pc|3003</contextHandle>
      <contextName>ServerDirectory</contextName>
      <contextType>ServerDirectory</contextType>
    </items>
    <items>
      <contextHandle>pc|3004</contextHandle>
      <contextName>Video</contextName>
      <contextType>Video</contextType>
    </items>
  </publishContextArray>
</getPublishContextsReturn>
```
