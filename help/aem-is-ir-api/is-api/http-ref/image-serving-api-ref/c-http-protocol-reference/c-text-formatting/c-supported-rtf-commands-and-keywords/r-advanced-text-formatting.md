---
description: 고급 텍스트 서식을 지정하려면 다음 명령을 사용합니다.
seo-description: 고급 텍스트 서식을 지정하려면 다음 명령을 사용합니다.
seo-title: 고급 텍스트 서식
solution: Experience Manager
title: 고급 텍스트 서식
topic: Scene7 Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 고급 텍스트 서식{#advanced-text-formatting}

고급 텍스트 서식을 지정하려면 다음 명령을 사용합니다.

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
   <td> <span class="codeph"> \dn <span class="varname"> N </span></span> </td> 
   <td> <p>글꼴 크기가 변경되지 않은 Subscript </p> </td> 
   <td> <p>1/2 포인트 위치;기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up <span class="varname"> N </span></span> </td> 
   <td> <p>글꼴 크기가 변경되지 않은 위 첨자 </p> </td> 
   <td> <p>1/2 포인트 위치;기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning <span class="varname"> N </span></span> </td> 
   <td> <p>지정된 글꼴 크기로 비활성화/활성화합니다. </p> </td> 
   <td> <p>커닝을 적용할 글꼴 크기(반점)0 - 커닝을 사용하지 않도록 설정기본값은 1(1/2포인트 이상 모든 글꼴 크기 커닝)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningoptical </span> </td> 
   <td> <p>시각적 커닝을 선택합니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 전용입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerningmetric </span> </td> 
   <td> <p>지표 커닝을 선택합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expnd <span class="varname"> N </span></span> </td> 
   <td> <p>문자 간격을 수정합니다. </p> </td> 
   <td> <p>긍정 또는 부정 분기 포인트;기본값은 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expandtw <span class="varname"> N </span></span> </td> 
   <td> <p>문자 간격을 수정합니다. </p> </td> 
   <td> <p>양수 또는 음수 트위프. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex <span class="varname"> N </span></span> </td> 
   <td> <p>가로 문자 크기 조절. </p> </td> 
   <td> <p>긍정적 또는 부정적 퍼센트;기본값은 100입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley <span class="varname"> N </span></span> </td> 
   <td> <p>세로 문자 크기 조절. </p> </td> 
   <td> <p>긍정적 또는 부정적 퍼센트;기본값은 100입니다.Scene7 확장. </p> <p> <span class="codeph"> \charscaley </span> 는 <span class="codeph"> text=로 적용할 때 행 간격의 크기를 조절할 </span>수도 있습니다. <span class="codeph"> textPs= </span> 세로 문자 크기 조절에 상관없이 항상 줄 간격을 유지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch </span> </td> 
   <td> <p>왼쪽에서 오른쪽 문자 흐름을 선택합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch </span> </td> 
   <td> <p>오른쪽에서 왼쪽으로 쓰는 문자 흐름을 선택합니다. </p> </td> 
   <td> <p> <span class="codeph"> text= </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \자동 맞춤 <span class="varname"> N </span></span> </td> 
   <td> <p>복사 맞춤을 활성화하고 허용되는 최대 글꼴 크기를 설정합니다. </p> </td> 
   <td> <p>글꼴 크기(1/2 포인트); <span class="codeph"> textPs= </span> only;Scene7 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines <span class="varname"> N </span></span> </td> 
   <td> <p>최대 자동 맞춤 라인(소프트 제한). </p> </td> 
   <td> <p>0(라인 제한 없음) <span class="codeph"> textPs= </span> only;Scene7 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines <span class="varname"> N </span></span> </td> 
   <td> <p>최대 자동 맞춤 선(자른 선)입니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;Scene7 확장. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir <span class="varname"> N </span></span> </td> 
   <td> <p>문자 방향. </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> only;non-Roman 글꼴에 대해 무시됨;\stextflow1 <span class="codeph"> 이 </span> 적용되지 않으면 무시됩니다. </p> <p>0 세로(기본값). </p> <p>시계 방향으로 90도 회전한 1개. </p> </td> 
  </tr> 
 </tbody> 
</table>

