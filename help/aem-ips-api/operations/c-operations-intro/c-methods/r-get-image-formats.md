---
description: PDF, EPS, SWF 등과 같은 이미지 형식을 반환합니다.
solution: Experience Manager
title: getImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 20%

---

# getImageFormat{#getimageformats}

PDF, EPS, SWF 등과 같은 이미지 형식을 반환합니다.

구문

## 승인된 사용자 유형 {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-eefa36a70b74498f8727ef61d98cfb63}

**입력(getImageFormatsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 가져오려는 이미지 형식이 있는 회사에 대한 핸들입니다. |

**출력(getImageFormatsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | 예 | 이미지 형식 배열입니다. |

## 예제 {#section-73881e12839b4904bf3299b0920bdd0c}

이 코드 샘플은 지정된 회사의 모든 이미지 형식을 반환합니다.

**요청**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**응답**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```
