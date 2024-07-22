---
description: ICC 프로필 메타데이터 필드를 설정합니다.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 13%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

ICC 프로필 메타데이터 필드를 설정합니다.

구문

## 승인된 사용자 유형 {#section-f6f7caf9434b4f469518dab64b76c0f4}

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
| company핸들 | `xsd:string` | 예 | ICC 프로파일이 포함된 회사를 처리합니다. |
| 배열 업데이트 | `xsd:string` | 예 | ICC 프로필 업데이트 배열. |

**출력(batchSetIccProfileFields)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| successCount | `xsd:int` | 예 | 성공적으로 설정된 ICC 프로파일 필드의 수입니다. |
| warningCount | `xsd:int` | 예 | 작업에서 ICC 프로파일 필드를 설정하려고 할 때 생성된 경고 수입니다. |
| errorCount | `xsd:int` | 예 | 작업에서 ICC 프로파일 필드를 설정하려고 할 때 생성된 오류 수. |
| warningDetailArray | `types:AssetOperationFaultArray` | 아니요 | 작업에서 업데이트를 적용하려고 할 때 경고를 생성한 자산과 관련된 세부 정보의 배열입니다. |
| errorDetailArray | `types:AssetOperationFaultArray` | 아니요 | 작업에서 업데이트를 적용하려고 할 때 오류가 발생한 자산과 관련된 세부 정보의 배열입니다. |

## 예제 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**요청**

```java {.line-numbers}
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

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
