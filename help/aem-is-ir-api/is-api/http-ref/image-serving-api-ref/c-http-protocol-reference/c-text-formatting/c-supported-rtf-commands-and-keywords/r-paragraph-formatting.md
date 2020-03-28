---
description: 다음 단락 서식 지정 명령이 지원됩니다.
seo-description: 다음 단락 서식 지정 명령이 지원됩니다.
seo-title: 단락 서식
solution: Experience Manager
title: 단락 서식
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 단락 서식{#paragraph-formatting}

다음 단락 서식 지정 명령이 지원됩니다.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>명령 </p> </th> 
   <th class="entry"> <p>설명 </p> </th> 
   <th class="entry"> <p>주의 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>단락 서식을 기본값으로 재설정합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>텍스트를 왼쪽으로 정렬합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>텍스트를 오른쪽으로 정렬할 수 있습니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>텍스트를 가로로 가운데로 맞춥니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>텍스트를 가로로 양쪽 정렬합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>단락의 마지막 줄을 왼쪽으로 정렬합니다. </p> </td> 
   <td> <p>기본값; <span class="codeph"> textPs= </span> only;\ <span class="codeph"> qj가 </span>활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>양쪽 정렬된 단락의 마지막 줄을 오른쪽 정렬합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;\qj <span class="codeph"> 가 활성화되지 않은 경우 </span> 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>양쪽 정렬된 단락의 마지막 줄을 가운데로 맞춥니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;\ <span class="codeph"> qj가 </span>활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>양쪽 정렬된 단락의 마지막 줄을 일시 중단(늘이기)합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;\ <span class="codeph"> qj가 </span>활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span></span> </td> 
   <td> <p>첫 줄 들여쓰기 </p> </td> 
   <td> <p>트위프;textPs <span class="codeph"> = </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span></span> </td> 
   <td> <p>왼쪽 들여쓰기 </p> </td> 
   <td> <p>트위프;textPs <span class="codeph"> = </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span></span> </td> 
   <td> <p>오른쪽 들여쓰기 </p> </td> 
   <td> <p>트위프;textPs <span class="codeph"> = </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span></span> </td> 
   <td> <p>줄 사이의 간격. </p> </td> 
   <td> <p>0(기본값) - 자동 줄 간격양수 값을 사용하여 기본 줄 간격보다 큰 경우에만 값을 사용할 수 있습니다.음수 값을 사용하여 공간을 강제 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span></span> </td> 
   <td> <p>줄 간격 다중 플래그. </p> </td> 
   <td> <p>\sl이 <span class="codeph"> 두 </span> 번 있는 경우 0(기본값)으로 설정하고, \sl <span class="codeph"> 이 기본 간격의 배수인 경우 </span> 1로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span></span> </td> 
   <td> <p>단락 앞에 추가 공백이 있습니다. </p> </td> 
   <td> <p>트위프;텍스트 <span class="codeph"> = \sb </span>가 텍스트 상자의 첫 번째 단락에 <span class="codeph"> 적용되지만 </span> textPs= <span class="codeph"> </span> 적용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span></span> </td> 
   <td> <p>단락 뒤에 추가 공백이 있습니다. </p> </td> 
   <td> <p>트위프;text= <span class="codeph"></span> 텍스트 상자의 마지막 단락에 \sa <span class="codeph"> 가 적용되지만 </span> textPs= <span class="codeph"> </span> 는 적용되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

