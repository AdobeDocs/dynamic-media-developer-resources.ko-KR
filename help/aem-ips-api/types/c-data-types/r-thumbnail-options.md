---
description: 축소판 이미지로 사용할 특정 비디오 프레임을 선택할 수 있는 선택적 유형입니다.
solution: Experience Manager
title: 축소판 옵션
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 5%

---


# ThumbnailOptions{#thumbnailoptions}

축소판 이미지로 사용할 특정 비디오 프레임을 선택할 수 있는 선택적 유형입니다.

구문

## 매개 변수 {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>비디오 축소판에 사용할 프레임에 대한 시간(비디오 시작 후 밀리초)을 설정합니다. 값은 0부터 비디오 끝까지의 범위입니다. <p>참고:시간을 잘못 지정하면 축소판의 비디오 첫 번째 프레임이 사용됩니다. <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>을 참조하십시오. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

