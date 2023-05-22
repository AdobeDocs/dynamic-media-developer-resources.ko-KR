---
description: 보기 높이. 응답 이미지의 높이를 지정합니다.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# hei{#hei}

보기 높이. 응답 이미지의 높이를 지정합니다.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>이미지 높이, 픽셀 단위(정수: 0보다 큼). </p></td> 
 </tr> 
</table>

래스터 형식은 기본 뷰 크기(또는 DefaultPix 설정)를 사용하여 렌더링됩니다. 클릭 **[!UICONTROL 응용 프로그램 설정]** > **[!UICONTROL 게시 설정]** > **[!UICONTROL 이미지 서버]**&#x200B;을 클릭한 다음 폭과 높이 값을 입력합니다. 크기가 작을수록 성능이 향상됩니다. 변경 사항을 적용하려면 설정을 저장하고 이미지 제공 게시를 수행해야 합니다.

을(를) 적용하면 `scale=1` 명령을 실행하면 래스터 형식 요청이 FXG에 지정된 크기로 렌더링됩니다.

## 기본값 {#section-76ee3daa77cb468ab310821357cc9404}

둘 다 아닌 경우 `wid=`, `hei=`, 또는 `scale=` 을 지정하면 응답 이미지가 FXG 파일에 지정된 기본 보기 크기입니다.

## 예 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

형식을 지정하지 않으면 이미지가 SWF 파일로 렌더링됩니다. 이 경우 SWF은 일반적으로 브라우저 창의 크기로 확장되므로 높이와 너비는 의미가 없습니다. 따라서 hei 및 wid는 래스터 또는 PDF 형식에만 적용됩니다. 래스터 형식에는 다음이 포함됩니다.

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-알파
* TIF-alpha
* PNG-alpha
