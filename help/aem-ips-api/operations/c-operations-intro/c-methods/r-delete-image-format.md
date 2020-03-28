---
description: 이미지 형식을 삭제합니다. saveImageFormat에서 이미지 형식 핸들을 가져옵니다.
seo-description: 이미지 형식을 삭제합니다. saveImageFormat에서 이미지 형식 핸들을 가져옵니다.
seo-title: deleteImageFormat
solution: Experience Manager
title: deleteImageFormat
topic: Scene7 Image Production System API
uuid: 70dddde9-830b-4267-8ef5-df5241f549e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteImageFormat{#deleteimageformat}

이미지 형식을 삭제합니다. saveImageFormat에서 이미지 형식 핸들을 가져옵니다.

구문

## 인증된 사용자 유형 {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-462c05d9aad746ee8d2be0656041b693}

**입력(deleteImageFormatParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 삭제할 이미지 형식이 포함된 회사의 핸들 |
| ` *`imageFormatHandle`*` | `xsd:string` | 예 | 삭제할 이미지 형식의 핸들입니다. |

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
