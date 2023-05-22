---
description: 고급 텍스트 서식을 지정하려면 다음 명령을 사용하십시오.
solution: Experience Manager
title: 고급 텍스트 서식
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd0e94dc-34ce-4fc1-8d52-f8647c8312b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# 고급 텍스트 서식{#advanced-text-formatting}

고급 텍스트 서식을 지정하려면 다음 명령을 사용하십시오.

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span> </span> </td> 
   <td> <p>글꼴 크기를 변경하지 않고 아래 첨자로 표시합니다. </p> </td> 
   <td> <p>절반 포인트 위치. 기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span> </span> </td> 
   <td> <p>글꼴 크기를 변경하지 않은 위 첨자. </p> </td> 
   <td> <p>절반 포인트 위치. 기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \커닝 <span class="varname"> N </span> </span> </td> 
   <td> <p>지정된 글꼴 크기에서 비활성화/활성화. </p> </td> 
   <td> <p>커닝을 적용할 글꼴 크기(위 절반의 포인트), 커닝을 비활성화할 글꼴 크기(0), 절반 포인트 이상의 모든 글꼴 크기를 커닝할 경우 기본값은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>광학 커닝을 선택합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 만 해당. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>지표 커닝을 선택합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span> </span> </td> 
   <td> <p>문자 간격을 수정합니다. </p> </td> 
   <td> <p>양수 또는 음수 분기점. 기본값은 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expndtw <span class="varname"> N </span> </span> </td> 
   <td> <p>문자 간격을 수정합니다. </p> </td> 
   <td> <p>양 또는 음의 트윕. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span> </span> </td> 
   <td> <p>가로 문자 크기 조절. </p> </td> 
   <td> <p>양수 또는 음수 퍼센트. 기본값은 100입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span> </span> </td> 
   <td> <p>세로 문자 크기 조절. </p> </td> 
   <td> <p>양수 또는 음수 퍼센트, 기본값은 100, Dynamic Media 확장. </p> <p> <span class="codeph"> \charscaley </span> 를 적용할 때 선 간격의 배율도 조절됩니다. <span class="codeph"> text= </span>. <span class="codeph"> textPs= </span> 세로 문자 비율의 크기에 관계없이 항상 선 간격을 유지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>왼쪽에서 오른쪽 문자 흐름을 선택합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>오른쪽에서 왼쪽 문자 흐름을 선택합니다. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> 만 해당. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfit <span class="varname"> N </span> </span> </td> 
   <td> <p>복사 피팅을 활성화하고 허용된 최대 글꼴 크기를 설정합니다. </p> </td> 
   <td> <p>글꼴 크기(반점), <span class="codeph"> textPs= </span> 전용, Dynamic Media 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span> </span> </td> 
   <td> <p>최대 카피 맞춤 라인(소프트 제한). </p> </td> 
   <td> <p>라인 제한이 없는 경우 0 <span class="codeph"> textPs= </span> 전용, Dynamic Media 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span> </span> </td> 
   <td> <p>최대 복사 맞춤 선(자르기). </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 전용, Dynamic Media 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span> </span> </td> 
   <td> <p>문자 방향. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 전용, 로마자가 아닌 글꼴에서는 무시됨, <span class="codeph"> \stextflow1 </span> 이(가) 적용되지 않습니다. </p> <p>0 세로(기본값). </p> <p>1이 시계 방향으로 90도 회전했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
