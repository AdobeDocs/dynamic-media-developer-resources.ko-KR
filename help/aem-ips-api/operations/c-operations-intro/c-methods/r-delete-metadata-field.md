---
description: 회사의 메타데이터 필드를 삭제합니다.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deleteMetadataField{#deletemetadatafield}

회사의 메타데이터 필드를 삭제합니다.

구문

## 인증된 사용자 유형 {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-73f12a30cc4340b6b32dd11effd5195e}

**입력(deleteMetadataFieldParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 삭제할 메타데이터 필드가 포함된 회사의 핸들입니다. |
| fieldHandle | `xsd:string` | 예 | 삭제할 메타데이터 필드의 핸들입니다. |

**출력(deleteMetadataFieldParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

이 코드 샘플은 회사의 메타데이터 필드를 삭제합니다. 회사 핸들 및 메타데이터 핸들을 `deleteMetadataFieldParam` 이 작업을 수행하기 위해 IPS 웹 서비스 서버에 전달되었습니다.

**요청**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**응답**

없음.0
