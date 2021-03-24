---
description: 다음 단락 서식 지정 명령이 지원됩니다.
solution: Experience Manager
title: 단락 서식
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

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
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>단락 서식을 기본값으로 재설정합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sql  </span> </td> 
   <td> <p>텍스트를 왼쪽으로 정렬합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>텍스트를 오른쪽으로 정렬합니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>텍스트를 가로로 가운데로 정렬합니다. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>텍스트를 가로로 양쪽 정렬합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>단락의 마지막 줄을 왼쪽으로 정렬합니다. </p> </td> 
   <td> <p>기본값;<span class="codeph"> textPs= </span> 전용;<span class="codeph"> \qj </span>이(가) 활성화되지 않은 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>양쪽 정렬된 단락의 마지막 줄을 오른쪽 정렬합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;\ <span class="codeph"> qj가 활성 상태가  </span> 아닌 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>양쪽 정렬된 단락의 마지막 줄을 가운데로 정렬합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;\ <span class="codeph"> qj가 활성 상태가  </span>아닌 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>정당화된 단락의 마지막 줄을 일시 중단(스트레치)합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;\ <span class="codeph"> qj가 활성 상태가  </span>아닌 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>첫 줄 들여쓰기. </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>만 해당. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>왼쪽 들여쓰기. </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>만 해당. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>오른쪽 들여쓰기. </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>만 해당. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>선 사이의 간격. </p> </td> 
   <td> <p>0(기본값)(자동 행 간격)값을 기본 행 간격보다 큰 경우에만 사용할 수 있는 양의 값입니다.음수 값을 사용하여 공간을 강제 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>여러 플래그를 줄별로 지정할 수 있습니다. </p> </td> 
   <td> <p><span class="codeph"> \sl </span>이 트위프인 경우 0(기본값), <span class="codeph"> \sl </span>이 기본 간격의 배수인 경우 1로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>단락 앞에 추가 공백이 있습니다. </p> </td> 
   <td> <p>Twips;<span class="codeph"> text= </span>이(가) 텍스트 상자의 첫 번째 단락에 <span class="codeph"> \sb </span>을(를) 적용하지만 <span class="codeph"> textPs= </span>은(는) 적용하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>단락 뒤에 추가 공백이 있습니다. </p> </td> 
   <td> <p>Twips;<span class="codeph"> text= </span>이(가) 텍스트 상자의 마지막 단락에 <span class="codeph"> \sa </span>을(를) 적용하지만 <span class="codeph"> textPs= </span>은(는) 적용되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

