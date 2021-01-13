---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
topic: Dynamic media
uuid: 7496fea1-8a69-4749-ab4b-ae6d375441b8
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 10%

---


# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 모든 축소판에 적용되는 이미지 제공 명령 문자열. URL에 지정된 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>의 모든 항목은 각각 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>으로 HTTP로 인코딩되어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-df5a0604766b4ac2b9a6742b377e427c}

선택 사항입니다.

## 기본값 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

없음.

## 예 {#section-813de2905d6c44c0991cfe0931581462}

뷰어 URL에 지정된 경우.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

구성 데이터에 지정된 경우입니다.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
