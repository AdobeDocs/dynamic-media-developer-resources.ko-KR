---
description: 명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩되어야 합니다. 이렇게 하면 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않습니다.
seo-description: 명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩되어야 합니다. 이렇게 하면 값 문자열에 예약된 문자 '=', '&' 및 '%'가 포함되지 않습니다.
seo-title: 이미지 제공 HTTP 인코딩
solution: Experience Manager
title: 이미지 제공 HTTP 인코딩
topic: Scene7 Image Serving - Image Rendering API
uuid: e7fb368b-060a-439e-95a1-16b94d4796dc
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 21%

---


# 이미지 제공 HTTP 인코딩{#image-serving-http-encoding}

명령 값은 %xx 이스케이프 시퀀스를 사용하여 http 인코딩되어야 합니다. 이렇게 하면 값 문자열에 예약된 문자 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39;가 포함되지 않습니다.

그렇지 않으면 표준 HTTP 인코딩 규칙이 적용됩니다. HTTP 사양은 안전하지 않은 문자뿐만 아니라 및 같은 모든 컨트롤 문자를 인코딩해야 `<return>` 합니다 `<tab>`. 문자의 URL 인코딩은 &quot;%&quot; 기호로 구성되며 그 뒤에 ISO-라틴 코드 포인트의 두 자리 16진수 표현(대/소문자 구분 안 함)이 옵니다. 안전하지 않은 문자 및 코드 포인트는 다음과 같습니다.

<table id="table_D2C01CADB35E477D82D4C27586424625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 안전하지 않은 문자 </th> 
   <th colname="col2" class="entry"> 코드 포인트(16진수) </th> 
   <th colname="col3" class="entry"> 코드 포인트(12월) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>공간 </p> </td> 
   <td colname="col2"> <p>20 </p> </td> 
   <td colname="col3"> <p>32 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lt; </p> </td> 
   <td colname="col2"> <p>3C </p> </td> 
   <td colname="col3"> <p>60 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&gt; </p> </td> 
   <td colname="col2"> <p>3E </p> </td> 
   <td colname="col3"> <p>62 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>" </p> </td> 
   <td colname="col2"> <p>22 </p> </td> 
   <td colname="col3"> <p>34 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p># </p> </td> 
   <td colname="col2"> <p>23 </p> </td> 
   <td colname="col3"> <p>35 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p>25 </p> </td> 
   <td colname="col3"> <p>37 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;lbraces; </p> </td> 
   <td colname="col2"> <p>7B </p> </td> 
   <td colname="col3"> <p>123 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;rbrace; </p> </td> 
   <td colname="col2"> <p>7D </p> </td> 
   <td colname="col3"> <p>125 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>| </p> </td> 
   <td colname="col2"> <p>7C </p> </td> 
   <td colname="col3"> <p>124 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>\ </p> </td> 
   <td colname="col2"> <p>5C </p> </td> 
   <td colname="col3"> <p>92 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>^ </p> </td> 
   <td colname="col2"> <p>5E </p> </td> 
   <td colname="col3"> <p>94 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~ </p> </td> 
   <td colname="col2"> <p>7E </p> </td> 
   <td colname="col3"> <p>126 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;lbrack; </p> </td> 
   <td colname="col2"> <p>5B </p> </td> 
   <td colname="col3"> <p>91 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;rbrack; </p> </td> 
   <td colname="col2"> <p>5D </p> </td> 
   <td colname="col3"> <p>93 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>` </p> </td> 
   <td colname="col2"> <p>60 </p> </td> 
   <td colname="col3"> <p>96 </p> </td> 
  </tr> 
 </tbody> 
</table>

예약된 문자도 인코딩해야 합니다.

<table id="table_A6C808A05EA6420F8125186D3D5C9E33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 예약된 문자 </th> 
   <th colname="col2" class="entry"> 코드 포인트(16진수) </th> 
   <th colname="col3" class="entry"> 코드 포인트(12월) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>$ </p> </td> 
   <td colname="col2"> <p>24 </p> </td> 
   <td colname="col3"> <p>36 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp; </p> </td> 
   <td colname="col2"> <p>26 </p> </td> 
   <td colname="col3"> <p>38 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+ </p> </td> 
   <td colname="col2"> <p>2B </p> </td> 
   <td colname="col3"> <p>43 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>, </p> </td> 
   <td colname="col2"> <p>2C </p> </td> 
   <td colname="col3"> <p>44 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>/ </p> </td> 
   <td colname="col2"> <p>2F </p> </td> 
   <td colname="col3"> <p>47 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>: </p> </td> 
   <td colname="col2"> <p>3A </p> </td> 
   <td colname="col3"> <p>58 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>; </p> </td> 
   <td colname="col2"> <p>3B </p> </td> 
   <td colname="col3"> <p>59 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>= </p> </td> 
   <td colname="col2"> <p>3D </p> </td> 
   <td colname="col3"> <p>61 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? </p> </td> 
   <td colname="col2"> <p>3F </p> </td> 
   <td colname="col3"> <p>63 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>@ </p> </td> 
   <td colname="col2"> <p>40 </p> </td> 
   <td colname="col3"> <p>64 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-b85895e5b6a84b96b7fca987656dd34d}

`…&$text=rate&weight=85% 27#&…`

난독화가 적용되지 않으면 위의 요청 조각을 다음과 같이 인코딩해야 합니다.

`…&$text=rate%26weight%3D85%25%2027%23&…`

난독화가 적용된 경우 인코딩을 &#39;=&#39;, &#39;&amp;&#39; 및 &#39;%&#39; 문자로 제한할 수 있습니다.

`…&$text=rate%26weight%3D85%25 27#&…`

## 참조 {#section-295476ec34c74973962d07dfa9eb2180}

[요청 난독화](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [HTTP/1.1 사양(RFC 2616)](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
