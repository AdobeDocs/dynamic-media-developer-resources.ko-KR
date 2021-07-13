---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>정보 패널을 표시할 시기를 지정합니다. </p> <p><span class="codeph"> 1</span> 로 설정하면 마우스가 이미지 맵 영역을 입력하면 정보 패널이 표시됩니다(이미지 맵에 비어 있지 않은 경우 <span class="codeph"> rollover_key</span> 특성). </p> <p>이미지 맵을 클릭할 때 <span class="codeph"> 0</span> 정보 패널이 트리거되는 경우(이미지 맵에 비어 있지 않은 <span class="codeph"> rollover_key</span> 및 비어 있는 <span class="codeph"> href</span> 특성). </p> <p> 터치 지원 데스크톱 시스템을 포함한 터치 장치에서 무시되고, 자동으로 <span class="codeph"> 0</span>로 설정됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-ccfedc2da28f412a86d03f390db92b4b}

선택 사항입니다.

## 기본값 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 예 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
