---
description: 회사의 구조(파일 수 등)에 대한 정보를 반환합니다.
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 13%

---

# getDiskUsage{#getdiskusage}

회사의 구조(파일 수 등)에 대한 정보를 반환합니다.

## 인증된 사용자 유형 {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**입력(getDiskUsageParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 디스크 사용을 가져오려는 회사의 핸들입니다. |

**출력(getDiskUsageReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | 예 | 회사 디스크 사용 배열입니다. |

## 예제 {#section-cb16a97badc94076ad5da277db5ed16a}

이 요청의 이름이 오해의 소지가 있습니다. 회사에서 사용 중인 디스크 공간의 양을 반영하는 스칼라 값만 반환하는 대신 회사 구조에 대한 다른 정보도 가져옵니다.

**요청**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**응답**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```
