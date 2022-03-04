---
description: 지정된 자산에 대한 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 설정합니다. 이러한 명령은 자산의 표현을 삭제하지 않고 수정합니다.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

지정된 자산에 대한 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 설정합니다. 이러한 명령은 자산의 표현을 삭제하지 않고 수정합니다.

이미지 제공 작업의 경우 `urlModifier` 매개 변수는 수정자 카탈로그 필드에 게시되고 요청 URL에 지정된 모든 명령 앞에 적용됩니다. 의 명령 `urlPostApplyModifier` 에 게시됨 `PostModifier` 카탈로그 필드를 작성하고 요청 URL이나 `urlModifier`. 이미지 렌더링의 경우 `urlModifier` 및 `urlPostApplyModifier` 수정자 카탈로그 필드에 연결 및 게시됩니다.

## 인증된 사용자 유형 {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**입력(setUrlModifierParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`assetHandle`*` | `xsd:string` | 예 | 자산 핸들. |
| `*`urlModifier`*` | `xsd:string` | 아니요 | 요청이나 요청 전에 적용할 이미지 제공 또는 이미지 렌더링 프로토콜 명령 `urlPostApplyModifier` 명령. |
| `*`urlPostApplyModifier`*` | `xsd:string` | 아니요 | 다음에 적용할 이미지 제공 또는 이미지 렌더링 프로토콜 명령 `urlModifier` 및 요청 명령 |

**출력(setUrlModifierReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-801d4b9b986443f59a5783a3d6bf44aa}

**요청**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**응답**

없음.
