---
description: 이미지 제공 제어 스크립트입니다. 이 스크립트는 Image Serving Server Supervisor를 시작, 중지 또는 다시 시작하는 데 사용되며, 이 경우 다른 모든 Image Serving 구성 요소가 시작, 정지 또는 다시 시작됩니다.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---

# ImageServing{#imageserving}

이미지 제공 제어 스크립트입니다. 이 스크립트는 Image Serving Server Supervisor를 시작, 중지 또는 다시 시작하는 데 사용되며, 이 경우 다른 모든 Image Serving 구성 요소가 시작, 정지 또는 다시 시작됩니다.

## 사용 {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`명령`*`

## 명령 {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>명령 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 시작 </span> </p> </td> 
   <td colname="col2"> <p> 서버 감독자 및 기타 모든 이미지 제공 구성 요소를 시작합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> 서버 감독자를 포함하여 모든 이미지 제공 구성 요소를 중지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 다시 시작 </span> </p> </td> 
   <td colname="col2"> <p>서버 감독자를 포함하여 모든 이미지 제공 구성 요소를 다시 시작합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ps 다시 시작 | | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Tomcat/Platform 서버, 이미지 서버 또는 SVG를 다시 시작합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상태 [ ps | | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>이미지 서버, Tomcat/Platform 서버 및 SVGserver에 대한 작동 시간 및 현재 메모리 사용 정보 또는 지정된 서버에 대한 상태를 반환합니다.서버 감독자가 실행되고 있지 않으면 정보 메시지가 대신 반환됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
