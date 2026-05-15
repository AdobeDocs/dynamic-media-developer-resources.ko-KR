---
title: wid
description: 보기 너비. 응답 이미지(이미지 보기)의 너비를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
TQID: 'https://experienceleague.adobe.com/A1n6WpZEsDWfdLoQZZY-ykX4zXjG86BRXHnVfcpO9yo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 1%

---

# wid{#wid}

보기 너비. 응답 이미지(이미지 보기)의 너비를 지정합니다.

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 값</span></span> </p> </td> 
  <td class="stentry"> <p>이미지 너비, 픽셀 단위(int가 0보다 큼), </p></td> 
 </tr> 
</table>

## 기본값 {#section-830bae0b6bac440098444d7cdcb23e2e}

`wid=`, `hei=` 및 `scale=`을(를) 지정하지 않으면 응답 이미지가 FXG 파일에 지정된 기본 보기 크기입니다.

래스터 형식은 기본 뷰 크기(또는 DefaultPix 설정)를 사용하여 렌더링됩니다. **[!UICONTROL 응용 프로그램 설정]** > **[!UICONTROL 게시 설정]** > **[!UICONTROL 이미지 서버]**&#x200B;를 클릭한 다음 너비와 높이 값을 입력하십시오. 크기가 작을수록 성능이 향상됩니다. 설정을 저장하고 이미지 서버 게시를 수행하여 변경 사항을 적용합니다.

`scale=1` 명령을 적용하면 래스터 형식 요청이 FXG에 지정된 크기로 렌더링됩니다.

## 예 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

형식을 지정하지 않으면 이미지가 SWF 파일로 렌더링됩니다. 이 경우 SWF은 일반적으로 브라우저 창의 크기로 확장되므로 높이와 너비는 의미가 없습니다. 따라서 `hei` 및 `wid`은(는) 래스터 또는 PDF 형식에만 적용됩니다. 래스터 형식에는 다음이 포함됩니다.

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
