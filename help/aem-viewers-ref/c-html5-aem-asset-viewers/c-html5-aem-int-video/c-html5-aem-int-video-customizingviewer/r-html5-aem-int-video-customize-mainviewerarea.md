---
description: 기본 보기 영역은 인터랙티브한 견본이 차지하는 영역입니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.
seo-description: 기본 보기 영역은 인터랙티브한 견본이 차지하는 영역입니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.
seo-title: 기본 뷰어 영역
solution: Experience Manager
title: 기본 뷰어 영역
topic: Dynamic media
uuid: 3e04c578-dcb2-4034-8809-dc949be80097
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---


# 기본 뷰어 영역{#main-viewer-area}

기본 보기 영역은 인터랙티브한 견본이 차지하는 영역입니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>뷰어의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>뷰어의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-ee18025b182a42dc98052de5f133ddfe}

흰색 배경( `#FFFFFF`)을 사용하여 뷰어를 설정하고 크기를 512 x 288픽셀로 설정하려면

```
.s7interactivevideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

