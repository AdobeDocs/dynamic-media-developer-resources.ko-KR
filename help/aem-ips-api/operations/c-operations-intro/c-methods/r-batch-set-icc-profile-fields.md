---
description: ICC 프로필 메타데이터 필드를 설정합니다.
seo-description: ICC 프로필 메타데이터 필드를 설정합니다.
seo-title: batchSetIccProfileFields
solution: Experience Manager
title: batchSetIccProfileFields
topic: Scene7 Image Production System API
uuid: 163b9b36-85b6-4880-8029-8421b04f4a08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 13%

---


# batchSetIccProfileFields{#batchseticcprofilefields}

ICC 프로필 메타데이터 필드를 설정합니다.

구문

## 인증된 사용자 유형 {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**입력(batchSetIccProfileFields)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | ICC 프로파일이 들어 있는 회사를 처리합니다. |
| ` *`업데이트 배열`*` | `xsd:string` | 예 | ICC 프로파일 업데이트 배열. |

**출력(batchSetIccProfileFields)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 예 | ICC 프로필 필드를 성공적으로 설정한 횟수입니다. |
| ` *`warningCount`*` | `xsd:int` | 예 | ICC 프로필 필드를 설정하려고 할 때 생성되는 경고 수입니다. |
| ` *`errorCount`*` | `xsd:int` | 예 | ICC 프로필 필드를 설정하려고 할 때 생성되는 오류 수입니다. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 경고를 생성한 자산과 연결된 세부 사항의 배열입니다. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 오류를 생성한 자산과 연결된 세부 사항의 배열입니다. |

## 예제 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**요청**

```java
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**응답**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```

