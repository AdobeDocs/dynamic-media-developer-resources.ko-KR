---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 21%

---

# getVignettePublishFormats{#getvignettepublishformats}

구문

## 승인된 사용자 유형 {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**입력(getVignettePublishFormatsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 손잡이. |

**출력(getVignettePublishFormatsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 비네팅 포맷 | `types:VignettePublishFormatArray` | 예 | 비네팅 게시 형식 배열. |

## 예제 {#section-2cc32b27cc6243b7b3e273cc05996226}

이 코드 샘플은 특정 회사와 연결된 두 개의 비네팅 게시 형식을 반환합니다. 정보는 배열로 반환되며, 간결성을 위해 잘립니다.

**요청**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**응답**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```
