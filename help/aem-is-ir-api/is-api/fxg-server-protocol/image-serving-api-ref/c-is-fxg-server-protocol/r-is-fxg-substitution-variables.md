---
description: 대체 변수는 요청 URL에서 서버에 저장된 FXG 템플릿으로 값을 전송하는 데 사용됩니다.
seo-description: 대체 변수는 요청 URL에서 서버에 저장된 FXG 템플릿으로 값을 전송하는 데 사용됩니다.
seo-title: 대체 변수
solution: Experience Manager
title: 대체 변수
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# 대체 변수{#substitution-variables}

대체 변수는 요청 URL에서 서버에 저장된 FXG 템플릿으로 값을 전송하는 데 사용됩니다.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>변수 이름. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>변수를 설정할 값(문자열)입니다. </p> </td> 
 </tr> 
</table>

* 변수 정의 및 참조는 요청 URL의 쿼리 부분에서 발생할 수 있습니다.
* 변수는 다른 IS 명령과 유사하게 위와 같이 정의됩니다.행간 &#39;$&#39;은(는) 명령을 변수 정의로 식별합니다.
* 변수 이름 `*`var`*`은 대/소문자를 구분하며 문자, 숫자, &#39;-&#39; 및 &#39;_&#39;의 조합으로 구성될 수 있습니다.
* 중요 값은 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩되어야 합니다.

