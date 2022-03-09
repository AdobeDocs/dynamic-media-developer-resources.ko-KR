---
description: 속성 배열을 사용하여 속성 세트를 업데이트합니다.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---

# updatePropertySet{#updatepropertyset}

속성 배열을 사용하여 속성 세트를 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-98361b063e9c41e8b2f744fabc0e13ed}

**입력(updatePropertySetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| setHandle | `xsd:string` | 예 | 속성 집합을 처리합니다. |
| replaceProperties | `xsd:string` | 아니요 | 을 로 설정합니다. `true` 를 클릭하여 속성을 바꿉니다. |
| propertyArray | `types:PropertyArray` | 예 | 속성 세트에 대해 업데이트된 속성의 배열입니다. |

**출력(updatePropertySetReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

이 코드 샘플은 속성 배열의 속성이 있는 속성 세트를 업데이트합니다.

**요청**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**응답**

없음.
