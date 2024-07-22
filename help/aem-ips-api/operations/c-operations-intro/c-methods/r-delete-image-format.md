---
description: 이미지 형식을 삭제합니다. saveImageFormat에서 이미지 형식 핸들을 가져옵니다.
solution: Experience Manager
title: 이미지 형식 삭제
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---

# 이미지 형식 삭제{#deleteimageformat}

이미지 형식을 삭제합니다. saveImageFormat에서 이미지 형식 핸들을 가져옵니다.

구문

## 승인된 사용자 유형 {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-462c05d9aad746ee8d2be0656041b693}

**입력(deleteImageFormatParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 삭제할 이미지 형식이 포함된 회사에 대한 핸들입니다. |
| imageFormatHandle | `xsd:string` | 예 | 삭제할 이미지 형식에 대한 핸들입니다. |

**출력(deleteImageFormatParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

이 코드 샘플은 회사에서 이미지 형식을 삭제합니다. 다른 작업에서 이미지 형식 핸들을 가져옵니다.

**요청**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**응답**

없음.

**관련 항목:**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
