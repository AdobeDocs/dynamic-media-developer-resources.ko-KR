---
title: SpinView.maxloadradius
description: SpinView가 유휴 상태일 때 각 방향에서 미리 로드할 프레임의 최대 수를 나타냅니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

SpinView가 유휴 상태일 때 각 방향에서 미리 로드할 프레임의 최대 수를 나타냅니다.

` [SpinView.|<containerId>_spinView.]maxloadradius= *`값`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 값</span></span> </p> </td> 
   <td colname="col2"> <p> 값 <span class="codeph"> -1</span>은(는) 집합의 모든 프레임을 미리 로드합니다. 미리 로드된 프레임은 항상 SpinView가 처음 로드되었던 원래 해상도로 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 미리 로드된 프레임의 품질을 제어합니다. </p> <p><span class="codeph"> 1</span>(으)로 설정하면 구성 요소의 크기와 일치하는 고품질로 프레임이 로드됩니다. </p> <p><span class="codeph"> 0</span>(으)로 설정된 경우 저해상도 미리 보기 타일만 로드됩니다.</p> <p>높은 해상도로 미리 로드하면 특히 자동 회전이 활성화된 경우 사용자의 경험이 향상됩니다. 동시에 시작 시간이 느려지고 네트워크 소비가 증가하므로 주의하여 사용해야 합니다. 고해상도 미리 로드를 사용하면 미리 로드된 프레임의 해상도는 항상 구성 요소가 처음 로드되었던 원래 해상도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
