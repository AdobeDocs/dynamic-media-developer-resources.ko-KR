---
description: 그룹을 삭제합니다.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 13%

---

# deleteGroup{#deletegroup}

그룹을 삭제합니다.

구문

## 인증된 사용자 유형 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-42775102ec724c36ae5241eea1a00b8e}

**입력(deleteGroupParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 삭제할 그룹에 속하는 회사의 핸들입니다. |
| `*`groupHandle`*` | `xsd:string` | 예 | 삭제할 그룹의 핸들입니다. |

**출력(deleteGroupParam)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

이 샘플 코드는 회사에서 그룹을 삭제합니다. 다른 작업에서 가져와야 하는 그룹 핸들이 필요합니다.

**요청**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**응답**

없음.
