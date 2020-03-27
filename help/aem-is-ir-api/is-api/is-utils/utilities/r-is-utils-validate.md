---
description: 이미지 유효성 검사 유틸리티. 이 명령줄 유틸리티는 이미지 파일이 유효한지 확인하여 이미지 제공에서 손쉽게 읽을 수 있도록 합니다.
seo-description: 이미지 유효성 검사 유틸리티. 이 명령줄 유틸리티는 이미지 파일이 유효한지 확인하여 이미지 제공에서 손쉽게 읽을 수 있도록 합니다.
seo-title: 유효성 확인
solution: Experience Manager
title: 유효성 확인
topic: Scene7 Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 유효성 확인{#validate}

이미지 유효성 검사 유틸리티. 이 명령줄 유틸리티는 이미지 파일이 유효한지 확인하여 이미지 제공에서 손쉽게 읽을 수 있도록 합니다.

PTIFF가 아닌 모든 이미지 파일은 소스 이미지로 이미지 제공에서 파일을 사용할 수 있도록 하기 전에 유효성 검사를 전달해야 합니다. PTIFF 이미지는 신뢰할 수 없는 복사 작업 후 검증되어야 합니다.

## 사용 {#usage}

` validate *`파일`* [ *``*] [ *`유형SourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 파일 <span class="varname"> 유형 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg| -ptif| -any </span> </p> <p>소스 파일 유형;하나 이상을 지정해야 합니다(-any는 IC에서 지원하는 동일한 이미지 파일 형식을 허용합니다). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 옵션 </span></span> </p> </td> 
  <td class="stentry"> <p>기타 명령 옵션(아래 참조). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 소스 <span class="varname"> 파일 </span></span> </p> </td> 
  <td class="stentry"> <p> 이미지 파일. 하나 이상, 공백으로 구분됩니다. </p> </td> 
 </tr> 
</table>

## Returns {#section-67a7cf7c53144fbb8f24b818f4a10901}

0(성공한 경우)을 선택합니다. 오류가 발생하면 0이 아닌 값이 반환되고 오류 세부 정보가 로 `stderr`전송됩니다.

## 옵션 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span></span> </p> </td> 
  <td class="stentry"> <p>이미지 파일 목록을 포함하는 별도의 텍스트 파일을 지정합니다. 파일당 레코드 한 개 - <span class="codeph"> fileList가 </span> 포함된 경우 <span class="varname"> sourceFile을 </span> 지정하지 않아야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>전체 이미지 파일을 확인할 수 있습니다. 기본적으로 이미지 헤더만 유효성이 확인됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>포함된 색상 프로필에 유효성이 있는지 확인합니다. 기본적으로 프로필 본문은 선택되지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 이미지 구성 요소당 16비트로 이미지를 거부합니다. 이미지 서버가 원격 소스 이미지의 유효성을 검사할 때 항상 지정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 이미지가 잘못된 경우 자세한 정보를 인쇄합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>stdout <span class="codeph"> / </span>stderr <span class="codeph"> </span> 출력을 비활성화합니다. 상태만 반환됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>추가 파일의 유효성을 아직 확인하지 않은 경우에도 파일 유효성 검사가 실패할 때 처리를 종료합니다. 기본적으로 유효성 검사 오류가 발생하면 처리가 계속됩니다 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -버전 </span> </p> </td> 
  <td class="stentry"> <p>이 유틸리티에 대한 버전 정보를 반환합니다. 다른 옵션 없이 지정합니다. </p> </td> 
 </tr> 
</table>

