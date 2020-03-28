---
description: 최적화된 피라미드 TIF 파일에 대한 이미지 선명도를 개선하는 설정입니다.
seo-description: 최적화된 피라미드 TIF 파일에 대한 이미지 선명도를 개선하는 설정입니다.
seo-title: UnsharpMaskOptions
solution: Experience Manager
title: UnsharpMaskOptions
topic: Scene7 Image Production System API
uuid: 73073de0-41b6-471c-8887-f6b94ed2af90
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# UnsharpMaskOptions{#unsharpmaskoptions}

최적화된 피라미드 TIF 파일에 대한 이미지 선명도를 개선하는 설정입니다.

`unsharpMaskOptions=[ *`양, 반경, 임계값, 단색`*]`

## 매개 변수 {#section-c3f0d03136ba4422819cb463bd393885}

옵션 값을 `unsharpMaskOptions` `minOccurs=" *`n으로 지정합니다.`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 이름 </th>
   <th colname="col2" class="entry"> 유형 </th>
   <th colname="col3" class="entry"> 설명 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 금액</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>가장자리 픽셀에 적용된 대비를 제어합니다. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">범위:0.0 - 5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">기본값:0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 반경</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>이미지 가장자리 주위의 픽셀 수를 설정하여 선명도를 제어합니다. 올바른 값은 이미지 크기에 따라 달라집니다. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">범위:0.0 - 250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">낮은 값은 가장자리 픽셀만 선명하게 합니다. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">높은 값은 더 넓은 범위의 픽셀을 선명하게 합니다. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 임계값</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>가장자리 픽셀로 간주하여 선명하게 하기 전에 주변 영역과 얼마나 다른 픽셀을 사용해야 하는지를 결정합니다. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">범위:0 - 255(정수만 해당). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">기본값:6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 단색</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>값에는 <span class="codeph"> 0</span> 또는 <span class="codeph"> 1만</span> 포함됩니다. </p><p>각 색상 구성 요소에 개별적으로 적용하거나 <span class="codeph"> 1</span> <span class="codeph"></span> 이미지 밝기(강도)에만 적용하려면 0으로 설정합니다. 레이어 마스크 또는 합성 마스크도 선명하게 됩니다. </p><p><span class="codeph"><span class="varname"> 흑백</span></span> 이미지는 회색 음영 이미지에 대해 무시됩니다. </p></td>
  </tr>
 </tbody>
</table>

## 예 {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## 사용 방법 {#section-db8124a5468b498694a780f8a56a4560}

이 `unsharpMaskOptions` 유형은 다음과 같이 사용됩니다.

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrl작업](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [이미지 제공 API 참조:op_usm](https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/http_ref/r_op_usm.html)

