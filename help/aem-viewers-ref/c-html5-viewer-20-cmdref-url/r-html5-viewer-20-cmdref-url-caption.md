---
description: 모든 뷰어에 공통되는 매개 변수입니다.
solution: Experience Manager
title: 캡션
feature: Dynamic Media Classic,뷰어,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 6%

---


# caption{#caption}

모든 뷰어에 공통되는 매개 변수입니다.

>[!NOTE]
>
>이 명령은 비디오 이미지 뷰어에 적용되지 않습니다.

` caption= *`파일`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 파일  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT 캡션 내용의 URL 또는 경로를 지정합니다. 이미지 제공은 WebVTT 파일을 지원합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 기본 캡션 상태를 지정합니다. 활성화됨: <span class="codeph"> 1 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

이 뷰어는 호스팅되는 WebVTT 파일을 통해 자막을 지원합니다. 이 매개 변수로 지정된 캡션은 미디어 세트에서 먼저 오는 비디오에 적용됩니다.후속 비디오에서는 캡션 없이 재생됩니다. 겹치는 큐 및 영역은 지원되지 않습니다. 지원되는 큐 위치 지정 연산자:

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
   <td colname="col4"> <p> 텍스트의 정렬을 제어합니다. </p> <p>기본값은 <span class="codeph"> 중간 </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>텍스트 위치 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 캡션 텍스트 시작 부분에 대한 VideoPlayer 구성 요소에 삽입된 인세트 비율입니다. </p> <p>기본값은 <span class="codeph"> 0% </span>입니다. </p> </td> 
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
   <td colname="col4"> <p> 페이지의 라인 위치를 결정합니다. </p> <p>백분율 기호가 없는 정수로 표현되는 경우 텍스트가 표시되는 맨 위의 줄 수입니다. </p> <p>백분율로 표현되는 경우 - 백분율 기호가 마지막 문자인 경우 캡션 텍스트가 표시 영역 아래에 백분율로 표시됩니다. </p> <p>기본값은 <span class="codeph"> 100% </span>입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

WebVTT 파일에 다른 WebVTT 기능이 있는 경우에는 지원되지 않습니다.그러나 캡션을 방해하지는 않습니다.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 파일  </span> </span> </p> </td> 
   <td colname="col2"> <p> WebVTT 캡션 내용의 URL 또는 경로를 지정합니다. WebVTT 파일은 이미지 제공에서 제공됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 기본 캡션 상태를 지정합니다. </p> <p>활성화됨: <span class="codeph"> 1 </span> </p> </td> 
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

