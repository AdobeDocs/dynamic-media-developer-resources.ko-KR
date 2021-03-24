---
description: 이미지 맵을 삭제합니다.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
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
>사용자에게 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-28de12bab79045a5977c68855e37ae3d}

**입력(deleteImageMapParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 삭제할 이미지 맵을 포함하는 회사의 핸들입니다. |
| `*`imageMapHandle`*` | `xsd:string` | 예 | 삭제할 이미지 맵의 핸들입니다. |

**출력(deleteImageMapParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

이 코드 샘플은 회사에서 이미지 맵을 삭제합니다. 다른 작업에서 이미지 맵 핸들을 구해야 합니다.

**요청**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**응답**

없음
