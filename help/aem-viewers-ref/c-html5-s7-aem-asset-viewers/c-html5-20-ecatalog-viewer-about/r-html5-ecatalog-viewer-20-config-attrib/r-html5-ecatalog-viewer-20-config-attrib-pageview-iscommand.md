---
description: 널
seo-description: 널
seo-title: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
topic: Dynamic media
uuid: 6c853c6a-a57d-4cab-ad71-74baf9e870d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 페이지 이미지에 적용되는 이미지 제공 명령 문자열. URL에 지정된 경우 &amp; <span class="codeph"></span><span class="codeph"> 및</span> =의 모든 항목은 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>,각각 HTTP로 인코딩되어야 합니다. </p> <p> <p>참고: 이미지 크기 조정 조작 명령은 지원되지 않습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-df5a0604766b4ac2b9a6742b377e427c}

선택 사항입니다.

## 기본값 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

없음.

## 예 {#section-813de2905d6c44c0991cfe0931581462}

뷰어 URL 파섹

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정된 경우입니다.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
