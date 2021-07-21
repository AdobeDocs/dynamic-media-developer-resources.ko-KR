---
description: 폴더 이름을 변경합니다.
solution: Experience Manager
title: renameFolder
feature: Dynamic Media Classic,SDK/API,자산 관리
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 20%

---

# renameFolder{#renamefolder}

폴더 이름을 변경합니다.

구문

## 인증된 사용자 유형 {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**입력(renameFolderParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 이름을 바꿀 폴더가 있는 회사를 처리합니다. |
| `*`folderHandle`*` | `xsd:string` | 예 | 폴더를 처리합니다. |
| `*`folderName`*` | `xsd:string` | 예 | 새 폴더 이름. |

**출력(renameFolderReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 예 | 이름이 변경된 폴더를 처리합니다. |

## 예제 {#section-98bdd2f88d164f488676e90aba1dc864}

이 코드 샘플은 폴더 이름을 변경합니다.

**요청**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**응답**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```
