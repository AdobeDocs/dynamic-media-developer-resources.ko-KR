---
description: 널
seo-description: 널
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 57c86b63-7495-4f6f-bd30-8c4ebf017e36
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대에 표시되는 시간의 패턴을 설정합니다. 여기서 <span class="codeph"> h</span> 는 <span class="codeph"> 시간, m</span><span class="codeph"> 은 분,</span> s는 초입니다. </p> <p>각 시간 단위에 사용되는 문자 수는 해당 단위에 대해 표시할 자릿수를 결정합니다. 해당 숫자가 지정된 숫자에 맞지 않으면 해당 값이 다음 단위에 표시됩니다. </p> <p>예를 들어 현재 동영상 시간이 67분 5초인 경우 시간 패턴 <span class="codeph"> m:ss</span> 는 67:05로 표시됩니다. 주어진 시간 패턴이 <span class="codeph"> h:mm:s인 경우 동일한 시간이 1:07:5로 표시됩니다</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
