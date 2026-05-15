---
title: style
description: style
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
TQID: 'https://experienceleague.adobe.com/vkV2CfEEhJmPdQg64y0G-5Ep-T6SPd4tQX88CWbPryw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 7%

---

# style{#style}

URL 쿼리 문자열 및 구성에서 다음 명령을 적용할 수 있습니다. URL 쿼리 문자열에 적용된 명령은 항상 config에 있는 동일한 명령보다 우선합니다.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 상대 또는 절대 CSS 위치. </p> <p>사용자 지정 CSS 파일의 위치를 지정합니다. <span class="codeph"><span class="varname"> cssPath</span></span>이(가) 상대적인 경우 뷰어 HTML 페이지 위치와 <span class="codeph"> contentUrl=</span> 매개 변수의 값에 대해 확인됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS 파일 내의 모든 에셋 참조는 호출하는 HTML 페이지의 위치가 아니라 CSS 파일 위치에 대해 확인됩니다.

## 속성 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

선택적.

## 기본값 {#section-79a827f7a3bb4f36b3d72c309155059e}

없음.

## 예제 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
