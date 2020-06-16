---
description: 기존 기본 소스 이미지 자산에서 파생된 새 자산을 만듭니다.
seo-description: 기존 기본 소스 이미지 자산에서 파생된 새 자산을 만듭니다.
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
topic: Scene7 Image Production System API
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 8%

---


# createDerivedAsset{#createderivedasset}

기존 기본 소스 이미지 자산에서 파생된 새 자산을 만듭니다.

구문

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

파생 자산은 소유자 이미지의 표현을 수정하는 이미지 서버 프로토콜 명령을 지정합니다. 파생된 유형은 단일 이미지(예: 자르기 사각형 지정)에 간단한 수정 사항을 적용하는 데 도움이 되지만, 이 유형은 텍스트 또는 추가 이미지를 포함할 수 있는 다중 레이어 보기를 만드는 데 `AdjustedView` `LayerView` 도움이 됩니다.

이미지 복사본과 달리( [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)참조) 파생된 이미지는 소유자 이미지에 연결됩니다. 소유자 이미지를 변경하면 관련 파생 자산이 수정됩니다. 소유자 이미지를 삭제하면 연결된 파생 이미지가 삭제됩니다.

## 공인 사용자 유형 {#authorized-user-types}

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 새 자산을 파생할 자산이 들어 있는 회사의 핸들 |
| ` *`ownerHandle`*` | `xsd:string` | 예 | 새 이미지가 파생되는 기본 이미지 자산의 핸들입니다. |
| ` *`folderHandle`*` | `xsd:string` | 예 | 새 파생 자산을 만들 폴더의 핸들 |
| ` *`name`*` | `xsd:string` | 예 | 파생된 자산의 이름입니다. |
| ` *`type`*` | `xsd:string` | 예 | 파생된 새 자산의 자산 유형: `AdjustedView` 또는 `LayerView`. |
| ` *`urlModifier`*` | `xsd:string` | 아니요 | 요청이나 명령 *전에* 적용된 이미지 제공 또는 이미지 렌더링 프로토콜 `urlPostApplyModifier` 명령 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | 아니요 | 요청이나 명령 *이후에* 적용되는 이미지 제공 또는 이미지 렌더링 프로토콜 `urlPostApplyModifier` 명령 |

**출력(createDerivedAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 예 | 파생 자산의 핸들입니다. |

## 예제 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

샘플 코드는 조정된 보기와 임의의 값이 있는 파생 자산을 `urlModifier` 만듭니다 `urlPostApplyModifier` . 응답은 새로 파생된 자산의 핸들을 반환합니다.

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

