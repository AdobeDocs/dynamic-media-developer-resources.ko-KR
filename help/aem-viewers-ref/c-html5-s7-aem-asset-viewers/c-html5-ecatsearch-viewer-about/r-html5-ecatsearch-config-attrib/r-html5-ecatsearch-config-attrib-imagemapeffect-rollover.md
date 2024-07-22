---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>정보 패널을 표시할 시기를 지정합니다. </p> <p><span class="codeph"> 1</span>(으)로 설정하면 마우스가 이미지 맵 영역에 들어갈 때 정보 패널이 표시됩니다(이미지 맵에 비어 있지 않은 <span class="codeph"> rollover_key</span> 특성이 있는 경우). </p> <p><span class="codeph"> 0</span>(으)로 설정된 경우 이미지 맵을 선택할 때 정보 패널이 트리거됩니다(이미지 맵에 비어 있지 않은 <span class="codeph"> rollover_key</span>과(와) 비어 있는 <span class="codeph"> href</span> 특성이 있는 경우). </p> <p> 터치 지원 데스크톱 시스템을 포함한 터치 장치에서 무시되며 자동으로 <span class="codeph"> 0</span>(으)로 설정됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-ccfedc2da28f412a86d03f390db92b4b}

선택적.

## 기본값 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 예 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
