---
title: 캡션
description: 스마트 자르기 비디오 뷰어에 대한 URL 명령입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d7000d0-9181-4c6e-a94e-31ab5ad17fa4
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 11%

---

# 캡션{#caption}

스마트 자르기 비디오 뷰어에 대한 URL 명령입니다.

` caption= *`파일`*[,0|1]`

뷰어는 호스팅된 WebVTT 파일을 통해 폐쇄 캡션을 지원합니다. 겹치는 큐와 영역은 지원되지 않습니다. 지원되는 큐 위치 지정 연산자에는 다음이 포함됩니다.

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
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
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>텍스트 정렬 </p> </td> 
   <td colname="col3"> <p><span class="codeph"> 왼쪽|오른쪽|중간|시작|종료</span> </p> </td> 
   <td colname="col4"> <p> 텍스트 맞춤을 제어합니다. </p> <p>기본값은 입니다 <span class="codeph"> 가운데</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>텍스트 위치 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 캡션 텍스트 시작 부분에 대한 VideoPlayer 구성 요소에 삽입되는 비율입니다. </p> <p>기본값은 0입니다%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>선 크기 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 캡션에 사용되는 비디오 너비의 백분율입니다. </p> <p>기본값은 100입니다%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>라인 위치 </p> </td> 
   <td colname="col3"> <p> 0%-100%|정수 </p> </td> 
   <td colname="col4"> <p> 페이지의 라인 위치를 결정합니다. </p> <p>정수(퍼센트 기호 없음)로 표시되는 경우 텍스트가 표시되는 위쪽의 줄 수입니다. </p> <p>백분율(퍼센트 기호가 마지막 문자)이면 표시 영역 아래에 해당 백분율로 캡션 텍스트가 표시됩니다. </p> <p>기본값은 100입니다%. </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT 파일에 있는 다른 WebVTT 기능은 지원되지 않지만 캡션을 중단해서는 안 됩니다.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 파일</span></span> </p> </td> 
   <td colname="col2"> <p> WebVTT 캡션 컨텐츠의 URL 또는 경로를 지정합니다. ImageServing에서 WebVTT 파일을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 기본 캡션 상태를 지정합니다(활성화됨: <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택적.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
