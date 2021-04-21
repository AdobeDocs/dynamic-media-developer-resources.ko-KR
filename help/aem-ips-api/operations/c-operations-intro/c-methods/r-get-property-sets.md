---
description: 유형 아이디와 연결된 속성 집합을 가져옵니다.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 17%

---


# getPropertySets{#getpropertysets}

유형 아이디와 연결된 속성 집합을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-d8da2847e77e4a95a4441d9848cac775}

**입력(getPropertySetsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 예 | 속성 집합 유형의 핸들입니다. |
| `*`primaryOwnerHandle`*` | `xsd:string` | 예 | 데이터베이스 객체에 바인딩된 데이터의 기본 소유자입니다. |
| `*`secondaryOwnerHandle`*` | `xsd:string` | 아니요 | 데이터의 보조 소유자(선택 사항). |

**출력(getPropertySetsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`setArray`*` | `types:PropertySetArray` | 예 | 속성 집합 배열. |

## 예제 {#section-1358af974eab4259864910337a6f0bd2}

이 코드 샘플은 형식 핸들로 지정된 기본 소유자의 속성 집합을 반환합니다.

**요청**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**응답**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```

