---
description: 확대/축소 대상을 만들거나 편집합니다.
seo-description: 확대/축소 대상을 만들거나 편집합니다.
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Scene7 Image Production System API
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 20%

---


# saveZoomTarget{#savezoomtarget}

확대/축소 대상을 만들거나 편집합니다.

구문

## 인증된 사용자 유형 {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-4a23983cae4e49a098e9bbe736933996}

**입력(saveZoomTargetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 저장할 확대/축소 타겟이 있는 회사의 핸들입니다. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 확대/축소 대상에 대한 핸들입니다. |
| ` *`zoomTargetHandle`*` | `xsd:string` | 아니요 | 확대/축소 대상을 편집하거나 만듭니다. |
| ` *`name`*` | `xsd:string` | 예 | 확대/축소 대상 이름. |
| ` *`xPosition`*` | `xsd:int` | 예 | 왼쪽 픽셀 위치. |
| ` *`yPosition`*` | `xsd:int` | 예 | 위쪽 픽셀 위치. |
| ` *`width`*` | `xsd:int` | 예 | 대상 너비를 확대/축소합니다. |
| ` *`height`*` | `xsd:int` | 예 | 대상 높이를 확대/축소합니다. |
| ` *`사용자 데이터`*` | `xsd:string` | 예 | 고객별 정보를 참조하십시오. 모든 유형의 데이터를 포함할 수 있습니다. |

**출력(saveZoomTargetReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`zoomTargetHandle`*` | `xsd:string` | 예 | 새로 만든 확대/축소 타겟을 처리합니다. |

## 예제 {#section-509c472c316549cdb228d7e1cfa8400a}

이 코드 샘플은 확대/축소 대상을 저장합니다. 응답에서 확대/축소 대상 핸들을 반환합니다.

**요청**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**응답**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```

