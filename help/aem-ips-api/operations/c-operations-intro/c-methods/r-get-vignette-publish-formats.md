---
description: 널
seo-description: 널
seo-title: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
topic: Scene7 Image Production System API
uuid: 2cf58002-5c4a-4391-85d4-4a67cb085afa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getVignettePublishFormats{#getvignettepublishformats}

구문

## 인가된 사용자 유형 {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**입력(getVignettePublishFormatsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사의 손잡이입니다. |

**출력(getVignettePublishFormatsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | 예 | 비네팅 게시 형식 배열입니다. |

## 예제 {#section-2cc32b27cc6243b7b3e273cc05996226}

이 코드 샘플은 특정 회사와 연결된 두 개의 비네팅 게시 형식을 반환합니다. 정보가 배열로 반환되며 간결하게 잘립니다.

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

