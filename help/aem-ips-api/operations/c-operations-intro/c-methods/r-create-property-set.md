---
description: 속성 세트는 속성 세트 유형에 따라 다양한 IPS 객체에 첨부할 수 있는 응용 프로그램별 이름-값 쌍 세트입니다. 속성 집합 유형에서 객체에 여러 집합을 연결할 수 없고(PropertySetType/allowMultiplisfalse) 이미 동일한 유형의 연결된 집합이 있는 경우 새 세트가 기존 집합을 대체합니다.
seo-description: 속성 세트는 속성 세트 유형에 따라 다양한 IPS 객체에 첨부할 수 있는 응용 프로그램별 이름-값 쌍 세트입니다. 속성 집합 유형에서 객체에 여러 집합을 연결할 수 없고(PropertySetType/allowMultiplisfalse) 이미 동일한 유형의 연결된 집합이 있는 경우 새 세트가 기존 집합을 대체합니다.
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
topic: Scene7 Image Production System API
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 6%

---


# createPropertySet{#createpropertyset}

속성 세트는 속성 세트 유형에 따라 다양한 IPS 객체에 첨부할 수 있는 응용 프로그램별 이름-값 쌍 세트입니다. 속성 집합 유형에서 객체에 여러 집합을 연결할 수 없고(PropertySetType/allowMultiplisfalse) 이미 동일한 유형의 연결된 집합이 있는 경우 새 세트가 기존 집합을 대체합니다.

구문

## 인증된 사용자 유형 {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-25258e75f5f3419bad165c797eb6cd8e}

**입력(createPropertySetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | 예 | 속성 집합 유형의 핸들입니다. |
| ` *`primaryOwnerHandle`*` | `xsd:string` | 예 | 속성 세트의 기본 소유자에 대한 핸들입니다. |
| ` *`secondaryOwnerHandle`*` | `xsd:string` | 아니요 | 속성 세트의 보조 소유자에 대한 핸들입니다. |
| ` *`propertyArray`*` | `types:PropertyArray` | 예 | 속성의 배열입니다. |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**출력(createPropertySetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | 예 | 새 속성 세트의 핸들입니다. |

## 예제 {#section-4e1f5b2883664bc88f590fcd253df22b}

이 코드 샘플은 속성의 이름과 값을 포함하는 속성 세트를 만듭니다. 응답에서 새 속성 집합에 대한 핸들을 반환합니다.

**요청**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**응답**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

