---
title: PageView.enableHD
description: PageView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f03762f2-87db-4284-ba59-9ece8caa0d09
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# PageView.enableHD{#pageview-enablehd}

` [PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`숫자`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상|제한 안 함|제한</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>이 <span class="codeph"> 1</span>보다 큰 장치, 즉, iPhone4 및 이와 유사한 장치와 같이 고밀도 디스플레이를 사용하는 장치의 최적화를 활성화, 제한 또는 비활성화합니다. 활성화하면 구성 요소가 장치의 픽셀 비율이 <span class="codeph"> 1</span>인 것처럼 IS 이미지 요청의 크기를 제한하여 대역폭을 줄입니다. </p> <p>아래 예 참조 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 숫자</span></span> </p> </td> 
   <td colname="col2"> <p> 제한 설정을 사용하는 경우 구성 요소는 높은 픽셀 밀도를 지정된 제한까지만 활성화합니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-38b878e38caa439bb462d4fa637afdaa}

선택적.

## 기본값 {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## 예 {#section-09433488774245d985acef6c0341ece0}

뷰어에 이 구성 속성을 사용하고 뷰어 크기는 1000 x 1000인 경우 예상되는 결과는 다음과 같습니다.

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>설정된 변수가 인 경우 </p> </th> 
   <th colname="col2" class="entry"> <p>결과 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 항상</span> </p> </td> 
   <td colname="col2"> <p>화면/장치의 픽셀 밀도는 항상 고려됩니다. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>화면 픽셀 밀도가 1이면 요청한 이미지는 1000 x 1000입니다. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>화면 픽셀 밀도 = 1.5이면 요청한 이미지는 1500 x 1500입니다. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>화면 픽셀 밀도가 2이면 요청된 이미지는 2000 x 2000입니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 사용 안 함</span> </p> </td> 
   <td colname="col2"> <p>이 설정은 항상 픽셀 밀도 1을 사용하며 장치의 HD 기능을 무시합니다. 따라서 요청된 이미지는 항상 1000 x 1000입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 제한&lt;숫자&gt;</span> </p> </td> 
   <td colname="col2"> <p>결과 이미지가 지정된 제한 이하인 경우에만 장치 픽셀 밀도가 요청되고 제공됩니다. </p> <p>제한 번호는 너비 또는 높이 차원에 적용됩니다. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>제한 번호가 1600이고 픽셀 밀도가 1.5이면 1500 x 1500 이미지가 제공됩니다. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>제한 번호가 1600이고 픽셀 밀도가 2인 경우 2000 x 2000 이미지가 제한을 초과하므로 1000 x 1000 이미지가 제공됩니다. </p> </li> 
     </ul> </p> <p><b>모범 사례</b>: 최대 크기 이미지에 대한 회사 설정에서 제한 숫자를 사용해야 합니다. 따라서 제한 수를 회사 최대 이미지 크기 설정과 동일하게 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
