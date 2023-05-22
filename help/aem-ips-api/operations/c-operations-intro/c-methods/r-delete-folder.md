---
description: 폴더를 삭제합니다.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 11%

---

# deleteFolder{#deletefolder}

폴더를 삭제합니다.

구문

## 승인된 사용자 유형 {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 폴더 및 모든 하위 항목에 대한 읽기 및 삭제 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-a793c98a481a4f26ab50bc69b16b57e7}

**입력(deleteFolderParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 폴더가 속한 회사에 대한 핸들입니다. |
| folder핸들 | `xsd:string` | 예 | 삭제할 폴더의 핸들입니다. |

**출력(deleteFolderParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-9d4617b322e8442d80e59be0f8714841}

이 샘플 코드는 회사 루트에서 폴더를 삭제합니다. 폴더 핸들이 필요하며, 이 핸들은 다른 작업에서 받아야 합니다.

**요청**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

없음.
