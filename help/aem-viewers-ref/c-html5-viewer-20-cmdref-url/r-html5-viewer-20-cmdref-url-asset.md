---
description: 모든 뷰어에 공통으로 사용되는 매개 변수입니다.
seo-description: 모든 뷰어에 공통으로 사용되는 매개 변수입니다.
seo-title: asset
solution: Experience Manager
title: asset
topic: Dynamic media
uuid: 6a72257f-d204-4258-b6f8-de6f7b00fd54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# asset{#asset}

모든 뷰어에 공통으로 사용되는 매개 변수입니다.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자산 <span class="varname"> ID </span></span> </p> </td> 
   <td colname="col2"> <p> 단일 비디오 또는 응용 비디오 세트의 자산 ID입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

매개 변수를 사용하지 않는 한 이 속성은 `video` 필요합니다. 비디오 [360에서 비디오](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) 또는 [외부 비디오 지원의](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) 외부 비디오 지원을 참조하십시오.

또는

` asset= *`이미지`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이미지 </span></span> </p> </td> 
   <td colname="col2"> <p> 단일 이미지 또는 회전판 세트를 지정합니다. 이미지 이름이나 회전판 세트 이름에 존재하는 안전하지 않은 모든 문자에 이중 HTTP 인코딩을 적용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

또는

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListimageListWithModifiersmultiDimensionsSpinSetmodifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이미지 </span></span> </p> </td> 
   <td colname="col2"> <p> 단일 이미지를 지정합니다. 이미지 이름에 있는 안전하지 않은 모든 문자에 이중 HTTP 인코딩을 적용합니다. </p> <p>또는 이미지 세트에 대한 참조를 지정합니다. 뷰어는 req=set IS <span class="codeph"> </span> 요청을 사용하여 서버에서 이미지 세트를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 이미지 <span class="varname"> 목록 </span></span> </p> </td> 
   <td colname="col2"> <p> 항목 또는 프레임의 정렬된 시퀀스로 구성된 명확한 이미지 집합을 쉼표로 구분하여 지정합니다. </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageListWithModifiers <span class="varname"> </span></span> </p> </td> 
   <td colname="col2"> <p> 각 프레임에 자체 이미지 제공 수정자가 있는 명시적 이미지 세트를 지정합니다. 이 경우 프레임 목록은 괄호 안에 래핑됩니다. 프레임별 이미지 제공 수정자에 있는 쉼표에 이중 HTTP 인코딩을 적용해야 합니다. </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 다차원스핀 </span> 세트 </span> </p> </td> 
   <td colname="col2"> <p>다음 구문을 사용하여 명시적 다차원 회전 집합을 지정합니다. </p> <p> <span class="codeph"> (( <span class="varname"> 수평 회전 집합 </span>)[,( <span class="varname"> 수평 회전 집합 </span>)]) </span> </p> <p> 여기서 <span class="codeph"><span class="varname"> 수평 </span> 회전 </span> 집합은 주어진 수평 축에 대한 쉼표로 구분된 프레임 목록입니다. 모든 <span class="codeph"> 수평 <span class="varname"> 회전 집합은 </span> 동일한 프레임 수를 </span> 가져야 합니다. </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 수정자 </span></span> </p> </td> 
   <td colname="col2"> <p> 이미지 제공 명령;&amp; <span class="codeph"> 및 </span> 구분자는 <span class="codeph"> 각각 </span> %26 및 <span class="codeph"> %3D로 HTTP 인코딩 및 </span> %3D <span class="codeph"> </span>로 인코딩되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

또는

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetvideoswatchIdimageswatchIdsetIdswatchIdIDvideoswatchIdimageswatchIdsetIdswatchIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 미디어 <span class="varname"> 세트 </span></span> </p> </td> 
   <td colname="col2"> <p> 미디어 세트에 대한 참조를 지정합니다. 뷰어는 req=set IS 요청을 사용하여 서버에서 미디어 세트를 검색합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 비디오 <span class="varname"> </span></span> </p> </td> 
   <td colname="col2"> <p> 단일 비디오 또는 응용 비디오 집합. </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이미지 </span></span> </p> </td> 
   <td colname="col2"> <p> 단일 이미지. </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span></span> </p> </td> 
   <td colname="col2"> <p> 견본 집합. </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 견본 </span> ID </span> </p> </td> 
   <td colname="col2"> <p>견본 이미지. </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ID <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> 미디어 세트 항목 유형 식별자는 다음 중 하나일 수 있습니다. </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>단일 이미지 </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatch set </span> </p> <p>중첩된 견본 집합의 경우 </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> 회전 </span> </p> <p>회전 집합. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video </span> </p> <p>단일 비디오용 </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>응용 비디오 집합의 경우 </p> </li> 
     </ul> </p> <p> <p>참고: 이 기능은 Adobe Scene7 Publishing System에서 지원됩니다.adobe Experience Manager Assets에서는 지원되지 않습니다. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 수정자 </span></span> </p> </td> 
   <td colname="col2"> <p> 이미지 제공 명령;&amp; <span class="codeph"> 및 </span> 구분자는 <span class="codeph"> 각각 </span> %26 및 <span class="codeph"> %3D로 HTTP 인코딩 및 </span> %3D <span class="codeph"> </span>로 인코딩되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>IR(이미지 렌더링) 또는 UGC(사용자 생성 컨텐츠)를 사용하는 이미지는 이 뷰어에서 지원되지 않습니다.

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

필수.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

없음.

## 예제 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

단일 에셋 참조:

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

명시적 다차원 회전 집합:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

단일 혼합 미디어 집합 참조:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

명시적 혼합 미디어 세트:

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

