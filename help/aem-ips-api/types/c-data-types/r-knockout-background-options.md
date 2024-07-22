---
title: 녹아웃 배경 옵션
description: 선택한 이미지의 배경을 마스킹(녹아웃)합니다. 이 데이터 유형을 사용하면 대상 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다. 기본적으로 꺼져 있는 선택적 매개 변수입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

선택한 이미지의 배경을 마스킹(녹아웃)합니다. 이 데이터 유형을 사용하면 대상 이미지 외부의 투명도를 사용하여 다른 레이어에 오버레이할 수 있습니다.

이 데이터 유형은 선택 사항이며 기본적으로 꺼져 있습니다.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## 매개 변수 {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>Adobe Experience Manager에서 `KnockoutBackgroundOptions`을(를) 구성하는 경우 대신 다음 매개 변수를 사용하십시오.
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>예: `kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 모서리</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">작업할 코너를 선택합니다. <span class="codeph"> corner</span>이(가) 다음 값을 허용합니다. 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> 왼쪽 위</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> 왼쪽 아래</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> 오른쪽 위</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> 오른쪽 아래</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 허용 한도</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">투명도에 따라 이미지 가장자리에서 공백을 제거하는 선택적 설정입니다. 0.0에서 1.0 사이의 값 범위를 허용합니다. 다음을 지정합니다. 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0을 지정하면 색상이 정확하게 일치합니다. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 - 대부분의 색상 차이를 활성화합니다. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><span class="codeph"><span class="varname"> corner</span></span> 변수로 지정된 위치의 픽셀 투명도를 제어합니다. <span class="codeph"> fillMethod</span>은(는) 다음 값을 허용합니다. </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>: 지정한 모퉁이의 모든 픽셀을 투명하게 바꿉니다. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>: 위치에 관계없이 일치하는 모든 픽셀을 투명하게 바꿉니다. </li> 
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

## 사용한 사람 {#section-28c43baafe85434a9ee9e303ed10569a}

`KnockoutBackgroundOptions` 형식은 다음 경우에 사용됩니다.

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
