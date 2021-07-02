---
description: SpinView가 유휴 상태일 때 각 방향으로 미리 로드할 최대 프레임 수를 나타냅니다.
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

SpinView가 유휴 상태일 때 각 방향으로 미리 로드할 최대 프레임 수를 나타냅니다.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> -1</span> 값은 집합의 모든 프레임을 미리 로드합니다. 미리 로드된 프레임은 항상 SpinView가 처음에 로드되었던 원래 해상도에서 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 미리 로드된 프레임의 품질을 제어합니다. </p> <p><span class="codeph"> 1</span> 로 설정하면 프레임이 고품질로 로드되어 구성 요소의 크기와 일치합니다. </p> <p><span class="codeph"> 0</span>으로 설정하면 저해상도 미리 보기 타일만 로드됩니다. </p> <p>특히 자동 스핀이 활성화되어 있을 때 고해상도로 사전 로드하면 최종 사용자 경험이 향상됩니다. 동시에 시작 시간이 느려지고 네트워크 사용량이 높아지므로 주의하여 사용해야 합니다. 고해상도 사전 로드를 사용하는 경우 미리 로드된 프레임은 항상 구성 요소가 처음 로드되는 원래 해상도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
