---
title: ImageMapEffect.롤오버
description: ImageMapEffect.롤오버
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
TQID: 'https://experienceleague.adobe.com/V5KPk6tOhMcCUtL7iraaeBNt4xp81Uo7FTpT-1Z44ks'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 5%

---

# ImageMapEffect.롤오버{#imagemapeffect-rollover}

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
