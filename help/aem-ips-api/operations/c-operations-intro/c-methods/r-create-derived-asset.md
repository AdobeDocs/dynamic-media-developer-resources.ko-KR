---
description: 기존 기본 소스 이미지 에셋에서 파생된 새 에셋을 만듭니다.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

기존 기본 소스 이미지 에셋에서 파생된 새 에셋을 만듭니다.

구문

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

파생된 자산은 소유자 이미지의 표현을 수정하는 이미지 서버 프로토콜 명령을 지정합니다. 다음 `AdjustedView` 파생 형식은 단일 이미지에 간단한 수정 사항을 적용하는 데 도움이 됩니다(예: 자르기 사각형을 지정). `LayerView` 텍스트 또는 추가 이미지를 포함할 수 있는 다중 계층 보기를 생성하는 데 도움이 됩니다.

이미지 사본과 달리(참조) [이미지 복사](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0))에서 파생된 이미지는 소유자 이미지에 연결됩니다. 소유자 이미지를 변경하면 연결된 파생된 자산이 수정됩니다. 소유자 이미지를 삭제하면 연결된 모든 파생 이미지가 삭제됩니다.

## 승인된 사용자 유형 {#authorized-user-types}

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
| company핸들 | `xsd:string` | 예 | 새 자산을 파생할 자산을 포함하는 회사에 대한 핸들입니다. |
| owner핸들 | `xsd:string` | 예 | 새 이미지가 파생된 기본 이미지 에셋에 대한 핸들입니다. |
| folder핸들 | `xsd:string` | 예 | 파생된 새 에셋이 생성되는 폴더에 대한 핸들입니다. |
| name | `xsd:string` | 예 | 파생된 에셋의 이름입니다. |
| 유형 | `xsd:string` | 예 | 새로 파생된 에셋의 에셋 유형: `AdjustedView` 또는 `LayerView`. |
| urlModifier | `xsd:string` | 아니요 | 이미지 제공 또는 이미지 렌더링 프로토콜 명령 적용됨 *다음 이전* 요청 또는 `urlPostApplyModifier` 명령입니다. |
| urlPostApplyModifier | `xsd:string` | 아니요 | 이미지 제공 또는 이미지 렌더링 프로토콜 명령 적용됨 *이후* 또는 요청에 `urlPostApplyModifier` 명령입니다. |

**출력(createDerivedAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetHandle | `xsd:string` | 예 | 파생된 자산에 대한 핸들입니다. |

## 예제 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

샘플 코드는 조정된 보기 및 를 사용하여 파생된 자산을 만듭니다. `urlModifier` 및 `urlPostApplyModifier` 임의 값 포함. 응답은 새로 파생된 자산에 대한 핸들을 반환합니다.

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
