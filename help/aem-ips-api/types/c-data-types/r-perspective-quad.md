---
description: getPhotoshopPath 작업에서 반환된 이미지 위치 좌표입니다.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
TQID: 'https://experienceleague.adobe.com/jJYhv5-HhU2t1CyVeRVzmIsprZ3xM4ZQtcMDS-Zgt6I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 7%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

getPhotoshopPath 작업에서 반환된 이미지 위치 좌표입니다.

구문

## 매개 변수 {#section-59792c446366456d90de7f5875bad1b0}

| 이름 | 유형 | 설명 |
|---|---|---|
| x0 | `xsd:double` | 왼쪽 위 x축 좌표. |
| y0 | `xsd:double` | 왼쪽 위 y축 좌표. |
| x1 | `xsd:double` | 오른쪽 위 x축 좌표. |
| y1 | `xsd:double` | 오른쪽 위 y축 좌표. |
| x2 | `xsd:double` | 오른쪽 아래 x축 좌표. |
| y2 | `xsd:double` | 오른쪽 아래 y축 좌표. |
| x3 | `xsd:double` | 왼쪽 아래 X축 좌표. |
| y3 | `xsd:double` | 왼쪽 Y축 아래 좌표. |

## 예 {#section-19ed4409ff3a41c9b52a9c9424612927}

`PerspectiveQuad` 형식은 다음 순서로 데이터를 반환합니다.

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

