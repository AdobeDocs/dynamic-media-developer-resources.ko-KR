---
description: 속성 집합은 속성 집합 유형에 따라 다양한 IPS 개체에 첨부할 수 있는 응용 프로그램별 이름-값 쌍 집합입니다. 속성 집합 형식에서 개체에 여러 집합을 첨부할 수 없는 경우(PropertySetType/allowMultipleisfalse) 개체에 이미 같은 형식의 연결된 집합이 있으면 새 집합이 기존 집합을 대체합니다.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 7%

---

# createPropertySet{#createpropertyset}

속성 집합은 속성 집합 유형에 따라 다양한 IPS 개체에 첨부할 수 있는 응용 프로그램별 이름-값 쌍 집합입니다. 속성 집합 형식에서 개체에 여러 집합을 첨부할 수 없는 경우(PropertySetType/allowMultipleisfalse) 개체에 이미 같은 형식의 연결된 집합이 있으면 새 집합이 기존 집합을 대체합니다.

구문

## 승인된 사용자 유형 {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-25258e75f5f3419bad165c797eb6cd8e}

**입력(createPropertySetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| typeHandle | `xsd:string` | 예 | 속성 집합 유형에 대한 핸들입니다. |
| primaryOwner핸들 | `xsd:string` | 예 | 속성 집합의 기본 소유자에 대한 핸들입니다. |
| secondaryOwner핸들 | `xsd:string` | 아니요 | 속성 집합의 보조 소유자에 대한 핸들입니다. |
| propertyArray | `types:PropertyArray` | 예 | 속성의 배열입니다. |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**출력(createPropertySetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| setHandle | `xsd:string` | 예 | 새 속성 집합에 대한 핸들입니다. |

## 예제 {#section-4e1f5b2883664bc88f590fcd253df22b}

이 코드 샘플은 속성의 이름과 값을 포함하는 속성 집합을 만듭니다. 이 응답은 새 속성 집합에 대한 핸들을 반환합니다.

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
