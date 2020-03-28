---
description: 다양한 회사별 구성 값을 설정합니다.
seo-description: 다양한 회사별 구성 값을 설정합니다.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Scene7 Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 핸들 |
| ` *`overwriteMode`*` | `xsd:string` | 아니요 | 에셋 덮어쓰기 모드. |
| ` *`retain 파섹`*` | `xsd:boolean` | 아니요 | 자산을 다시 업로드할 때 게시 상태를 `true` 유지하도록 설정합니다. |
| ` *`defaultSourceProfileHandle`*` | `xsd:string` | 아니요 | 기본 소스 색상 프로파일로 사용할 IccProfile 자산 |
| ` *`defaultDisplayProfileHandle`*` | `xsd:string` | 아니요 | 기본 표시 색상 프로파일로 사용할 IccProfile 자산 |
| ` *`iptcExif 파섹`*` | `xsd:string` | 아니요 | IPTC 및 EXIF 메타데이터를 IPS 메타데이터 필드에 매핑하는 데 사용되는 XSL 에셋입니다. |
| ` *`xmpMappingXsltHandle`*` | `xsd:string` | 아니요 | XMP 메타데이터를 IPS 메타데이터 필드에 매핑하는 데 사용되는 XSL 에셋입니다. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | 아니요 | 경고 메시지가 전송되기 전에 사용할 수 있는 최소 여유 디스크 공간(KB)입니다. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | 아니요 | 자산을 휴지통에서 비울 때마다 회사 관리자에게 알림을 보내도록 `true` 설정합니다. |

**출력(setCompanySettingsReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

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
