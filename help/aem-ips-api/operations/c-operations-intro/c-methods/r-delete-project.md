---
description: 회사에서 프로젝트를 삭제합니다. 자산과 프로젝트 사이의 링크가 끊겼지만 IPS에서 자산이 삭제되지 않습니다.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 9%

---

# deleteProject{#deleteproject}

회사에서 프로젝트를 삭제합니다. 자산과 프로젝트 사이의 링크가 끊겼지만 IPS에서 자산이 삭제되지 않습니다.

구문

## 인증된 사용자 유형 {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-00d1e00dd5014513a52b4e6b4f61de62}

**입력(deleteProjectParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyName | `xsd:string` | 예 | 프로젝트와 연결된 회사의 이름입니다. |
| projectHandle | `xsd:string` | 예 | 삭제할 프로젝트의 핸들입니다. |

**출력(deleteProjectReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-e38507f1f7ec41b9a625f47390490254}

이 코드 샘플은 프로젝트를 삭제하기 위해 IPS 웹 서비스 서버로 전송된 deleteProjectParam의 필드로 회사 핸들 및 프로젝트 핸들을 사용합니다.

**요청**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**응답**

없음.
