---
description: 널
seo-description: 널
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> SpinView가 유휴 상태일 때 각 방향으로 미리 로드할 최대 프레임 수를 나타냅니다. - <span class="codeph"> 1</span> 값은 세트의 모든 프레임을 미리 로드합니다. 미리 로드된 프레임은 항상 SpinView가 처음에 로드되었던 원래 해상도에서 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 미리 로드된 프레임의 품질을 제어합니다. 1 <span class="codeph"> 프레임으로 설정하면</span> 구성 요소의 크기와 일치하는 고품질 프레임을 로드합니다. 0으로 <span class="codeph"> 설정하면</span> 저해상도 미리 보기 타일만 로드됩니다. </p> <p>고해상도로 미리 로드하면 최종 사용자 경험이 향상되며, 특히 자동 회전이 활성화된 경우 더욱 그렇습니다. 동시에 시작 시간이 느려지고 네트워크 사용량이 높으므로 주의해서 사용하십시오. 고해상도 미리 로드를 사용하는 경우 미리 로드된 프레임은 항상 구성 요소가 처음에 로드되었던 원래 해상도에 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택 사항입니다.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
