---
description: 에셋 이미지와 연결된 확대/축소 대상을 설정합니다. 기존 확대/축소 대상을 덮어씁니다.
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
TQID: 'https://experienceleague.adobe.com/JQfWp3-Xm1rGlAmd1qisxzo2irZy3aedScXmeBbL1Pk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 12%

---

# setZoomTargets{#setzoomtargets}

에셋 이미지와 연결된 확대/축소 대상을 설정합니다. 기존 확대/축소 대상을 덮어씁니다.

구문

## 승인된 사용자 유형 {#section-c5e1863e9cb1426591bfea513620b6ab}

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
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| assetHandle | `xsd:string` | 예 | 설정하려는 확대/축소 대상이 있는 에셋입니다. |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | 예 | 확대/축소 대상 정의 배열입니다. |

**출력(setZoomTargetsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | 예 | 이 작업으로 생성된 확대/축소 대상에 대한 핸들 집합입니다. |

## 예제 {#section-a2f14c7a1499443e96d099ea8a76c182}

이 코드 샘플은 이름, 위치(x축 및 y축), 너비, 높이별로 확대/축소 대상 배열을 정의하고 배열을 에셋에 할당합니다. 응답에는 새로 생성된 확대/축소 대상에 대한 핸들이 포함됩니다.

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
