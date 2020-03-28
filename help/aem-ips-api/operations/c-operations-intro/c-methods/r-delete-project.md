---
description: 회사에서 프로젝트를 삭제합니다. 자산과 프로젝트 간의 링크가 끊겼지만, 자산은 IPS에서 삭제되지 않습니다.
seo-description: 회사에서 프로젝트를 삭제합니다. 자산과 프로젝트 간의 링크가 끊겼지만, 자산은 IPS에서 삭제되지 않습니다.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
topic: Scene7 Image Production System API
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteProject{#deleteproject}

회사에서 프로젝트를 삭제합니다. 자산과 프로젝트 간의 링크가 끊겼지만, 자산은 IPS에서 삭제되지 않습니다.

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
| ` *`companyName`*` | `xsd:string` | 예 | 프로젝트와 연결된 회사의 이름입니다. |
| ` *`projectHandle`*` | `xsd:string` | 예 | 삭제할 프로젝트의 핸들입니다. |

**출력(deleteProjectReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-e38507f1f7ec41b9a625f47390490254}

이 코드 샘플에서는 프로젝트를 삭제하기 위해 IPS 웹 서비스 서버로 보낸 deleteProjectParam의 필드 및 회사 핸들을 사용합니다.

**요청**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**응답**

없음.
