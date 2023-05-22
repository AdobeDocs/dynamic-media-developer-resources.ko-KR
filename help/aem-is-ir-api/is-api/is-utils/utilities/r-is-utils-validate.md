---
description: 이미지 유효성 검사 유틸리티. 이 명령줄 유틸리티는 이미지 파일이 유효한지 확인하고 이미지 제공으로 어려움 없이 읽을 수 있는지 확인합니다.
solution: Experience Manager
title: 유효성 확인
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# 유효성 확인{#validate}

이미지 유효성 검사 유틸리티. 이 명령줄 유틸리티는 이미지 파일이 유효한지 확인하고 이미지 제공으로 어려움 없이 읽을 수 있는지 확인합니다.

PTIFF가 아닌 모든 이미지 파일은 유효성 검사를 통과해야 파일을 이미지 서비스 제공에 소스 이미지로 사용할 수 있습니다. PTIFF 이미지는 잠재적으로 신뢰할 수 없는 복사 작업 후에 유효성이 검사되어야 합니다.

## 사용 {#usage}

` validate *`fileType`* [ *`옵션`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>소스 파일 형식, 하나 이상을 지정해야 합니다(-any는 IC에서 지원하는 동일한 이미지 파일 형식을 허용합니다). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 옵션 </span> </span> </p> </td> 
  <td class="stentry"> <p>기타 명령 옵션(아래 참조) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> 이미지 파일입니다. 공백으로 구분된 항목이 없습니다. </p> </td> 
 </tr> 
</table>

## 반환 {#section-67a7cf7c53144fbb8f24b818f4a10901}

성공하면 0입니다. 오류가 발생하면 0이 아닌 값이 반환되고 오류 세부 정보가 로 전송됩니다. `stderr`.

## 옵션 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 파일 목록을 포함하는 별도의 텍스트 파일을 지정합니다. 파일당 하나의 레코드입니다. If <span class="codeph"> -fileList </span> 포함, <span class="varname"> sourceFile </span> 을(를) 지정하지 않아야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>전체 이미지 파일을 확인할 수 있습니다. 기본적으로 이미지 헤더만 확인됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>임베드된 색상 프로파일이 유효한지 확인합니다. 기본적으로 프로필 본문은 선택되어 있지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 이미지 구성 요소당 16비트가 있는 이미지를 거부합니다. 원격 소스 이미지의 유효성을 검사할 때 항상 이미지 서버에서 지정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 이미지가 잘못된 경우 자세한 정보를 인쇄합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -자동 </span> </p> </td> 
  <td class="stentry"> <p>비활성화 <span class="codeph"> stdout </span>/ <span class="codeph"> stder </span> 출력. 상태만 반환됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>추가 파일의 유효성을 검사하지 못한 경우에도 파일 유효성 검사 오류가 발생하면 처리를 종료합니다. 기본적으로 유효성 검사 오류가 발생하면 처리가 계속됩니다 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -버전 </span> </p> </td> 
  <td class="stentry"> <p>이 유틸리티의 버전 정보를 반환합니다. 다른 옵션을 사용하지 않고 을(를) 지정합니다. </p> </td> 
 </tr> 
</table>
