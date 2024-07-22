---
description: 썸네일 이미지로 사용할 특정 비디오 프레임을 선택할 수 있는 선택적 유형입니다.
solution: Experience Manager
title: 썸네일 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

썸네일 이미지로 사용할 특정 비디오 프레임을 선택할 수 있는 선택적 유형입니다.

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
   <td colname="col3"> <p>비디오 썸네일에 사용할 프레임의 시간(비디오 시작부터 밀리초)을 설정합니다. 값의 범위는 0부터 비디오 끝까지 입니다. <p>참고: 시간을 잘못 지정하면 썸네일에 대해 비디오의 첫 번째 프레임이 사용됩니다. <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>을(를) 참조하십시오. </p></p> </td> 
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
