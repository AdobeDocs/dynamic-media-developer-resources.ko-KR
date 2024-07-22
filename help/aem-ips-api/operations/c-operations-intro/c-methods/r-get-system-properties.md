---
description: 단일 요청에서 모든 시스템 속성을 검색합니다.
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 16%

---

# getSystemProperties{#getsystemproperties}

단일 요청에서 모든 시스템 속성을 검색합니다.

구문

## 승인된 사용자 유형 {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 매개 변수 {#section-b2a4fb7068424223aec87c50f0586d73}

**입력(getSystemPropertiesParam)**

없음.

**출력(getSystemPropertiesReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| propertyArray | `types:PropertyArray` | 예 | 시스템 속성의 배열입니다. |

## 예제 {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

이 코드 샘플은 시스템 속성의 배열을 반환합니다. 간결성을 위해 응답이 잘렸습니다.

**요청**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**응답**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```
