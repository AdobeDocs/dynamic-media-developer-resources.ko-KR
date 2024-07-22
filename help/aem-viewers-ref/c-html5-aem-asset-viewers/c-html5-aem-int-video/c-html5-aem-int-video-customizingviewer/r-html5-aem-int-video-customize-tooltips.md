---
title: 툴팁
description: 데스크탑 시스템에서는 버튼과 같은 일부 사용자 인터페이스 요소에 마우스 가리키기에 표시되는 툴팁이 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 430809d8-3d51-49b7-b6bf-c3c3c77501ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---

# 툴팁{#tooltips}

데스크탑 시스템에서는 버튼과 같은 일부 사용자 인터페이스 요소에 마우스 가리키기에 표시되는 툴팁이 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

도구 설명의 모양은 다음 CSS 클래스 선택기를 사용하여 제어합니다.

```
.s7tooltip
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
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 배경 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> 배경 테두리 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>포함 웹 페이지 내에서 도구 설명 스타일을 사용자 지정하는 경우 모든 속성에 `!IMPORTANT` 규칙이 포함되어야 합니다. 뷰어의 CSS 파일 내에서 도구 설명을 사용자 지정하는 경우에는 이 참고 사항이 필요하지 않습니다.

## 예 {#section-59e009fd05b14019936aba04d7ca779d}

회색 테두리에 Arial®의 3픽셀 모퉁이 반경, 검정색 배경 및 흰색 텍스트가 있는 도구 설명을 설정하려면 11픽셀로 하십시오.

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
