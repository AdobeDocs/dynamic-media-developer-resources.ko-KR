---
description: 선택한 이미지의 배경을 마스크(녹아웃)합니다. 따라서 대상 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. 기본적으로 꺼져 있는 선택적 매개 변수입니다.
seo-description: 선택한 이미지의 배경을 마스크(녹아웃)합니다. 따라서 대상 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. 기본적으로 꺼져 있는 선택적 매개 변수입니다.
seo-title: 녹아웃 배경 옵션
solution: Experience Manager
title: 녹아웃 배경 옵션
topic: Scene7 Image Production System API
uuid: 1486d646-f42a-4ed4-9450-313950969c39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---


# KnockoutBackgroundOptions{#knockoutbackgroundoptions}

선택한 이미지의 배경을 마스크(녹아웃)합니다. 따라서 대상 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. 기본적으로 꺼져 있는 선택적 매개 변수입니다.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## 매개 변수 {#section-3149b49ccb714e6eafa6655354816819}

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 모퉁이</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">작업할 모퉁이를 선택합니다. <span class="codeph"> 다음 값을 </span> 코너링합니다. 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> 왼쪽 위</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> 왼쪽 아래</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> 오른쪽 위</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> 오른쪽 아래</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 허용치</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">투명도를 기반으로 이미지 가장자리에서 공백을 제거하는 선택 설정입니다. 0.0부터 1.0까지의 값 범위를 허용합니다. 다음을 지정합니다. 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">색상을 정확하게 일치시키기 위해 0을 설정합니다. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 - 색상 차이가 가장 많이 나는 것을 활성화합니다. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p><span class="codeph"><span class="varname"> 모퉁이</span></span> 변수에 의해 지정된 위치의 픽셀 투명도를 제어합니다. <span class="codeph"> fillMethod</span>은 다음 값을 허용합니다. </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>:지정된 모퉁이의 모든 픽셀을 투명하게 바꿉니다. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> 일치 픽셀</span>:위치에 상관없이 일치하는 모든 픽셀을 투명하게 바꿉니다. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## {#section-28c43baafe85434a9ee9e303ed10569a}에서 사용됨

`KnockoutBackgroundOptions` 유형은 다음 사용자에 의해 사용됩니다.

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

