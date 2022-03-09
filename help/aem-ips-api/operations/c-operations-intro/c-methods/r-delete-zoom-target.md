---
description: 확대/축소 대상을 삭제합니다.
solution: Experience Manager
title: deleteZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa1f7cf8-038a-4fa8-b869-12ce4b2ad41f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 13%

---

# deleteZoomTarget{#deletezoomtarget}

확대/축소 대상을 삭제합니다.

## 인증된 사용자 유형 {#section-09ca82bc817e49048271c5cba545702e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-225330a45e7a408f8375e084677d9cb1}

**입력(deleteZoomTargetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 확대/축소 대상이 속하는 회사의 핸들입니다. |
| zoomTargetHandle | `xsd:string` | 예 | 삭제할 확대/축소 타겟의 핸들입니다. |

**출력(deleteZoomTargetParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예 {#section-a35857a5ca884357a879f7ba6cf985fe}

이 코드 샘플은 회사에서 확대/축소 타겟을 삭제합니다.

**요청**

```java
<ns1:deleteZoomTargetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:zoomTargetHandle>34194|9|301</ns1:zoomTargetHandle>
</ns1:deleteZoomTargetParam>
```

**응답**

없음.
