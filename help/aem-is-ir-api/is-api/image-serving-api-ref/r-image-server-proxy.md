---
description: 영상 서버 프록시는 일본 전화기의 이미지 크기를 조정하는 데 사용될 수 있다.
solution: Experience Manager
title: 이미지 서버 프록시
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# 이미지 서버 프록시{#image-server-proxy}

영상 서버 프록시는 일본 전화기의 이미지 크기를 조정하는 데 사용될 수 있다.

## URL 형식 {#section-2e8c40b0547c4f99874cdf502b338940}

IS 프록시의 URL 형식은 일반 IS 요청과 매우 유사합니다. 프록시에 전달된 모든 IS 수정자가 이미지 서버로 전달됩니다. IS 수정자에 대한 정보는 [HTTP 프로토콜 참조](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 프록시 관련 수정자 목록 {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>이미지 너비로 사용할 장치의 사용 가능한 너비의 비율을 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>이미지 높이로 사용할 장치의 사용 가능한 높이 비율을 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>응답 크기를 제한할 장치의 메모리 제한 포함 미디어 속성의 비율을 지정합니다. jpg 응답에만 적용됩니다. 응답 크기가 지정된 비율 내에 있을 때까지 이미지 품질이 저하됩니다. </p></td> 
 </tr> 
</table>

## 포함된 이미지 메모리 제한 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

웹 페이지에 포함할 수 있는 이미지 크기에 제한이 있는 장치의 경우 응답 형식이 jpg인 경우 이미지 크기는 해당 크기로 제한됩니다. 프록시는 장치에 제한이 없는 경우 응답을 500MB로 제한합니다.

## 백엔드 처리 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

프록시는 Device Atlas 데이터 파일을 하루에 한 번 다운로드하여 확인하고 로드합니다. 확인은 다른 장치에 대해 다른 속성을 가져와 새 데이터를 수락하기 전에 예상되는 값과 비교합니다.
