---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 8%

---

# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 모든 썸네일에 적용되는 이미지 제공 명령 문자열. URL에 지정되는 경우 <span class="codeph"> 및</span> 및 <span class="codeph"> =</span> 은(는) (으)로 HTTP 인코딩되어야 합니다. <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>, 각각 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-df5a0604766b4ac2b9a6742b377e427c}

선택적.

## 기본값 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

없음.

## 예 {#section-813de2905d6c44c0991cfe0931581462}

뷰어 URL에 지정되는 경우.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

구성 데이터에 지정된 경우.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
