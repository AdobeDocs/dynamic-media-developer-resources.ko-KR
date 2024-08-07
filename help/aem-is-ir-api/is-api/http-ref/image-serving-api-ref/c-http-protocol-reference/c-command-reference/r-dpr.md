---
title: dpr
description: 장치 픽셀 비율(DPR)&mdash;CSS 픽셀 비율&mdash;은 장치의 실제 픽셀과 논리 픽셀 간의 관계입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 9%

---

# dpr{#dpr}

CSS 픽셀 비율이라고도 하는 디바이스 픽셀 비율(DPR)은 디바이스의 물리적 픽셀과 논리 픽셀 간의 관계입니다. 특히, 망막 스크린의 등장과 함께, 최신 모바일 디바이스의 픽셀 해상도는 빠른 속도로 성장하고 있다.

장치 픽셀 비율 최적화를 활성화하면 화면의 기본 해상도로 이미지가 렌더링되어 선명해집니다.

현재 디스플레이의 픽셀 밀도는 Akamai CDN 헤더 값에서 가져옵니다.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> / </span> </span> </p> </td> 
  <td class="stentry"> <p>개별 이미지 URL 수준에서 DPR 최적화를 해제합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>사용자 지정 값(클라이언트측 논리 또는 기타 수단으로 감지된 값)으로 스마트 이미징에서 감지된 DPR 값을 재정의합니다. DprValue에 대해 허용되는 값은 0보다 큰 수입니다. </p> </td> 
 </tr> 
</table>


회사 수준 DPR 설정이 꺼진 경우에도 `dpr=on,dprValue`을(를) 사용할 수 있습니다.

DPR 최적화로 인해 결과 이미지가 MaxPix Dynamic Media 설정보다 클 경우 이미지의 종횡비를 유지하여 MaxPix 너비를 항상 인식합니다.

| 요청한 이미지 크기 | DPR 값 | 게재된 이미지 크기 |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR 값은 번들 CDN의 감지된 클라이언트측 값을 기반으로 합니다. 이러한 값은 때때로 부정확합니다. 예를 들어, `dpr=2`이(가) 있는 iPhone5와 dpr=3이 있는 iPhone12는 모두 `dpr=2`을(를) 표시합니다. 고해상도 장치의 경우 `dpr=2`을(를) 보내는 것이 `dpr=1`을(를) 보내는 것보다 좋습니다. 그러나 이러한 부정확성을 극복하는 가장 좋은 방법은 클라이언트측 DPR을 사용하여 100% 정확한 값을 제공하는 것입니다. 또한 Apple 또는 출시된 다른 디바이스 등 어떤 디바이스에서도 작동합니다. [클라이언트측 장치 픽셀 비율로 스마트 이미징 사용](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en)을 참조하세요.

## 속성

요청 속성입니다. `dpr`이(가) 꺼져 있거나 `dprValue=1`인 경우 아무런 영향을 주지 않습니다.

## 기본값

`dpr=off`


## 예

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 참조

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [네트워크](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [스마트 이미징](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
