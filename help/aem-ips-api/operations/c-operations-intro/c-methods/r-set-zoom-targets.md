---
description: 자산 이미지와 연결된 확대/축소 대상을 설정합니다. 기존 확대/축소 타겟을 덮어씁니다.
seo-description: 자산 이미지와 연결된 확대/축소 대상을 설정합니다. 기존 확대/축소 타겟을 덮어씁니다.
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 12%

---


# setZoomTargets{#setzoomtargets}

자산 이미지와 연결된 확대/축소 대상을 설정합니다. 기존 확대/축소 타겟을 덮어씁니다.

구문

## 인가된 사용자 유형 {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-161f8c733cc4439f94a06e12119d4226}

**입력(setZoomTargetsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 설정할 확대/축소 대상이 있는 에셋. |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | 예 | 확대/축소 대상 정의 배열입니다. |

**출력(setZoomTargetsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | 예 | 이 작업으로 만든 확대/축소 대상에 대한 핸들 세트입니다. |

## 예제 {#section-a2f14c7a1499443e96d099ea8a76c182}

이 코드 샘플은 이름, 위치(x 및 y축), 너비, 높이, 높이로 확대/축소 대상 배열을 정의하고 해당 배열을 자산에 할당합니다. 응답에는 새로 만든 확대/축소 대상에 대한 핸들이 포함됩니다.

**요청**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**응답**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```

