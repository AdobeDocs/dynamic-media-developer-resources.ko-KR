---
title: 즐겨찾기 보기
description: 즐겨찾기 보기는 썸네일 이미지 열로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---

# 즐겨찾기 보기{#favorites-view}

즐겨찾기 보기는 썸네일 이미지 열로 구성됩니다.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

다음 CSS 클래스 선택기를 사용하여 즐겨찾기 보기 컨테이너의 모양이 제어됩니다.

```
.s7ecatalogsearchviewer .s7favoritesview
```

즐겨찾기 보기의 위치 및 높이는 보기에서 관리됩니다. CSS에서는 너비만 정의할 수 있습니다.

**즐겨찾기 보기의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 즐겨찾기 보기의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>보기의 폭입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 반투명 회색 배경이 있는 100픽셀 너비의 즐겨찾기 보기를 설정합니다.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

즐겨찾기 썸네일 간의 간격은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**즐겨찾기 썸네일의 CSS 속성**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 각 썸네일 주변의 세로 여백 크기입니다. 실제 썸네일 간격은 에 대해 설정된 위쪽 및 아래쪽 여백의 합과 같습니다. <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 10개의 픽셀 간격을 설정합니다.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

개별 썸네일의 모양은 다음 CSS 클래스 선택기로 제어합니다.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**즐겨찾기 썸네일의 CSS 속성**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>썸네일은 `state` 속성 선택기: 다른 썸네일 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히, `state="selected"` 사용자가 최근에 선택한 썸네일에 해당합니다. While `state="default"` 은 나머지 썸네일에 해당합니다. 및 `state="over"` 마우스를 가리킬 때 사용됩니다.

예 - 75 x 75픽셀인 썸네일을 설정하려면 밝은 회색의 기본 테두리와 어두운 회색의 선택된 테두리를 사용합니다.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

썸네일 레이블의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**즐겨찾기 레이블의 CSS 속성**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 패밀리 </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 14픽셀 Helvetica® 글꼴로 레이블을 설정합니다.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
