---
title: 네트워크
description: 네트워크 대역폭 최적화를 사용하여 실제 네트워크 대역폭을 기반으로 제공되는 이미지 품질을 조정하는 방법에 대해 알아봅니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 2%

---

# 네트워크{#network}

네트워크 대역폭을 켜면 실제 네트워크 대역폭에 따라 제공되는 이미지 품질이 자동으로 조정됩니다. 네트워크 대역폭이 낮은 경우 [DPR(장치 픽셀 비율)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) 최적화는 이미 설정되어 있더라도 자동으로 해제됩니다.

원할 경우 을 추가하여 개별 이미지 수준에서 네트워크 대역폭 최적화를 옵트아웃할 수 있습니다 `network=off` 이미지의 URL에 매핑합니다.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 켜기|끄기 </span> </p> </td> 
  <td class="stentry"> <p>네트워크 대역폭이 실제 네트워크 대역폭(켜짐)을 기준으로 제공되는 이미지 품질을 조정할지 또는 이미지 품질 조정이 없는 경우 네트워크 대역폭 최적화가 꺼지는지 여부를 지정합니다.</p> </td> 
 </tr> 
</table>

DPR 및 네트워크 대역폭 값은 번들 CDN의 감지된 클라이언트측 값을 기반으로 합니다. 이러한 값은 때때로 부정확합니다. 예: iPhone5 `dpr=2`, 및 iPhone12 `dpr=3`, 모두 표시 `dpr=2`. 고해상도 장치의 경우 `dpr=2` 는 dpr=1을 보내는 것보다 낫습니다. 그러나 이러한 부정확성을 극복하는 가장 좋은 방법은 클라이언트측 DPR을 사용하여 100% 정확한 값을 제공하는 것입니다. 또한 Apple 또는 출시된 다른 디바이스 등 어떤 디바이스에서도 작동합니다. 다음을 참조하십시오 [클라이언트측 장치 픽셀 비율이 있는 스마트 이미징 사용](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## 속성



## 기본값

`network=off`

## 예

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 참조

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [스마트 이미징](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)