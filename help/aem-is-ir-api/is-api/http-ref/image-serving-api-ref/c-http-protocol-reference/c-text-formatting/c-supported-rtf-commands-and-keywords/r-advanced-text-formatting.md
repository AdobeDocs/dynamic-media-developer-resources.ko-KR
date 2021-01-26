---
description: 고급 텍스트 서식에 다음 명령을 사용합니다.
seo-description: 고급 텍스트 서식에 다음 명령을 사용합니다.
seo-title: 고급 텍스트 서식 지정
solution: Experience Manager
title: 고급 텍스트 서식 지정
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 340166a5-5aef-4081-9114-a715cde68891
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 1%

---


# 고급 텍스트 서식 지정{#advanced-text-formatting}

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
   <td> <p>글꼴 크기가 변경되지 않은 서브스크립트 </p> </td> 
   <td> <p>50% 포인트 위치;기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \up  <span class="varname"> N  </span> </span> </td> 
   <td> <p>글꼴 크기가 변경되지 않은 위 첨자 </p> </td> 
   <td> <p>50% 포인트 위치;기본값은 6입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \kerning  <span class="varname"> N  </span> </span> </td> 
   <td> <p>지정된 글꼴 크기로 비활성화/활성화합니다. </p> </td> 
   <td> <p>커닝을 적용할 글꼴 크기(반점)0 - 커닝을 사용하지 않도록 설정합니다.기본값은 1/2포인트 위의 모든 글꼴 크기를 커닝하는 경우 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ker닝광  </span> </td> 
   <td> <p>시각적 커닝을 선택합니다. </p> </td> 
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
   <td> <p>긍정적 또는 부정적 분기 포인트;기본값은 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \expandtw  <span class="varname"> N  </span> </span> </td> 
   <td> <p>문자 간격을 수정합니다. </p> </td> 
   <td> <p>긍정적 또는 부정적 트윗입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscalex  <span class="varname"> N  </span> </span> </td> 
   <td> <p>가로 문자 크기 조절. </p> </td> 
   <td> <p>긍정적 또는 부정적 퍼센트;기본값은 100입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \charscaley  <span class="varname"> N  </span> </span> </td> 
   <td> <p>세로 문자 비율. </p> </td> 
   <td> <p>긍정적 또는 부정적 퍼센트;기본값은 100입니다.Dynamic Media 확장 </p> <p> <span class="codeph"> \charscaley는  </span> text=와 함께 적용할 때  <span class="codeph"> 행 간격도  </span>조정합니다. <span class="codeph"> textPs= </span> 는 세로 문자 비율 조정 양에 상관없이 항상 행 간격을 유지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ltrch  </span> </td> 
   <td> <p>왼쪽에서 오른쪽 문자 흐름을 선택합니다. </p> </td> 
   <td> <p>기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \rtlch  </span> </td> 
   <td> <p>오른쪽에서 왼쪽으로 문자 흐름을 선택합니다. </p> </td> 
   <td> <p> <span class="codeph"> text=  </span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \자동맞춤  <span class="varname"> N  </span> </span> </td> 
   <td> <p>복사 맞춤을 활성화하고 허용되는 최대 글꼴 크기를 설정합니다. </p> </td> 
   <td> <p>글꼴 크기(반점);<span class="codeph"> textPs= </span> 전용;Dynamic Media 확장 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>최대 복사 맞춤 선(소프트 제한). </p> </td> 
   <td> <p>0(라인 제한 없음)<span class="codeph"> textPs= </span> 전용;Dynamic Media 확장 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \copyfitmaxlines  <span class="varname"> N  </span> </span> </td> 
   <td> <p>최대 복사 맞춤 선(자르기)입니다. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;Dynamic Media 확장 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \baselinedir  <span class="varname"> N  </span> </span> </td> 
   <td> <p>문자 방향. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only;로마자 이외의 글꼴에 대해 무시됨;\stextflow1 <span class="codeph"> 이  </span> 적용되지 않는 경우 무시됩니다. </p> <p>0 세로(기본값). </p> <p>시계 방향으로 90도 회전한 1개. </p> </td> 
  </tr> 
 </tbody> 
</table>

