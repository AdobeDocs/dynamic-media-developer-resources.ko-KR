---
description: 높이 보기. 응답 이미지의 높이를 지정합니다.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 3%

---


# hei{#hei}

높이 보기. 응답 이미지의 높이를 지정합니다.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>이미지 높이(픽셀 단위: 0보다 큼). </p></td> 
 </tr> 
</table>

래스터 형식은 기본 보기 크기(또는 DefaultPix 설정)를 사용하여 렌더링됩니다. **[!UICONTROL 응용 프로그램 설정]** > **[!UICONTROL 제작 설정]** > **[!UICONTROL 이미지 서버]**&#x200B;를 클릭한 다음 너비 및 높이 값을 입력합니다. 크기가 작을수록 성능이 향상됩니다. 설정을 저장하고 변경 사항을 적용하려면 이미지 제공 게시를 수행해야 합니다.

`scale=1` 명령을 적용하면 래스터 형식 요청이 FXG에 지정된 크기로 렌더링됩니다.

## 기본값 {#section-76ee3daa77cb468ab310821357cc9404}

`wid=`, `hei=` 또는 `scale=`가 지정되지 않은 경우 응답 이미지는 FXG 파일에 지정된 기본 보기 크기입니다.

## 예 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

형식을 지정하지 않으면 이미지가 SWF 파일로 렌더링됩니다. 이 경우 SWF는 일반적으로 브라우저 창의 크기로 확장되므로 높이와 너비는 아무런 의미가 없습니다. 따라서 hei와 wid는 래스터 또는 PDF 형식에만 적용됩니다. 래스터 형식은 다음과 같습니다.

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-알파

