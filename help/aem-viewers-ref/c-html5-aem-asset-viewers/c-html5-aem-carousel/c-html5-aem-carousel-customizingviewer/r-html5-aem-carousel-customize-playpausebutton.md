---
description: '[재생/일시 정지] 단추를 사용하면 회전판 자동 재생 동작을 일시 정지하거나 다시 시작할 수 있습니다.'
seo-description: '[재생/일시 정지] 단추를 사용하면 회전판 자동 재생 동작을 일시 정지하거나 다시 시작할 수 있습니다.'
seo-title: 재생 일시 정지 단추
solution: Experience Manager
title: 재생 일시 정지 단추
topic: Dynamic media
uuid: 342def36-9dfb-487c-bed5-b0f301ce8430
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 2%

---


# PlayPause 단추{#playpause-button}

[재생/일시 정지] 단추를 사용하면 회전판 자동 재생 동작을 일시 정지하거나 다시 시작할 수 있습니다.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

버튼은 `CarouselViewer.autoplay` 매개 변수가 `1`;으로 설정된 경우에만 표시됩니다.그렇지 않으면 숨겨집니다. CSS를 사용하여 이 단추를 포함하는 컨트롤 막대를 기준으로 크기를 조정하고 스킨 후 위치를 지정할 수 있습니다.

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p>뷰어 테두리의 맨 위에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 테두리의 오른쪽에서 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 왼쪽에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 테두리 아래쪽의 위치입니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 커서  </span> </p> </td> 
   <td colname="col2"> <p>커서 유형입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md)의 현지화를 참조하십시오.

예 - 28 x 28픽셀인 재생 일시 정지 단추를 설정하려면, 이 단추를 설정하려면 뷰어 아래쪽에서 17픽셀, 왼쪽 가장자리에서 12픽셀로 배치하고, 이 단추를 선택하거나 선택하지 않을 때 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시합니다.

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

