---
description: 텍스처 반복 모드. 대상 표면을 칠하기 위해 텍스처 이미지를 바둑판식으로 배열하는 방법을 지정합니다.
seo-description: 텍스처 반복 모드. 대상 표면을 칠하기 위해 텍스처 이미지를 바둑판식으로 배열하는 방법을 지정합니다.
seo-title: 반복
solution: Experience Manager
title: 반복
topic: Scene7 Image Serving - Image Rendering API
uuid: bd15a573-9902-4672-992d-90d171160a46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 19%

---


# 반복{#repeat}

텍스처 반복 모드. 대상 표면을 칠하기 위해 텍스처 이미지를 바둑판식으로 배열하는 방법을 지정합니다.

## 속성 {#section-cef4109cddf54ce095c3293d85bc412d}

열거형. 반복 가능한 텍스처에만 사용됩니다. 다른 모든 자료에 대해 무시됩니다.

반복 가능한 텍스처 재질에 대해 다음 값이 허용됩니다.

<table id="simpletable_C24FDA80A8AC431DA3FC86188E3774E1" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>0 </p></td> 
  <td class="- topic/stentry stentry"> <p>반복해 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>1 </p></td> 
  <td class="- topic/stentry stentry"> <p>4방향 임의 타일링 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>2 </p></td> 
  <td class="- topic/stentry stentry"> <p>8방향 임의 타일링 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>3 </p></td> 
  <td class="- topic/stentry stentry"> <p>다이아몬드 타일링. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>4 </p></td> 
  <td class="- topic/stentry stentry"> <p>1/4드롭 배경 무늬 표시 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>5 </p></td> 
  <td class="- topic/stentry stentry"> <p>셋드롭 벽지가 걸려 있습니다. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>6 </p></td> 
  <td class="- topic/stentry stentry"> <p>반쪽짜리 벽지가 걸려 있다. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>7 </p></td> 
  <td class="- topic/stentry stentry"> <p>5번째 벽지가 걸려 있다. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>8 </p></td> 
  <td class="- topic/stentry stentry"> <p>벽지를 뒤집으면 정지한다. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>9 </p></td> 
  <td class="- topic/stentry stentry"> <p>무작위 벽지가 멈춥니다. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>10 </p></td> 
  <td class="- topic/stentry stentry"> <p>임의 드롭. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>11 </p></td> 
  <td class="- topic/stentry stentry"> <p>무작위 범위 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>12 </p></td> 
  <td class="- topic/stentry stentry"> <p>반쪽입니다. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>13 </p></td> 
  <td class="- topic/stentry stentry"> <p>미러(북일치). </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>14 </p></td> 
  <td class="- topic/stentry stentry"> <p>표준 무작위 지정. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>15 </p></td> 
  <td class="- topic/stentry stentry"> <p>높은 주파수 무작위 추출기. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>16 </p></td> 
  <td class="- topic/stentry stentry"> <p>낮은 주파수 무작위 추출기. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>17 </p></td> 
  <td class="- topic/stentry stentry"> <p>수평 무작위 기호 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>18 </p></td> 
  <td class="- topic/stentry stentry"> <p>수직 무작위 기호 </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>19년 </p></td> 
  <td class="- topic/stentry stentry"> <p>가장자리 임의화 프로그램. </p></td> 
 </tr> 
</table>

## 기본값 {#section-23fba3bd1f3544c7913d12f2ca148517}

0(연속 반복).

## 참조 {#section-a08887a91db34ed3b183899c69c9f74f}

[반복=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8)
