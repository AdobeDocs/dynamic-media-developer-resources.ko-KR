---
description: 이미지 서버 프록시를 사용하여 일본어 전화의 이미지 크기를 조정할 수 있습니다.
solution: Experience Manager
title: 이미지 서버 프록시
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 이미지 서버 프록시{#image-server-proxy}

이미지 서버 프록시를 사용하여 일본어 전화의 이미지 크기를 조정할 수 있습니다.

## URL 형식 {#section-2e8c40b0547c4f99874cdf502b338940}

IS 프록시의 URL 형식은 일반 IS 요청과 매우 유사합니다. 프록시에 전달된 모든 IS 수정자는 이미지 서버로 전달됩니다. 에서 IS 수정자에 대한 정보를 찾을 수 있습니다 [HTTP 프로토콜 참조](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 프록시별 수정자 목록 {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>이미지 너비로 사용할 장치의 사용 가능한 너비 비율을 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>이미지 높이로 사용할 장치의 사용 가능한 높이의 백분율을 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>응답 크기를 제한할 장치의 메모리 제한 포함된 미디어 속성의 백분율을 지정합니다. 이는 jpg 응답에만 적용됩니다. 응답 크기가 지정된 백분율 이내가 될 때까지 이미지 품질이 낮아집니다. </p></td> 
 </tr> 
</table>

## 포함된 이미지 메모리 제한 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

장치에 웹 페이지에 임베드할 수 있는 이미지 크기에 제한이 있는 경우 응답 형식이 jpg인 한 이미지 크기가 해당 크기로 제한됩니다. 프록시는 디바이스에 제한이 없는 경우 응답을 500MB로 제한합니다.

## 백엔드 처리 중 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

프록시는 Device Atlas 데이터 파일을 하루에 한 번 다운로드하고 확인하고 로드합니다. 확인은 장치마다 다른 속성을 꺼내어 예상값과 비교한 후 새 데이터를 승인합니다.
