---
title: CallToAction.direction
description: 대화형 비디오 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# CallToAction.direction{#calltoaction-direction}

대화형 비디오 뷰어에 대한 구성 속성입니다.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|왼쪽|오른쪽  </span> </p> </td> 
   <td colname="col2"> <p> 보기에서 미리 보기를 채우는 방법을 지정합니다. </p> <p>왼쪽에서 오른쪽으로 채우기 순서를 설정하려면 <span class="codeph"> 왼쪽으로 </span> 로 설정하십시오. </p> <p><span class="codeph"> 오른쪽 </span>으로 설정하면 보기가 오른쪽에서 왼쪽, 위에서 아래로 채워지도록 순서를 반대로 설정합니다. </p> <p>로케일이 <span class="codeph"> "ja" </span>;(으)로 설정된 경우 구성 요소가 올바른 모드를 적용하도록 하려면 <span class="codeph"> auto </span> 로 설정합니다. 그렇지 않으면 <span class="codeph"> 왼쪽 </span>이 사용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
