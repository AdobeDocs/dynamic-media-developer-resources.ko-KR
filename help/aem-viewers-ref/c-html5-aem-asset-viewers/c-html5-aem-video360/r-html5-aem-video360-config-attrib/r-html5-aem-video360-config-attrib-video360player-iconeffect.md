---
description: Video360 뷰어에 대한 구성 속성입니다.
seo-description: Video360 뷰어에 대한 구성 속성입니다.
seo-title: Video360Player.iconeffect
solution: Experience Manager
title: Video360Player.iconeffect
topic: Dynamic media
uuid: a0a2f840-e330-4636-8daf-1cd3f2eddf01
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# Video360Player.iconeffect{#video-player-iconeffect}

Video360 뷰어에 대한 구성 속성입니다.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 비디오가 일시 중지된 상태에서 비디오 위에 표시되도록 IconEffect를 활성화합니다. 일부 장치에서는 기본 컨트롤이 사용됩니다. 이 경우 <span class="codeph"> 아이콘 효과</span> 수정자는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 계수</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 나타나고 다시 나타나는 최대 횟수를 지정합니다. <span class="codeph"> -1</span>의 값은 아이콘이 무기한 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션을 표시하거나 숨기는 지속 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 자동으로 가려지기 전에 완전히 표시되는 상태로 유지되는 시간(초)을 설정합니다. 즉, 애니메이션의 페이드가 완료된 후 페이드 아웃 애니메이션이 시작되기 전의 시간입니다. 자동 숨기기 비헤이비어를 비활성화하려면 <span class="codeph"> 0</span>으로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
