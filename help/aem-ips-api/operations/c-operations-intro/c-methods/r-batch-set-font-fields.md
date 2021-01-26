---
description: 글꼴 메타데이터 필드를 설정합니다.
seo-description: 글꼴 메타데이터 필드를 설정합니다.
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
topic: Dynamic Media Image Production System API
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 14%

---


# batchSetFontFields{#batchsetfontfields}

글꼴 메타데이터 필드를 설정합니다.

## 인증된 사용자 유형 {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-836f5948d00a46e98ccb62f0573e4e68}

**입력(batchSetFontFieldsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 글꼴이 포함된 회사를 처리합니다. |
| `*`updateArray`*` | `types:FontFieldUpdateArray` | 예 | 글꼴 필드 업데이트 배열입니다. |

**출력(batchSetFontFieldsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 예 | 글꼴 필드를 성공적으로 설정한 횟수입니다. |
| `*`warningCount`*` | `xsd:int` | 예 | 작업이 글꼴 필드를 설정하려고 할 때 생성된 경고 수입니다. |
| `*`errorCount`*` | `xsd:int` | 예 | 작업이 글꼴 필드를 설정하려고 할 때 발생한 오류 수입니다. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 경고를 생성한 자산과 연결된 세부 사항의 배열입니다. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 아니요 | 작업이 업데이트를 적용하려고 할 때 오류를 생성한 자산과 연결된 세부 사항의 배열입니다. |

## 예제 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**요청**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**응답**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

