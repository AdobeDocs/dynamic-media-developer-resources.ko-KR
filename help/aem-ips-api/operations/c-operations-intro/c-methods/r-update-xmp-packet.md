---
description: 자산에 대한 XMP 메타데이터 패킷을 설정하거나 업데이트합니다.
seo-description: 자산에 대한 XMP 메타데이터 패킷을 설정하거나 업데이트합니다.
seo-title: updateXMPPacket
solution: Experience Manager
title: updateXMPPacket
topic: Scene7 Image Production System API
uuid: 97a40261-8f85-4e8c-8aa5-ed4fec297f33
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 22%

---


# updateXMPPacket{#updatexmppacket}

자산에 대한 XMP 메타데이터 패킷을 설정하거나 업데이트합니다.

구문

## 인증된 사용자 유형 {#section-ee88a759f4774482a4734201a971f610}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalcontribUser`

## 매개 변수 {#section-7a89621d441840faba639746b410a489}

**입력(updateXMPPacketParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 자산 핸들. |
| ` *`compressedPacket`*` | `xsd:Base 64 binary` | 예 | [!DNL zlib-compressed] 설정하거나 업데이트할 XMP 패킷입니다. |

**출력(updateXMPPacketReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`성공`*` | `xsd:boolean` | 예 | 패킷이 업데이트된 경우 `true`을 반환합니다. |

## 예제 {#section-38b556b94e5044bf97a954519ff6c212}

**요청**

```java
<ns:updateXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
   <ns:compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg
+955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/LrQ5KcAxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzAQZkunymD8cvs5
lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC41IjNF1YlksGV2v2
6mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFglldKO+bn/ZpqrFv+xsS519WKO1mX9yyoHppveRXrgWTlxX9qJk0ojHG9eaBP3PtKnNaNRNJkq6lN
C8bO5sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh3LPyoIWfgNKX1Vz4i
8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7tx+8xdjuhqNPERMBaoBAAA=</ns:compressedPacket>
</ns:updateXMPPacketParam>
```

**응답**

```java
<updateXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <success>true</success>
</updateXMPPacketReturn>
```

