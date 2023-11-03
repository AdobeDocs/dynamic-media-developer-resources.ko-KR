---
description: 폴더 경로에서 시작하여 모든 폴더 및 하위 폴더를 반환합니다. getFolders 응답은 최대 100,000개의 폴더를 반환합니다.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 8%

---

# getFolders{#getfolders}

폴더 경로에서 시작하여 모든 폴더 및 하위 폴더를 반환합니다. getFolders 응답은 최대 100,000개의 폴더를 반환합니다.

## 폴더 용도 {#section-66e344d5333f42f1b060a0cba25935c3}

폴더를 사용하면 하위 폴더와 에셋을 구성할 수 있습니다. 모든 폴더 및 자산 이름은 고유해야 합니다. 동일한 이름을 공유하는 폴더 및 자산은 서로 다른 폴더 계층 구조에 있더라도 네임스페이스 충돌을 일으킵니다.
구문

## 승인된 사용자 유형 {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 폴더에 대한 데이터를 반환하려면 폴더에 대한 읽기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-0c1976503eaa418a9226b51667901176}

**입력(getFoldersParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 손잡이. |
| accessUser핸들 | `xsd:string` | 아니요 | 관리자가 특정 사용자를 가장하는 데 사용됩니다. |
| 액세스 그룹 핸들 | `xsd:string` | 아니요 | 특정 그룹으로 필터링합니다. |
| folderPath | `xsd:string` | 아니요 | 폴더 및 모든 하위 폴더를 리프 수준으로 검색할 루트 폴더입니다. 제외되는 경우 회사 루트가 사용됩니다. |
| assetTypeArray | `types:StringArray` | 아니요 | 지정된 자산 유형만 포함하는 폴더를 반환합니다. |
| responseFieldArray | `types:StringArray` | 아니요 | 응답에 포함할 필드 목록을 포함합니다. |
| exclude필드 배열 | `types:StringArray` | 아니요 | 응답에서 제외할 필드 목록을 포함합니다. |

**출력(getFoldersReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| folderArray | `types:FolderArray` | 아니요 | 필터 조건과 일치하는 폴더의 배열입니다. 응답은 최대 100,000개의 폴더로 제한됩니다. |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## 예제 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

이 코드 샘플은 각 폴더에 대한 특정 정보와 함께 회사의 모든 폴더가 포함된 배열을 반환합니다.

**요청**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**응답**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```
