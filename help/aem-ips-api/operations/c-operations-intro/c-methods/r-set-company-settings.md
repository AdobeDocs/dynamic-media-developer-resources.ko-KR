---
description: 다양한 회사별 구성 값을 설정합니다.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# setCompanySettings{#setcompanysettings}

다양한 회사별 구성 값을 설정합니다.

구문

## 인증된 사용자 유형 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-a472da6c57c74a94a179dda081004888}

**입력(setCompanySettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`overwriteMode`*` | `xsd:string` | 아니요 | 자산 덮어쓰기 모드. |
| `*`keepPublishState`*` | `xsd:boolean` | 아니요 | 자산을 다시 업로드할 때 게시 상태를 유지하려면 `true` 로 설정하십시오. |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | 아니요 | 기본 원본 색상 프로파일로 사용할 Icc 프로필 자산 |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | 아니요 | 기본 표시 색상 프로파일로 사용할 Icc 프로필 자산 |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | 아니요 | IPTC 및 EXIF 메타데이터를 IPS 메타데이터 필드에 매핑하는 데 사용되는 XSL 자산입니다. |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | 아니요 | XMP 메타데이터를 IPS 메타데이터 필드에 매핑하는 데 사용되는 XSL 자산입니다. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | 아니요 | 경고 메시지가 전송되기 전에 사용 가능한 최소 디스크 공간(KB)입니다. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | 아니요 | 자산이 휴지통에서 비워질 때마다 회사 관리자에게 알림을 보내려면 `true`으로 설정하십시오. |

**출력(setCompanySettingsReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

이 코드 샘플은 회사의 구성을 설정합니다.

**요청**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**응답**

없음.
