---
description: 널
seo-description: 널
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 1ed18115-9e29-434a-a48d-40bf6b48fe6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 이미지 서버에서 이미지를 로드하는 데 구성 요소에서 사용할 이미지 형식을 지정합니다. 지정된 형식이 <span class="codeph"> "-alpha"로 끝나는</span>경우 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 다른 모든 이미지 포맷의 경우 구성 요소는 이미지를 불투명하게 처리합니다. 기본적으로 구성 요소에는 흰색 배경이 있습니다. 따라서 완전히 투명하게 하려면 <span class="codeph"> 배경색</span> CSS 속성을 <span class="codeph"> 투명하게</span>설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

선택 사항입니다.

## 기본값 {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## 예 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
