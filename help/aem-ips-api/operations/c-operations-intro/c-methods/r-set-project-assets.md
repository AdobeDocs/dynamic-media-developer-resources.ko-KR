---
description: 프로젝트에서 에셋을 할당하거나 업데이트합니다.
seo-description: 프로젝트에서 에셋을 할당하거나 업데이트합니다.
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
feature: Dynamic Media Classic,SDK/API,자산 관리
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 17%

---


# setProjectAssets{#setprojectassets}

프로젝트에서 에셋을 할당하거나 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**입력(setProjectAssetsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`projectHandle`*` | `xsd:string` | 예 | 프로젝트 핸들. |
| `*`assetHandleArray`*` | `types:HandleArray` | 예 | 프로젝트와 연결할 자산 핸들 배열입니다. |

**출력(setProjectAssetsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 예 | 성공적으로 추가된 자산의 수입니다. |

## 예제 {#section-33c1a909c3dc4aa98da474c23a036596}

이 코드 샘플은 프로젝트에 에셋을 할당합니다. 요청은 성공 카운트를 1로 반환합니다.

**요청**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**응답**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

