---
description: getPhotoshopPath 작업에서 반환된 이미지 위치 좌표입니다.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 19%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

getPhotoshopPath 작업에서 반환된 이미지 위치 좌표입니다.

구문

## 매개 변수 {#section-59792c446366456d90de7f5875bad1b0}

| 이름 | 유형 | 설명 |
|---|---|---|
| x0 | `xsd:double` | 왼쪽 위 x축 좌표입니다. |
| y0 | `xsd:double` | 왼쪽 위 y축 좌표입니다. |
| x1 | `xsd:double` | 오른쪽 위 x축 좌표입니다. |
| y1 | `xsd:double` | 오른쪽 위 y축 좌표입니다. |
| x2 | `xsd:double` | 오른쪽 x축 좌표 아래. |
| y2 | `xsd:double` | 오른쪽 아래 y축 좌표. |
| x3 | `xsd:double` | 왼쪽 x축 좌표계 아래. |
| y3 | `xsd:double` | 왼쪽 아래 y축 좌표. |

## 예 {#section-19ed4409ff3a41c9b52a9c9424612927}

다음 `PerspectiveQuad` 유형은 다음 순서로 데이터를 반환합니다.

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

