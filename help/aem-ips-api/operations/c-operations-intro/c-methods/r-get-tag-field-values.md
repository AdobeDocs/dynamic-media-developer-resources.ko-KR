---
description: 하나 이상의 태그 필드에 대해 정의된 모든 태그 사전 값을 가져옵니다.
seo-description: 하나 이상의 태그 필드에 대해 정의된 모든 태그 사전 값을 가져옵니다.
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
topic: Scene7 Image Production System API
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 16%

---


# getTagFieldValues{#gettagfieldvalues}

하나 이상의 태그 필드에 대해 정의된 모든 태그 사전 값을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-9ad806e7736e4d51ae42cad185050cf9}

**입력(getTagFieldValuesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 태그 필드를 포함하는 회사의 핸들입니다. |
| ` *`fieldHandleArray`*` | `types:HandleArray` | 예 | 반환하려는 태그 값에 대한 필드 핸들 배열입니다. |

**출력(getTagFieldValuesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`fieldArray`*` | `types:TagFieldValuesArray` | 예 | 요청된 각 필드에 대한 사전의 태그 값 배열입니다. |

## 예제 {#section-4492742614e44bb191a7d397dc1a1407}

**요청**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**응답**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```

