---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,User
exl-id: fd1fa0f2-d666-4470-8b5b-673f3c4327e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---

# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 페이지 이미지에 적용되는 이미지 제공 명령 문자열입니다. URL에 지정된 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>의 모든 항목은 각각 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>로 HTTP로 인코딩되어야 합니다. </p> <p> <p>참고:  이미지 크기 조정 조작 명령은 지원되지 않습니다. </p> </p> </td> 
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

구성 데이터에 지정되는 경우.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
