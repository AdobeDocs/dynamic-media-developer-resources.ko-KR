---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`값`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 값</span></span> </p> </td> 
   <td colname="col2"> <p> SpinView가 유휴 상태일 때 각 방향에서 미리 로드할 프레임의 최대 수를 나타냅니다. 값 <span class="codeph"> -1</span>은(는) 집합의 모든 프레임을 미리 로드합니다. 미리 로드된 프레임은 항상 SpinView가 처음 로드되었던 원래 해상도로 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 미리 로드된 프레임의 품질을 제어합니다. <span class="codeph">(으)로 설정하면 구성 요소의 크기와 일치하는 고품질의 1</span> 프레임이 로드됩니다. <span class="codeph"> 0</span>(으)로 설정된 경우 저해상도 미리 보기 타일만 로드됩니다. </p> <p>특히 자동 회전이 활성화된 경우 고해상도로 미리 로드하면 최종 사용자 경험이 향상됩니다. 동시에 시작 시간이 느려지고 네트워크 사용량이 증가하므로 신중하게 사용하십시오. 고해상도 미리 로드를 사용하는 경우 미리 로드된 프레임의 해상도는 항상 구성 요소가 처음 로드되었던 원래 해상도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택적.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
