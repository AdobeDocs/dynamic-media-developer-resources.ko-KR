---
description: 확대/축소 대상을 만들거나 편집합니다.
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
TQID: 'https://experienceleague.adobe.com/rw-joRwkyumLI261ifPiWTeIgy4mvx-4MpgmaKcX5-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 19%

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
| company핸들 | `xsd:string` | 예 | 저장할 확대/축소 대상이 있는 회사의 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 확대/축소 대상에 대한 핸들입니다. |
| 확대/축소 대상 핸들 | `xsd:string` | 아니요 | 확대/축소 대상을 편집하거나 만듭니다. |
| name | `xsd:string` | 예 | 확대/축소 대상 이름입니다. |
| x위치 | `xsd:int` | 예 | 왼쪽 픽셀 위치. |
| y위치 | `xsd:int` | 예 | 상단 픽셀 위치. |
| 너비 | `xsd:int` | 예 | 확대/축소 대상 너비. |
| 높이 | `xsd:int` | 예 | 확대/축소 대상 높이. |
| userData | `xsd:string` | 예 | 고객별 정보. 모든 유형의 데이터를 포함할 수 있습니다. |

**출력(saveZoomTargetReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 확대/축소 대상 핸들 | `xsd:string` | 예 | 새로 생성된 확대/축소 대상에 대해 처리합니다. |

## 예제 {#section-509c472c316549cdb228d7e1cfa8400a}

이 코드 샘플은 확대/축소 대상을 저장합니다. 응답은 확대/축소 대상 핸들을 반환합니다.

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

