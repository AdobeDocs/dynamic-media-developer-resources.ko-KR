---
description: 특정 회사에 대한 IPS 설정을 반환합니다.
solution: Experience Manager
title: getCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b9f41405-8a45-416c-acec-ef22c2ee119e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 21%

---

# getCompanySettings{#getcompanysettings}

특정 회사에 대한 IPS 설정을 반환합니다.

구문

## 승인된 사용자 유형 {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e146f479c2744baa8f68be8c8848c97f}

**입력(getCompanySettingsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 설정을 검색할 회사에 대한 핸들입니다. |

**출력(getCompanySettingsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 설정 | `types:CompanySettings` | 예 | 회사 설정. |

## 예제 {#section-191f78995ecf473a95eadf7296204fd7}

이 코드 샘플은 특정 회사에 대한 모든 IPS 설정을 반환합니다.

**요청**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**응답**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```
