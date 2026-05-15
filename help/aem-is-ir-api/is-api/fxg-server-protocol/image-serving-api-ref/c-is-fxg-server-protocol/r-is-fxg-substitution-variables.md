---
description: 대체 변수는 요청 URL의 값을 서버에 저장된 FXG 템플릿으로 전송하는 데 사용됩니다.
solution: Experience Manager
title: 대체 변수
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: 'https://experienceleague.adobe.com/-IHIbaXxoDEGqbV2inp4RlmWpH-8js7Dn9b-CK1paxg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 0%

---

# 대체 변수{#substitution-variables}

대체 변수는 요청 URL의 값을 서버에 저장된 FXG 템플릿으로 전송하는 데 사용됩니다.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 변수 </span> </span> </p> </td> 
  <td class="stentry"> <p>변수 이름. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td> 
  <td class="stentry"> <p>변수를 설정할 값(문자열). </p> </td> 
 </tr> 
</table>

* 변수 정의 및 참조는 요청 URL의 쿼리 부분에서 발생할 수 있습니다.
* 변수는 다른 IS 명령과 마찬가지로 위와 같이 정의됩니다. 선행 &#39;$&#39;는 명령을 변수 정의로 식별합니다.
* 변수 이름 `*`var`*`은(는) 대/소문자를 구분하며 문자, 숫자, &#39;-&#39; 및 &#39;_&#39;의 조합으로 구성될 수 있습니다.
* 중요한 값은 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩되어야 합니다.
