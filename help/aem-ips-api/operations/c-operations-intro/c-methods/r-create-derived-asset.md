---
description: 기존 기본 소스 이미지 자산에서 파생된 새 자산을 만듭니다.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,자산 관리
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

기존 기본 소스 이미지 자산에서 파생된 새 자산을 만듭니다.

구문

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

파생 자산은 소유자 이미지의 표현을 수정하는 이미지 서버 프로토콜 명령을 지정합니다. `AdjustedView` 파생 유형은 간단한 수정 사항을 단일 이미지(예: 자르기 사각형 지정)에 적용하는 데 도움이 되지만, `LayerView`을 사용하면 텍스트 또는 추가 이미지를 포함할 수 있는 다중 레이어 보기를 만들 수 있습니다.

이미지 복사([copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0) 참조)와 달리, 파생된 이미지는 해당 소유자 이미지에 연결됩니다. 소유자 이미지를 변경하면 연결된 파생 자산이 수정됩니다. 소유자 이미지를 삭제하면 연결된 파생 이미지가 모두 삭제됩니다.

## 인증된 사용자 유형 {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-5a0dde01cff6454da3646ea805c2be1e}

**입력(createDerivedAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 새 자산을 파생시킬 자산이 포함된 회사의 핸들입니다. |
| `*`ownerHandle`*` | `xsd:string` | 예 | 새 이미지가 파생되는 기본 이미지 자산에 대한 핸들입니다. |
| `*`folderHandle`*` | `xsd:string` | 예 | 새 파생 자산을 만들 폴더의 핸들입니다. |
| `*`name`*` | `xsd:string` | 예 | 파생된 자산의 이름입니다. |
| `*`type`*` | `xsd:string` | 예 | 새로 파생된 자산의 자산 유형: `AdjustedView` 또는 `LayerView` |
| `*`urlModifier`*` | `xsd:string` | 아니요 | 요청 또는 `urlPostApplyModifier` 명령 전에 *이미지 제공 또는 이미지 렌더링 프로토콜 명령이 적용되었습니다.* |
| `*`urlPostApplyModifier`*` | `xsd:string` | 아니요 | *after* 를 요청 또는 `urlPostApplyModifier` 명령에 적용한 이미지 제공 또는 이미지 렌더링 프로토콜 명령입니다. |

**출력(createDerivedAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 예 | 파생 자산에 대한 핸들입니다. |

## 예제 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

샘플 코드는 조정된 보기와 임의의 값이 있는 `urlModifier` 및 `urlPostApplyModifier` 를 사용하여 파생된 자산을 만듭니다. 응답은 새로 파생된 자산에 대한 핸들을 반환합니다.

**요청**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**응답**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```
