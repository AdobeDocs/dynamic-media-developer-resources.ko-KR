---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
feature: Dynamic Media Classic,뷰어,SDK/API,혼합 미디어 집합
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 6%

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`수`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> iPhone4 및 이와 유사한 장치와 같은 고밀도 디스플레이가 있는 장치인 <span class="codeph"> devicePixelRatio</span>이(가) <span class="codeph"> 1</span>보다 큰 장치에 대한 최적화를 활성화, 제한 또는 비활성화합니다. 활성 상태인 경우, 구성 요소는 마치 장치가 <span class="codeph"> 1</span>의 픽셀 비율만 있는 것처럼 IS 이미지 요청의 크기를 제한하므로 대역폭을 줄입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 수</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 제한</span> 설정을 사용하는 경우 구성 요소는 지정된 제한까지 높은 픽셀 밀도를 활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
