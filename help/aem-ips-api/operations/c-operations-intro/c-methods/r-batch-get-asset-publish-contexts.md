---
description: 게시용으로 표시된 에셋의 게시 컨텍스트를 반환합니다.
solution: Experience Manager
title: batchGetAssetPublishContext
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 14%

---

# batchGetAssetPublishContext{#batchgetassetpublishcontexts}

게시용으로 표시된 에셋의 게시 컨텍스트를 반환합니다.

구문

## 승인된 사용자 유형 {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

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
>* 에셋을 반환하려면 사용자에게 읽기 권한이 있어야 합니다.
>* 모든 사용자는 공유 회사에 액세스할 수 있습니다.
>

## 매개 변수 {#section-1742fcb196224545b270eb8241f757a8}

**입력(batchGetAssetPublishContextsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사를 위해 처리하십시오. |
| assetHandleArray | ` `유형:HandleArray&quot; | 예 | 활성(게시용으로 표시) 컨텍스트에 대해 쿼리할 자산 목록입니다. |

**출력(batchGetAssetPublishContextsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | 예 | 각 자산이 게시용으로 표시된 게시 컨텍스트 배열입니다. |

## 예제 {#section-457f6809ccfa425b9a0976313d613f4e}

**요청**

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**응답**

```java {.line-numbers}
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```
