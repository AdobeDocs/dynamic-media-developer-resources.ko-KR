---
description: 전달된 매개 변수를 기반으로 2개의 다른 유형의 정보를 반환합니다. OriginatorHandle은 지정된 자산에서 생성된 자산에 대한 정보를 반환합니다. generateHandle은 지정된 자산 또는 파일을 생성하는 데 사용되는 단계에 대한 정보를 반환합니다.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 9%

---


# getGenerationInfo{#getgenerationinfo}

전달된 매개 변수를 기반으로 2개의 다른 유형의 정보를 반환합니다. OriginatorHandle은 지정된 자산에서 생성된 자산에 대한 정보를 반환합니다. generateHandle은 지정된 자산 또는 파일을 생성하는 데 사용되는 단계에 대한 정보를 반환합니다.

구문

## 인증된 사용자 유형 {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-b7fa94c82147455888e8469fa5f6922b}

**입력(getGenerationInfoParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`코드 구문`*` | `xsd:string` | 예 | 회사의 손잡이입니다. |
| `*`코드 구문`*` | `xsd:string` | 아니요 | 세대에 사용된 엔진입니다. 글꼴 스타일을 참조하십시오. |
| `*`코드 구문`*` | `xsd:string` | 아니요 | 생성된 자산을 쿼리할 자산의 핸들. |
| `*`코드 구문`*` | `xsd:string` | 아니요 | 생성에 사용된 자산 및 엔진을 쿼리할 자산의 핸들. |
| `*`코드 구문`*` | `xsd:StringArray` | 아니요 | 작업에 포함된 속성입니다. |
| `*`코드 구문`*` | `xsd:StringArray` | 아니요 | 작업에서 제외된 속성입니다. |

**출력(getGenerationInfoReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | 예 | 생성 정보의 배열입니다. |

## 예제 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

이 코드 샘플은 특정 자산에서 생성된 자산에 대한 정보를 반환합니다. 지정된 자산을 생성하는 데 사용되는 단계에 대한 정보를 검색하지 않습니다. 잠시 동안 응답이 잘립니다.

**요청**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**응답**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```

