---
description: 이미지 맵을 삭제합니다.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 12%

---

# deleteImageMap{#deleteimagemap}

이미지 맵을 삭제합니다.

구문

## 인증된 사용자 유형 {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-28de12bab79045a5977c68855e37ae3d}

**입력(deleteImageMapParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 삭제할 이미지 맵이 포함된 회사의 핸들입니다. |
| imageMapHandle | `xsd:string` | 예 | 삭제할 이미지 맵의 핸들입니다. |

**출력(deleteImageMapParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

이 코드 샘플은 회사에서 이미지 맵을 삭제합니다. 다른 작업에서 이미지 맵 핸들을 가져와야 합니다.

**요청**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**응답**

없음
