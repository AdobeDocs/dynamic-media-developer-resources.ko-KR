---
description: 단일 요청에서 모든 시스템 속성을 검색합니다.
seo-description: 단일 요청에서 모든 시스템 속성을 검색합니다.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
topic: Scene7 Image Production System API
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getSystemProperties{#getsystemproperties}

단일 요청에서 모든 시스템 속성을 검색합니다.

구문

## 인증된 사용자 유형 {#section-fc311ce90a54400fa95b9dd36b756e23}

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
| ` *`propertyArray`*` | `types:PropertyArray` | 예 | 시스템 속성의 배열입니다. |

## 예제 {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

이 코드 샘플은 시스템 속성의 배열을 반환합니다. 간결한 응답입니다.

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

