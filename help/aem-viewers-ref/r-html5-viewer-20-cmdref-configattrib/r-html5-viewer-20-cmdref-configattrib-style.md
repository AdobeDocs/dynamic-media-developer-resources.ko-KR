---
description: style
solution: Experience Manager
title: style
feature: Dynamic Media Classic,뷰어,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 7%

---


# style{#style}

URL 쿼리 문자열과 구성에서 다음 명령을 모두 적용할 수 있습니다. URL 쿼리 문자열에 적용된 명령은 항상 구성에 있는 동일한 명령보다 우선합니다.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 상대 또는 절대 CSS 위치. </p> <p>사용자 지정 CSS 파일의 위치를 지정합니다. <span class="codeph"><span class="varname"> cssPath</span></span>가 상대적인 경우 뷰어 HTML 페이지 위치 및 <span class="codeph"> contentUrl=</span> 매개 변수의 값을 기준으로 결정됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS 파일 내의 모든 에셋 참조는 호출된 HTML 페이지의 위치가 아니라 CSS 파일 위치에 대해 확인됩니다.

## 속성 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

선택 사항입니다.

## 기본값 {#section-79a827f7a3bb4f36b3d72c309155059e}

없음.

## 예제 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
