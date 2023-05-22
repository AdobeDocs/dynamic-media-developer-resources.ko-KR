---
description: 폴더를 새 위치로 이동합니다.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 28%

---

# moveFolder{#movefolder}

폴더를 새 위치로 이동합니다.

구문

## 승인된 사용자 유형 {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-473c2e68bcc14a9ea2593bee26e679dd}

**입력(moveFolderParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| folder핸들 | `xsd:string` | 예 | 폴더 핸들. |
| destFolderHandle | `xsd:string` | 예 | 대상 폴더에 대한 를 처리합니다. |

**출력(moveFolderReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| folder핸들 | `xsd:string` | 예 | 이동된 폴더로 처리합니다. |

## 예제 {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**요청**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**응답**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```
