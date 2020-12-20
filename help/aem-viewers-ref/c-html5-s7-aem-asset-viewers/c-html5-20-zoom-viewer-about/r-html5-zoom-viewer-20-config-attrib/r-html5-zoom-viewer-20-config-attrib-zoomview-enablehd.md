---
description: 널
seo-description: 널
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 1d64e161-761e-4f43-bb05-3a0edc5a3c60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 3%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`수`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> iPhone4 및 이와 유사한 장치와 같은 고밀도 디스플레이가 있는 장치인 <span class="codeph"> devicePixelRatio</span>이(가) <span class="codeph"> 1</span>보다 큰 장치에 대한 최적화를 활성화, 제한 또는 비활성화합니다. 활성 상태인 경우, 구성 요소는 마치 장치가 <span class="codeph"> 1</span>의 픽셀 비율만 있고 이렇게 하면 대역폭이 감소되는 것처럼 IS 이미지 요청의 크기를 제한합니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 수</span></span> </p> </td> 
   <td colname="col2"> <p> 제한 설정을 사용하는 경우 구성 요소는 지정된 제한까지 높은 픽셀 밀도를 활성화합니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

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
   <td colname="col2"> <p>화면/장치의 픽셀 밀도는 항상 고려됩니다. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>화면 픽셀 밀도가 1이면 요청된 이미지가 1000 x 1000입니다. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>화면 픽셀 밀도가 1.5이면 요청된 이미지가 1500 x 1500입니다. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>화면 픽셀 밀도가 2이면 요청된 이미지가 2000 x 2000입니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 안 함</span> </p> </td> 
   <td colname="col2"> <p>항상 1의 픽셀 밀도를 사용하며 장치의 HD 기능을 무시합니다. 따라서 요청된 이미지는 항상 1000 x 1000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 한계&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>장치 픽셀 밀도는 결과 이미지가 지정된 제한보다 낮은 경우에만 요청되고 제공됩니다. </p> <p>제한 번호는 너비 또는 높이 차원에 적용됩니다. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>제한 번호가 1600이고 픽셀 밀도가 1.5이면 1500 x 1500 이미지가 제공됩니다. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>제한 번호가 1600이고 픽셀 밀도가 2이면 2000 x 2000 이미지가 한계를 초과하므로 1000 x 1000 이미지가 제공됩니다. </p> </li> 
     </ul> </p> <p><b>우수 사례</b>:최대 크기 이미지를 위해 회사 설정과 함께 제한 수를 사용해야 합니다. 따라서 한도 숫자를 회사 최대 이미지 크기 설정과 같도록 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

