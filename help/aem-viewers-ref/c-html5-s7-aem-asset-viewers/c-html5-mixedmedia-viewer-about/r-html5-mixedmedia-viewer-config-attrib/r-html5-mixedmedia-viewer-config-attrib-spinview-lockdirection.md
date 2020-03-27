---
description: 널
seo-description: 널
seo-title: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic media
uuid: b46a3d78-e381-4351-a4f4-a228386df527
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 2D 회전 집합의 경우 회전 방향을 변경할지 여부를 지정합니다. </p> <p>1 <span class="codeph"> </span>로 설정하면 구성 요소가 제스처의 시작 부분에서 기본 드래그 또는 스와이프 방향(가로 및 세로)을 식별합니다. 이후 제스처가 끝날 때까지 해당 방향을 유지합니다. 예를 들어 사용자가 가로 회전을 시작한 다음 드래그 동작을 세로 방향으로 계속하기로 결정한 경우 구성 요소는 세로 회전을 수행하지 않습니다.대신 마우스 또는 스와이프의 가로 이동만 고려합니다. </p> <p>값 <span class="codeph"> 0을 </span> 사용하면 제스처가 진행되는 동안 언제든지 회전 방향을 변경할 수 있습니다. 스핀 세트가 1D인 경우 설정은 영향을 주지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
