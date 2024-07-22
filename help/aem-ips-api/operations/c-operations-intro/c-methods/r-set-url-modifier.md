---
description: 지정된 에셋에 대한 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 설정합니다. 이러한 명령은 에셋을 삭제하지 않고 해당 에셋의 표현을 수정합니다.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 6%

---

# setUrlModifier{#seturlmodifier}

지정된 에셋에 대한 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 설정합니다. 이러한 명령은 에셋을 삭제하지 않고 해당 에셋의 표현을 수정합니다.

이미지 제공의 경우 `urlModifier` 매개 변수의 명령이 Modifier 카탈로그 필드에 게시되고 요청 URL에 지정된 명령 앞에 적용됩니다. `urlPostApplyModifier`의 명령이 `PostModifier` 카탈로그 필드에 게시되고 요청 URL 또는 `urlModifier`의 모든 명령을 재정의합니다. 이미지 렌더링의 경우 `urlModifier` 및 `urlPostApplyModifier`의 명령이 연결되어 Modifier 카탈로그 필드에 게시됩니다.

## 승인된 사용자 유형 {#section-fefcd732ccf64c78956606538f96c73d}

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
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| assetHandle | `xsd:string` | 예 | 에셋 핸들. |
| urlModifier | `xsd:string` | 아니요 | 요청 또는 `urlPostApplyModifier` 명령에 앞서 적용할 이미지 제공 또는 이미지 렌더링 프로토콜 명령입니다. |
| urlPostApplyModifier | `xsd:string` | 아니요 | `urlModifier` 및 요청 명령 뒤에 적용할 이미지 제공 또는 이미지 렌더링 프로토콜 명령입니다. |

**출력(setUrlModifierReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

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
