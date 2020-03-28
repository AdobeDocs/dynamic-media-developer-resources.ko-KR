---
description: 표준 경고는 구성된 평균 간격이 끝날 때 통합 이메일 메시지와 함께 전송됩니다.
seo-description: 표준 경고는 구성된 평균 간격이 끝날 때 통합 이메일 메시지와 함께 전송됩니다.
seo-title: 표준 경고
solution: Experience Manager
title: 표준 경고
topic: Scene7 Image Serving - Image Rendering API
uuid: d3294434-a44b-4742-9d77-a6945760d33c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 표준 경고{#standard-alerts}

표준 경고는 구성된 평균 간격이 끝날 때 통합 이메일 메시지와 함께 전송됩니다.

다음 표에서는 각 유형의 표준 경고를 설명합니다.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>경고 유형</b> </th> 
   <th class="entry"> <b>제목 ID</b> </th> 
   <th class="entry"> <b>설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>잠긴 요청 </p> </td> 
   <td> <p>잠금 </p> </td> 
   <td> <p>요청이 지정된 임계값 내에서 클라이언트에 대한 응답을 반환하지 못할 때 전송됩니다. 대기 중인 요청을 나타낼 수 있으며, 이로 인해 Java 스레드 풀이 감소될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>높은 동시 시청 </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> 동시에 처리되는 요청 수( <i>겹침</i>)가 지정된 임계값을 초과할 때 발생합니다. 서버 오버로드 조건을 나타낼 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td> <p>최소 트래픽 </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>전체 요청 비율이 지정된 임계값 아래로 떨어질 때 생성됩니다. 일반적으로 서버 통신 문제를 나타냅니다(예: 서버가 오프라인으로 이동하는 경우). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>오류 비율 </p> </td> 
   <td> <p>오류 </p> </td> 
   <td> <p>샘플링 간격 동안의 평균 HTTP 오류 응답 비율이 지정된 임계값을 초과할 때 발생합니다. 구성 문제, 이미지 누락, 웹 사이트 프로그래밍 또는 데이터베이스 오류를 나타낼 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>응답 시간 </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>샘플링 간격 동안의 평균 요청 처리 시간이 지정된 임계값 이상으로 증가할 때 전송됩니다. 일반적으로 서버 또는 백엔드 이미지 스토리지 시스템의 임시 또는 지속적인 오버로드 상태를 나타냅니다. </p> <p>평균 응답 시간을 계산할 때 오류 응답은 고려되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

