---
description: 다음 단락 서식 명령이 지원됩니다.
solution: Experience Manager
title: 단락 서식
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 단락 서식{#paragraph-formatting}

다음 단락 서식 명령이 지원됩니다.

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
   <td> <p>단락 서식을 기본값으로 다시 설정합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>텍스트를 왼쪽으로 정렬합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>텍스트를 오른쪽으로 정렬합니다. </p> </td> 
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
   <td> <p> <span class="codeph"> textPs= </span>만 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>단락의 마지막 줄을 왼쪽으로 정렬합니다. </p> </td> 
   <td> <p>기본값; <span class="codeph"> textPs= </span>만; <span class="codeph"> \qj </span>이(가) 활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>양쪽 정렬된 단락의 마지막 줄을 오른쪽으로 정렬합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>만; <span class="codeph"> \qj </span>이(가) 활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>균등 배치된 단락의 마지막 줄을 가운데로 맞춥니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>만; <span class="codeph"> \qj </span>이(가) 활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>균등 배치된 단락의 마지막 줄을 확인(늘리기)합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>만; <span class="codeph"> \qj </span>이(가) 활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>첫 줄 들여쓰기입니다. </p> </td> 
   <td> <p>트윕; <span class="codeph"> textPs= </span>만. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>왼쪽 들여쓰기. </p> </td> 
   <td> <p>트윕; <span class="codeph"> textPs= </span>만. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>오른쪽 들여쓰기. </p> </td> 
   <td> <p>트윕; <span class="codeph"> textPs= </span>만. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>줄 사이 간격. </p> </td> 
   <td> <p>자동 라인 간격의 경우 0(기본값), 기본 라인 간격보다 큰 경우에만 값을 사용하려면 양수 값, 강제 간격의 경우 음수 값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>라인 간격 여러 플래그. </p> </td> 
   <td> <p><span class="codeph"> \sl </span>이(가) 트윕 단위인 경우 0(기본값)으로 설정하고 <span class="codeph"> \sl </span>이(가) 기본 간격의 배수인 경우 1로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>단락 앞에 추가 공백이 있습니다. </p> </td> 
   <td> <p>트윕; <span class="codeph"> text= </span>이(가) 텍스트 상자의 첫 번째 단락에 <span class="codeph"> \sb </span>을(를) 적용하지만 <span class="codeph"> textPs= </span>은(는) 적용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>단락 뒤에 추가 공백이 있습니다. </p> </td> 
   <td> <p>트윕; <span class="codeph"> text= </span>은(는) 텍스트 상자의 마지막 단락에 <span class="codeph"> \sa </span>을(를) 적용하지만 <span class="codeph"> textPs= </span>은(는) 적용되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
