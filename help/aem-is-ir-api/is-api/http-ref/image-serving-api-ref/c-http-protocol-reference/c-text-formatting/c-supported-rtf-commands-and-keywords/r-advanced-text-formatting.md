---
description: 고급 텍스트 서식에 다음 명령을 사용합니다.
solution: Experience Manager
title: 고급 텍스트 서식
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---

# 고급 텍스트 서식{#advanced-text-formatting}

고급 텍스트 서식에 다음 명령을 사용합니다.

<table id="table_43B2EB887C0F471BB60C23B570E7D3D2"> 
 <thead> 
  <tr> 
   <th class="entry"> 명령 </th> 
   <th class="entry"> 설명 </th> 
   <th class="entry"> 주의 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \dn  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴 크기가 변경되지 않은 하위 스크립트입니다. </p> </td> 
   <td> <p>50%의 위치에 배치합니다.기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴 크기가 변경되지 않은 위 첨자 </p> </td> 
   <td> <p>50%의 위치에 배치합니다.기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>지정된 글꼴 크기로 사용 안 함/사용 안 함 </p> </td> 
   <td> <p>커닝을 적용할 반점 위의 글꼴 크기0: 커닝을 사용하지 않도록 설정합니다.기본값은 1(1/2포인트 이상 모든 글꼴 크기 커닝에 대해) 입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningopy  </span> </td> 
   <td> <p>광학 커닝을 선택합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric  </span> </td> 
   <td> <p>지표 커닝을 선택합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd  <span class="varname"> N  </span> </span> </td> 
   <td> <p>문자 간격을 수정합니다. </p> </td> 
   <td> <p>양수 또는 음수 1/4포인트;기본값은 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expandtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>문자 간격을 수정합니다. </p> </td> 
   <td> <p>양수 또는 음수 돌풍. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>가로 문자 크기 조절. </p> </td> 
   <td> <p>양수 또는 음수 퍼센트.기본값은 100입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>세로 문자 비율 조정. </p> </td> 
   <td> <p>양수 또는 음수 퍼센트.기본값은 100입니다.Dynamic Media 확장. </p> <p> <span class="codeph"> \charscaley </span> 는  <span class="codeph"> text=  </span>로 적용할 때 줄 간격도 조정됩니다. <span class="codeph"> textPs= </span> 는 세로 문자 크기 조절에 관계없이 항상 줄 간격을 유지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>왼쪽에서 오른쪽 문자 흐름을 선택합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>오른쪽에서 왼쪽 쓰기 문자 흐름을 선택합니다. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> 전용. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit  <span class="varname"> N  </span> </span> </td> 
   <td> <p>복사 피팅을 활성화하고 최대 허용 글꼴 크기를 설정합니다. </p> </td> 
   <td> <p>글꼴 크기(반점);<span class="codeph"> textPs= </span> 전용;Dynamic Media 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>최대 복사/맞춤 선(소프트 제한). </p> </td> 
   <td> <p>0(라인 제한 없음)<span class="codeph"> textPs= </span> 전용;Dynamic Media 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>최대 복사/맞춤 라인(자르기) </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용;Dynamic Media 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>문자 방향. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> 전용;비로마자 글꼴에 대해 무시됩니다.\stextflow1 <span class="codeph"> 이  </span> 적용되지 않으면 무시됩니다. </p> <p>0개 세로(기본값) </p> <p>시계 방향으로 1도 회전했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
