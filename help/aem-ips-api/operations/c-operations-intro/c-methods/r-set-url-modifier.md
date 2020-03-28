---
description: 지정된 자산에 대한 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 설정합니다. 이러한 명령은 자산을 삭제하지 않고 자산의 표현을 수정합니다.
seo-description: 지정된 자산에 대한 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 설정합니다. 이러한 명령은 자산을 삭제하지 않고 자산의 표현을 수정합니다.
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

지정된 자산에 대한 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 설정합니다. 이러한 명령은 자산을 삭제하지 않고 자산의 표현을 수정합니다.

이미지 제공의 경우 매개 변수의 명령은 `urlModifier` 수정자 카탈로그 필드에 게시되고 요청 URL에 지정된 모든 명령 앞에 적용됩니다. 의 `urlPostApplyModifier` 명령은 `PostModifier` 카탈로그 필드에 게시되며 요청 URL 또는 에 있는 모든 명령을 무시합니다 `urlModifier`. 이미지 렌더링의 경우 의 명령을 `urlModifier` 연결하고 수정자 카탈로그 필드에 `urlPostApplyModifier` 게시합니다.

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 핸들 |
| ` *`assetHandle`*` | `xsd:string` | 예 | 자산 핸들. |
| ` *`urlModifier`*` | `xsd:string` | 아니요 | 이미지 제공 또는 이미지 렌더링 프로토콜 명령을 사용하여 요청이나 `urlPostApplyModifier` 명령 전에 적용할 수 있습니다. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | 아니요 | Image Serving or Image Rendering protocol command to apply after `urlModifier` and request commands. |

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
