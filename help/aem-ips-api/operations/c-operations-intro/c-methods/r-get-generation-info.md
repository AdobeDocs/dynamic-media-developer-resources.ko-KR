---
description: 전달된 매개 변수를 기반으로 두 가지 서로 다른 유형의 정보를 반환합니다. originatorHandle은 지정된 에셋에서 생성된 에셋에 대한 정보를 반환합니다. generateHandle은 지정된 에셋 또는 파일을 생성하는 데 사용되는 단계에 대한 정보를 반환합니다.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 9%

---

# getGenerationInfo{#getgenerationinfo}

전달된 매개 변수를 기반으로 두 가지 서로 다른 유형의 정보를 반환합니다. originatorHandle은 지정된 에셋에서 생성된 에셋에 대한 정보를 반환합니다. generateHandle은 지정된 에셋 또는 파일을 생성하는 데 사용되는 단계에 대한 정보를 반환합니다.

구문

## 승인된 사용자 유형 {#section-9cc2216b32c74107be07aeacecc11401}

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
| 코드 구 | `xsd:string` | 예 | 회사 손잡이. |
| 코드 구 | `xsd:string` | 아니요 | 세대에 사용된 엔진. 글꼴 스타일을 참조하십시오. |
| 코드 구 | `xsd:string` | 아니요 | 생성된 에셋을 쿼리할 에셋의 핸들입니다. |
| 코드 구 | `xsd:string` | 아니요 | 생성에 사용된 에셋 및 엔진을 쿼리하는 에셋의 핸들입니다. |
| 코드 구 | `xsd:StringArray` | 아니요 | 작업에 포함된 속성입니다. |
| 코드 구 | `xsd:StringArray` | 아니요 | 작업에서 제외된 속성입니다. |

**출력(getGenerationInfoReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | 예 | 생성 정보 배열. |

## 예제 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

이 코드 샘플은 특정 에셋에서 생성된 에셋에 대한 정보를 반환합니다. 지정된 에셋을 생성하는 데 사용되는 단계에 대한 정보는 검색하지 않습니다. 응답은 간결성을 위해 잘립니다.

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
