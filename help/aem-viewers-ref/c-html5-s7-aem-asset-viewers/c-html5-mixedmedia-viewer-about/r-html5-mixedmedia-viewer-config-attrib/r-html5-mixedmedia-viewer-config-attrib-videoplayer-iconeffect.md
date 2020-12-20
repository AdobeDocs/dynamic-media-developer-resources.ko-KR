---
description: 널
seo-description: 널
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 8e112f3c-8fa6-4c77-94c5-5027275225e7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 6%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 비디오가 일시 정지되면 IconEffect가 비디오 위에 표시되도록 합니다. 일부 장치에서는 기본 컨트롤이 사용됩니다. 이 경우 <span class="codeph"> 아이콘 효과</span> 수정자는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 나타나고 다시 나타나는 최대 횟수를 지정합니다. <span class="codeph"> -1</span>의 값은 아이콘이 무기한 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 페이드</span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션을 표시하거나 숨기는 지속 시간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffect가 자동으로 숨겨지기 전에 계속 표시되는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 후 페이드 아웃 애니메이션이 시작하기 전에 시간이 경과됩니다. <span class="codeph"> 0</span> 설정은 자동 숨기기 동작을 비활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
