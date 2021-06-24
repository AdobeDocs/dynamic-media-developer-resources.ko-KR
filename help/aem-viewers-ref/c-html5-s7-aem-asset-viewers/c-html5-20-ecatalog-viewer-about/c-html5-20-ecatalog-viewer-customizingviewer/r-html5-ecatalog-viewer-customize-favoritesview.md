---
description: 즐겨찾기 보기는 축소판 이미지 열로 구성됩니다.
solution: Experience Manager
title: 즐겨찾기 보기
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---

# 즐겨찾기 보기{#favorites-view}

즐겨찾기 보기는 축소판 이미지 열로 구성됩니다.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

즐겨찾기 보기 컨테이너의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoritesview
```

즐겨찾기 보기의 위치와 높이는 뷰로 관리됩니다.css에서는 너비를 정의할 수만 있습니다.

**즐겨찾기 보기의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 즐겨찾기 보기의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>보기의 폭입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 반투명 회색 배경을 사용하여 가로 100픽셀인 즐겨찾기 보기를 설정합니다.

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

즐겨찾기 축소판 간의 간격은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**즐겨찾기 축소판의 CSS 속성**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 각 축소판 주위의 세로 여백 크기입니다. 실제 축소판 간격은 <span class="codeph"> .s7thumbcell </span>에 대해 설정된 위쪽 및 아래쪽 여백의 합계와 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 10픽셀 간격을 설정합니다.

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

개별 축소판의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**즐겨찾기 축소판의 CSS 속성**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>축소판의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>축소판의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>축소판의 테두리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>섬네일은 `state` 속성 선택기를 지원합니다. 이 선택기를 사용하면 다른 스킨(thumbnail states)을 다른 축소판 상태에 적용할 수 있습니다. 특히 `state="selected"`은 사용자가 최근에 선택한 축소판에 해당합니다. `state="default"` 축소판의 나머지 부분에 해당합니다. 및 `state="over"`은 마우스 가리키기에 사용됩니다.

예 - 75 x 75픽셀로 축소판을 설정하려면 밝은 회색의 기본 테두리와 어두운 회색으로 선택한 테두리를 사용합니다.

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

축소판 레이블의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**즐겨찾기 레이블의 CSS 속성**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 패밀리  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 14픽셀 Helvetica 글꼴로 레이블을 설정합니다.

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
