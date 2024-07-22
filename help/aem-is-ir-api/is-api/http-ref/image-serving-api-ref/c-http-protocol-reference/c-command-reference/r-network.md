---
title: 네트워크
description: 네트워크 대역폭 최적화를 사용하여 실제 네트워크 대역폭을 기반으로 제공되는 이미지 품질을 조정하는 방법에 대해 알아봅니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# 네트워크{#network}

네트워크 대역폭을 켜면 실제 네트워크 대역폭에 따라 제공되는 이미지 품질이 자동으로 조정됩니다. 네트워크 대역폭이 낮은 경우 [DPR(장치 픽셀 비율)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) 최적화는 이미 켜져 있더라도 자동으로 꺼집니다.

원하는 경우 `network=off`을(를) 이미지의 URL에 추가하여 개별 이미지 수준에서 네트워크 대역폭 최적화를 옵트아웃할 수 있습니다.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 설정/해제 </span> </p> </td> 
  <td class="stentry"> <p>네트워크 대역폭이 실제 네트워크 대역폭(켜짐)을 기준으로 제공되는 이미지 품질을 조정할지 또는 이미지 품질 조정이 없는 경우 네트워크 대역폭 최적화가 꺼지는지 여부를 지정합니다.</p> </td> 
 </tr> 
</table>

네트워크 대역폭 값은 번들 CDN의 감지된 클라이언트측 값을 기반으로 합니다.

## 속성

요청 속성입니다. 네트워크 여건이 우수하면 효과가 없다.

## 기본값

`network=off`

## 예

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 참조

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [스마트 이미징](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
