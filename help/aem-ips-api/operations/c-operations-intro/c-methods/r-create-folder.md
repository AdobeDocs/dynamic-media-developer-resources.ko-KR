---
description: 폴더를 생성합니다.
seo-description: 폴더를 생성합니다.
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Scene7 Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createFolder{#createfolder}

폴더를 생성합니다.

>[!NOTE]
>
>새 폴더는 회사의 루트를 `/` 나타내는 Images 폴더에 종속됩니다.

구문

## 인증된 사용자 유형 {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>사용자는 상위 폴더에 대한 읽기/쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-c00d8d89cf114886a535056f2a1bf892}

**입력(createFolder)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | The Handle to the company |
| ` *`folderPath`*` | `xsd:string` | 예 | 폴더 및 모든 하위 폴더를 리프 수준으로 검색하는 데 사용되는 루트 폴더. 제외된 경우 회사 루트가 사용됩니다. |

**출력(createFolderParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | 예 | 새 폴더의 핸들입니다. |

## 예제 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

이 샘플 코드는 회사 루트에 폴더를 만듭니다. 응답은 새로 만든 폴더의 핸들을 반환합니다.

**요청**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**응답**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```

