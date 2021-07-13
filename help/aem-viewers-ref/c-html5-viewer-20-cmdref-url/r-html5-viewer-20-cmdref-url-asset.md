---
description: 모든 뷰어에 공통되는 매개 변수.
solution: Experience Manager
title: asset
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 2%

---

# 자산{#asset}

모든 뷰어에 공통되는 매개 변수.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId  </span> </span> </p> </td> 
   <td colname="col2"> <p> 단일 비디오 또는 응용 비디오 세트의 자산 ID입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

이 속성은 `video` 매개 변수를 사용하지 않는 한 필수입니다. Video 아래의 [외부 비디오 지원](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) 또는 Video360에서 [외부 비디오 지원](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760)을 참조하십시오.

또는

` asset= *`이미지`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이미지  </span> </span> </p> </td> 
   <td colname="col2"> <p> 단일 이미지 또는 회전 메뉴 세트를 지정합니다. 이미지 이름 또는 회전 메뉴 세트 이름에 있는 안전하지 않은 모든 문자에 이중 HTTP 인코딩을 적용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

또는

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListimageListWithModifiersmultiDimensionalSpinSetmodifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이미지  </span> </span> </p> </td> 
   <td colname="col2"> <p> 단일 이미지를 지정합니다. 이미지 이름에 있는 안전하지 않은 모든 문자에 이중 HTTP 인코딩을 적용합니다. </p> <p>또는 이미지 세트에 대한 참조를 지정합니다. 뷰어는 <span class="codeph"> req=set IS </span> 요청을 사용하여 서버에서 이미지 세트를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList  </span> </span> </p> </td> 
   <td colname="col2"> <p> 쉼표로 구분된 항목 또는 프레임의 정렬된 시퀀스로 구성된 명시적 이미지 집합을 지정합니다. </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers  </span> </span> </p> </td> 
   <td colname="col2"> <p> 각 프레임에 자체 이미지 제공 한정자가 있는 명시적 이미지 세트를 지정합니다. 이 경우 프레임 목록은 괄호 안에 래핑됩니다. 프레임 특정 이미지 제공 수정자에 있는 쉼표에 이중 HTTP 인코딩을 적용해야 합니다. </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet  </span> </span> </p> </td> 
   <td colname="col2"> <p>다음 구문을 사용하여 명시적 다차원 스핀 세트를 지정합니다. </p> <p> <span class="codeph"> ((  <span class="varname"> horizontalSpinSet  </span>)[,(  <span class="varname"> horizontalSpinSet  </span>)])  </span> </p> <p> 여기서 <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>은 지정된 가로 축에 대해 쉼표로 구분된 프레임 목록입니다. 모든 <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span>의 프레임 수는 같아야 합니다. </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 수정자  </span> </span> </p> </td> 
   <td colname="col2"> <p> 이미지 제공 명령 <span class="codeph"> 및 </span> 및 <span class="codeph"> = </span> 구분자는 각각 <span class="codeph"> %26 </span> 및 <span class="codeph"> %3D </span>로 HTTP로 인코딩되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

또는

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetvideowatchIdimageswatchIdsetIdswatchIdVIDEOSWATCHIDIMAGESWATCHIdSETIdSWATCHIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet  </span> </span> </p> </td> 
   <td colname="col2"> <p> 미디어 세트에 대한 참조를 지정합니다. 뷰어는 req=set IS 요청을 사용하여 서버에서 미디어 세트를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 비디오  </span> </span> </p> </td> 
   <td colname="col2"> <p> 단일 비디오 또는 응용 비디오 세트. </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이미지  </span> </span> </p> </td> 
   <td colname="col2"> <p> 단일 이미지. </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId  </span> </span> </p> </td> 
   <td colname="col2"> <p> 견본 집합입니다. </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId  </span> </span> </p> </td> 
   <td colname="col2"> <p>견본 이미지입니다. </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID  </span> </span> </p> </td> 
   <td colname="col2"> <p> 미디어 집합 항목 유형 식별자는 다음 중 하나일 수 있습니다. </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image  </span> </p> <p>단일 이미지입니다. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_watchset  </span> </p> <p>중첩 견본 집합입니다. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> 회전  </span> </p> <p>스핀 세트 </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> 비디오  </span> </p> <p>단일 비디오용. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set  </span> </p> <p>응용 비디오 세트용. </p> </li> 
     </ul> </p> <p> <p>참고:  이 기능은 Adobe Dynamic Media Classic에서 지원됩니다. Adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 수정자  </span> </span> </p> </td> 
   <td colname="col2"> <p> 이미지 제공 명령 <span class="codeph"> 및 </span> 및 <span class="codeph"> = </span> 구분자는 각각 <span class="codeph"> %26 </span> 및 <span class="codeph"> %3D </span>로 HTTP로 인코딩되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 콘텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

필수.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

없음.

## 예제 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

단일 자산 참조:

```
asset=Scene7SharedAssets/Backpack_B
```

또는

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

또는

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

또는

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

또는

```
asset=Viewers/space_station_360-AVS
```

카탈로그에 정의된 이미지 세트에 대한 단일 참조:

```
asset=Viewers/Pluralist
```

명시적 이미지 세트:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

프레임별 이미지 제공 한정자를 사용한 명시적 이미지 세트:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

카탈로그에 정의된 스핀 세트에 대한 단일 참조:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

명시적 스핀 세트:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

명시적 다차원 스핀 세트:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

단일 혼합 미디어 집합 참조:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

명시적 혼합 미디어 집합:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

선명하게 하기 수정자가 세트의 모든 이미지에 추가되었습니다.

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```
