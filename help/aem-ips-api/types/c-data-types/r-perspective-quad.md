---
description: getPhotoshopPath 작업에서 반환된 이미지 위치 좌표.
seo-description: getPhotoshopPath 작업에서 반환된 이미지 위치 좌표.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
topic: Scene7 Image Production System API
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# PerspectiveQuad{#perspectivequad}

getPhotoshopPath 작업에서 반환된 이미지 위치 좌표.

구문

## 매개 변수 {#section-59792c446366456d90de7f5875bad1b0}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`x0`*` | `xsd:double` | 왼쪽 위 x축 좌표. |
| ` *`y0`*` | `xsd:double` | 왼쪽 위 y축 좌표입니다. |
| ` *`x1`*` | `xsd:double` | 오른쪽 위 x축 좌표. |
| ` *`y1`*` | `xsd:double` | 오른쪽 위 y축 좌표입니다. |
| ` *`x2`*` | `xsd:double` | 오른쪽 아래 x축 좌표. |
| ` *`y2`*` | `xsd:double` | 오른쪽 아래 y축 좌표. |
| ` *`x3`*` | `xsd:double` | 왼쪽 아래 x축 좌표. |
| ` *`y3`*` | `xsd:double` | 왼쪽 아래 y축 좌표. |

## 예 {#section-19ed4409ff3a41c9b52a9c9424612927}

유형은 다음 순서로 데이터를 반환합니다. `PerspectiveQuad`

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)

