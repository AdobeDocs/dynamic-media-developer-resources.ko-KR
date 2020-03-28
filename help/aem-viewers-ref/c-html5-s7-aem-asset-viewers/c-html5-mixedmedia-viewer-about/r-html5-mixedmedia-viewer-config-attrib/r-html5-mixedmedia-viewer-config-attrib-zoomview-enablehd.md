---
description: 널
seo-description: 널
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: fb4e96d8-3cbf-4764-a30f-879a5c4c8244
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`수`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> devicePixelRatio가 <span class="codeph"> 1</span> <span class="codeph"></span>이상인 디바이스, 즉 iPhone4 및 유사한 디바이스와 같은 고밀도 디스플레이를 사용하는 디바이스에 대한 최적화를 활성화, 제한 또는 비활성화할 수 있습니다. 활성 상태인 경우 구성 요소는 IS 이미지 요청의 크기를 장치가 픽셀 비율만 <span class="codeph"> 1</span> 가지며 그렇게 하면 대역폭을 줄일 수 있습니다. </p> <p>아래 예 2를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 수</span></span> </p> </td> 
   <td colname="col2"> <p> 제한 설정을 사용하는 경우 구성 요소는 지정된 제한까지 높은 픽셀 밀도를 활성화합니다. </p> <p>아래 예 2를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

뷰어와 함께 이 구성 속성을 사용할 때 예상되는 결과는 다음과 같습니다. 뷰어 크기는 1000 x 1000입니다.

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>set 변수가 </p> </th> 
   <th colname="col2" class="entry"> <p>결과 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 항상</span> </p> </td> 
   <td colname="col2"> <p>화면/장치의 픽셀 밀도를 항상 고려합니다. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>화면 픽셀 밀도가 1이면 요청된 이미지가 1000 x 1000입니다. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>화면 픽셀 밀도가 1.5이면 요청된 이미지가 1500 x 1500입니다. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>화면 픽셀 밀도가 2이면 요청된 이미지가 2000 x 2000입니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 안 함</span> </p> </td> 
   <td colname="col2"> <p>이 플러그인은 항상 픽셀 밀도를 1로 사용하며 장치의 HD 기능을 무시합니다. 따라서 요청된 이미지는 항상 1000 x 1000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>장치 픽셀 밀도는 결과 이미지가 지정된 제한보다 낮은 경우에만 요청되고 제공됩니다. </p> <p>제한 번호는 너비 또는 높이 차원에 적용됩니다. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>제한 번호가 1600이고 픽셀 밀도가 1.5이면 1500 x 1500 이미지가 제공됩니다. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>제한 번호가 1600이고 픽셀 밀도가 2이면 2000 x 2000 이미지가 한계를 초과하므로 1000 x 1000 이미지가 제공됩니다. </p> </li> 
     </ul> </p> <p><b>우수 사례</b>:최대 크기 이미지를 위해 회사 설정과 함께 제한 번호가 작동해야 합니다. 따라서 한도 번호를 회사 최대 이미지 크기 설정과 같게 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

