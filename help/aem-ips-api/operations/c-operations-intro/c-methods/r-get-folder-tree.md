---
description: 계층 트리 구조의 폴더 및 하위 폴더를 반환합니다. getFolderTree 응답은 최대 100,000개의 폴더로 제한됩니다
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 9%

---

# getFolderTree{#getfoldertree}

계층 트리 구조의 폴더 및 하위 폴더를 반환합니다. getFolderTree 응답은 최대 100,000개의 폴더로 제한됩니다

구문

## 인증된 사용자 유형 {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>폴더에 대한 데이터를 반환하려면 폴더에 대한 읽기 권한이 있어야 합니다.

## 매개 변수 {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**입력(getFolderTreeParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 회사의 손잡이입니다. |
| accessUserHandle | `xsd:string` | 아니요 | 특정 사용자를 가장하기 위해 관리자만 사용합니다. |
| accessGroupHandle | `xsd:string` | 아니요 | 회사가 속한 그룹을 포함하여 특정 그룹으로 필터링하는 데 사용됩니다. |
| folderPath | `xsd:string` | 아니요 | 폴더 및 모든 하위 폴더를 리프 수준으로 검색하는 루트 폴더입니다. 제외된 경우 회사 루트가 사용됩니다. |
| 깊이 | `xsd:int` | 예 | 값이 0이면 최상위 폴더가 설정됩니다. 다른 값은 트리로 내려갈 깊이를 지정합니다. |
| assetTypeArray | `types:StringArray` | 아니요 | 지정된 자산 유형만 포함하는 폴더를 반환합니다. |
| responseFieldArray | `types:StringArray` | 아니요 | 응답에 포함할 필드 목록을 포함합니다. |
| excludeFieldArray | `types:StringArray` | 아니요 | 응답에서 제외할 필드 목록을 포함합니다. |

**출력(getFolderTreeReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 폴더 | `types:folders` | 아니요 | 트리 구조의 폴더 계층 구조입니다. 응답은 최대 100,000개의 폴더로 제한됩니다. |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## 예제 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

이 코드 샘플은 회사 핸들과 깊이 매개 변수를 사용하여 응답이 반환해야 하는 깊이의 수준을 결정합니다. 이 응답에는 관련된 폴더 및 하위 폴더 배열이 포함되어 있습니다. 폴더 트리로 깊이 탐색하려면 깊이 값을 더 작은 수로 설정합니다.

**요청**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**응답**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```
