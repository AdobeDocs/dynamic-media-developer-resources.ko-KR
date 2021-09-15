---
title: 캡션
description: 모든 뷰어에 공통되는 매개 변수.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 6%

---

# 캡션{#caption}

모든 뷰어에 공통되는 매개 변수.

>[!NOTE]
>
>이 명령은 비디오 이미지 뷰어에는 적용되지 않습니다.

` caption= *`파일`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 파일  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT 캡션 콘텐츠의 URL 또는 경로를 지정합니다. 이미지 제공 기능이 WebVTT 파일을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 기본 캡션 상태를 지정합니다. 활성화됨 은 <span class="codeph"> 1 </span>입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

이 뷰어는 호스팅된 WebVTT 파일을 통해 자막을 지원합니다. 이 매개 변수로 지정된 캡션은 미디어 세트에서 먼저 오는 비디오에 적용됩니다. 이후 비디오에서는 캡션 없이 재생됩니다. 겹치는 큐 및 영역은 지원되지 않습니다. 지원되는 큐 포지셔닝 연산자:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>키 </p> </th> 
   <th colname="col2" class="entry"> <p>이름 </p> </th> 
   <th colname="col3" class="entry"> <p>값 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>테스트 정렬 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 왼쪽|오른쪽|가운데|시작|끝  </span> </p> </td> 
   <td colname="col4"> <p> 텍스트 정렬을 제어합니다. </p> <p>기본값은 <span class="codeph"> 중간 </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>텍스트 위치 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 캡션 텍스트의 시작 부분에 대한 VideoPlayer 구성 요소에 대한 inset 비율입니다. </p> <p>기본값은 <span class="codeph"> 0% </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>선 크기 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 캡션에 사용되는 비디오 너비의 비율입니다. </p> <p>기본값은 <span class="codeph"> 100% </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>선 위치 </p> </td> 
   <td colname="col3"> <p> 0%-100%|정수 </p> </td> 
   <td colname="col4"> <p> 페이지에서 라인 위치를 결정합니다. </p> <p>퍼센트 기호가 없는 정수로 표시되는 경우 텍스트가 표시되는 맨 위의 라인 수입니다. </p> <p>백분율로 표현되는 경우 - 퍼센트 기호가 마지막 문자이고 표시 영역 아래쪽의 백분율 기호가 표시됩니다. </p> <p>기본값은 <span class="codeph"> 100% </span>입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT 파일 내에 다른 WebVTT 기능이 있는 경우 지원되지 않습니다. 그러나 캡션을 중단하지 않습니다.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 파일  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT 캡션 콘텐츠의 URL 또는 경로를 지정합니다. WebVTT 파일은 이미지 제공에서 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 기본 캡션 상태를 지정합니다. </p> <p>활성화됨 은 <span class="codeph"> 1 </span>입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

선택 사항입니다.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

없음.

## 예 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
