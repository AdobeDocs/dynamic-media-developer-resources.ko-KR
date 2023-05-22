---
title: 재생 일시 중지 단추
description: 재생/일시 중지 버튼을 사용하면 사용자가 캐러셀 자동 재생 동작을 일시 중지하거나 다시 시작할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 1b48aa7f-d1c8-4367-94c2-689991b90942
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 2%

---

# 재생 일시 중지 단추{#playpause-button}

재생/일시 중지 버튼을 사용하면 사용자가 캐러셀 자동 재생 동작을 일시 중지하거나 다시 시작할 수 있습니다.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

단추는 다음 경우에만 표시됩니다. `CarouselViewer.autoplay` 매개 변수가 로 설정되어 있습니다. `1`; 그렇지 않으면 숨겨집니다. CSS를 사용하여 이 단추를 포함하는 컨트롤 막대에 따라 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음 CSS 클래스 선택기로 제어합니다.

`.s7carouselviewer .s7playpausebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 테두리 맨 위에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 테두리 오른쪽에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>뷰어의 왼쪽에서 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 테두리 아래쪽에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>참조: <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스타일 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 커서 </span> </p> </td> 
   <td colname="col2"> <p>커서 유형입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md) 추가 정보.

예를 들어 28 x 28픽셀인 재생 일시 중지 버튼을 설정한다고 가정합니다. 단추는 뷰어의 맨 아래에서 17픽셀, 왼쪽 가장자리에서 12픽셀로 배치할 수 있습니다. 그리고 선택되거나 선택되지 않을 때 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시하려고 합니다.

```
.s7carouselviewer .s7playpausebutton { 
bottom:17px; 
left:12px; 
width:28px; 
height:28px; 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='up'] { 
  background-image:url(images/playBtn_up.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
}
```
