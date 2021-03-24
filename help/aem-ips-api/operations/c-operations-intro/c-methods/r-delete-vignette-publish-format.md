---
description: 비네팅 제작 형식을 삭제합니다.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 13%

---


# deleteVignettePublishFormat{#deletevignettepublishformat}

비네팅 제작 형식을 삭제합니다.

## 인증된 사용자 유형 {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-789625ba29df4b5f880914d4c64f77ce}

**입력(deleteVignettePublishFormatParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 비네팅이 속하는 회사의 핸들입니다. |
| `*`vignetteFormatHandle`*` | `xsd:string` | 예 | 삭제할 비네팅 게시 형식의 핸들입니다. |

**출력(deleteVignettePublishFormatParam)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

이 코드 샘플은 해당 핸들에 의해 지정된 비네팅 게시 형식을 삭제합니다.

**요청**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**응답**

없음.
