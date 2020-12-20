---
description: 비디오 뷰어용 URL 명령.
seo-description: 비디오 뷰어용 URL 명령.
seo-title: 캡션
solution: Experience Manager
title: 캡션
topic: Dynamic media
uuid: 670d83c2-bfc5-411a-8581-5103a62aa8cf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 11%

---


# caption{#caption}

비디오 뷰어용 URL 명령.

` caption= *`파일`*[,0|1]`

뷰어는 호스팅되는 WebVTT 파일을 통한 자막을 지원합니다. 겹치는 큐 및 영역은 지원되지 않습니다. 지원되는 큐 위치 지정 연산자는 다음과 같습니다.

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
   <td colname="col3"> <p><span class="codeph"> 왼쪽|오른쪽|가운데|시작|끝</span> </p> </td> 
   <td colname="col4"> <p> 텍스트 정렬을 제어할 수 있습니다. </p> <p>기본값은 <span class="codeph"> middle</span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>텍스트 위치 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 캡션 텍스트 시작 부분에 대한 VideoPlayer 구성 요소에 삽입된 인세트 비율입니다. </p> <p>기본값은 0입니다%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>선 크기 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 캡션에 사용되는 비디오 너비의 비율입니다. </p> <p>기본값은 100입니다%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>선 위치 </p> </td> 
   <td colname="col3"> <p> 0%-100%|정수 </p> </td> 
   <td colname="col4"> <p> 페이지의 라인 위치를 결정합니다. </p> <p>숫자 값이 정수(퍼센트 기호 없음)로 표현되는 경우 텍스트가 표시되는 맨 위의 줄 수입니다. </p> <p>백분율인 경우(백분율 기호는 마지막 문자임), 캡션 텍스트가 표시 영역 아래쪽의 백분율로 표시됩니다. </p> <p>기본값은 100입니다%. </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT 파일에 있는 다른 WebVTT 기능은 지원되지 않지만 캡션을 방해해서는 안 됩니다.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 파일</span></span> </p> </td> 
   <td colname="col2"> <p> WebVTT 캡션 내용의 URL 또는 경로를 지정합니다. ImageServing을 통해 WebVTT 파일을 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 기본 캡션 상태를 지정합니다(활성화됨: <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

없음.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```

