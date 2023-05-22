---
description: 다양한 회사별 구성 값을 설정합니다.
solution: Experience Manager
title: 회사 설정 설정 설정
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 12%

---

# 회사 설정 설정 설정{#setcompanysettings}

다양한 회사별 구성 값을 설정합니다.

구문

## 승인된 사용자 유형 {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-a472da6c57c74a94a179dda081004888}

**입력(setCompanySettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| overwriteMode | `xsd:string` | 아니요 | 에셋 덮어쓰기 모드. |
| retainPublishState | `xsd:boolean` | 아니요 | 다음으로 설정 `true` 에셋을 다시 업로드할 때 게시 상태를 유지합니다. |
| defaultSourceProfile핸들 | `xsd:string` | 아니요 | 기본 소스 색상 프로파일로 사용할 IccProfile 에셋. |
| defaultDisplayProfile핸들 | `xsd:string` | 아니요 | 기본 표시 색상 프로파일로 사용할 IccProfile 에셋. |
| iptcExifMappingXsltHandle | `xsd:string` | 아니요 | IPTC 및 EXIF 메타데이터를 IPS 메타데이터 필드에 매핑하는 데 사용되는 XSL 에셋입니다. |
| xmpMappingXsltHandle | `xsd:string` | 아니요 | XMP 메타데이터를 IPS 메타데이터 필드에 매핑하는 데 사용되는 XSL 자산입니다. |
| diskSpaceWarningMin | `xsd:int` | 아니요 | 경고 메시지가 전송되기 전에 사용 가능한 최소 디스크 공간(KB)입니다. |
| emailTrashCleanupWarning | `xsd:boolean` | 아니요 | 다음으로 설정 `true` 휴지통에서 자산이 비워질 때마다 회사 관리자에게 알림을 보냅니다. |

**출력(setCompanySettingsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

이 코드 샘플은 회사 구성을 설정합니다.

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
