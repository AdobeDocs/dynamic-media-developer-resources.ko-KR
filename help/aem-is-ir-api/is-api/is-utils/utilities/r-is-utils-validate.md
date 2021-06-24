---
description: 이미지 유효성 검사 유틸리티. 이 명령줄 유틸리티는 이미지 파일이 유효한지 확인하고 이미지 제공 기능을 통해 쉽게 읽을 수 있는지 확인합니다.
solution: Experience Manager
title: 유효성 확인
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---

# 유효성 확인{#validate}

이미지 유효성 검사 유틸리티. 이 명령줄 유틸리티는 이미지 파일이 유효한지 확인하고 이미지 제공 기능을 통해 쉽게 읽을 수 있는지 확인합니다.

Image Serving에서 소스 이미지로 사용할 수 있게 하려면 PTIFF가 아닌 모든 이미지 파일이 유효성 검사를 전달해야 합니다. 신뢰할 수 없는 복사 작업 후에 PTIFF 이미지의 유효성을 검사해야 합니다.

## 사용 {#usage}

` validate *``* [ *``*] [ *`fileTypeitionsourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>소스 파일 형식;하나 이상의 이미지 파일 형식을 지정해야 합니다(IC에서 지원하는 이미지 파일 형식을 허용함). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 옵션  </span> </span> </p> </td> 
  <td class="stentry"> <p>기타 명령 옵션(아래 참조). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> 이미지 파일입니다. 둘 이상, 공백으로 구분합니다. </p> </td> 
 </tr> 
</table>

## 반환 {#section-67a7cf7c53144fbb8f24b818f4a10901}

성공할 경우 0입니다. 오류가 발생하면 0이 아닌 값이 반환되고 오류 세부 정보가 `stderr`으로 전송됩니다.

## 옵션 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>이미지 파일 목록을 포함하는 별도의 텍스트 파일을 지정합니다. 파일당 하나의 레코드. <span class="codeph"> -fileList </span>가 포함된 경우 <span class="varname"> sourceFile </span>을 지정하지 않아야 합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>전체 이미지 파일을 확인할 수 있습니다. 기본적으로 이미지 헤더만 유효성이 검사됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>포함된 색상 프로파일에서 유효성을 확인합니다. 기본적으로 프로필 본문은 선택되어 있지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> 이미지 구성 요소당 16비트가 있는 이미지를 거부합니다. 원격 소스 이미지의 유효성을 확인할 때 항상 이미지 서버에서 지정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> 이미지가 잘못된 경우 자세한 정보를 인쇄합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> 출력을 비활성화합니다. 상태만 반환됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>추가 파일의 유효성을 아직 검사하지 않은 경우에도 파일 유효성 검사 오류가 발생하면 처리를 종료합니다. 기본적으로 유효성 검사 오류가 발생하면 처리가 계속됩니다 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -버전 </span> </p> </td> 
  <td class="stentry"> <p>이 유틸리티에 대한 버전 정보를 반환합니다. 다른 옵션 없이 을 지정합니다. </p> </td> 
 </tr> 
</table>
