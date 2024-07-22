---
description: 사용자 핸들을 지정하는지 여부에 따라 특정 사용자 또는 기본 사용자의 암호를 특정 값으로 설정합니다.
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 4%

---

# setPassword{#setpassword}

사용자 핸들을 지정하는지 여부에 따라 특정 사용자 또는 기본 사용자의 암호를 특정 값으로 설정합니다.

암호 만료일은 선택 사항입니다. 생략하면 암호가 만료되지 않습니다.

## 승인된 사용자 유형 {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*`IpsAdmin` 사용자 유형만* 다른 사용자에 대해 setPassword 호출을 실행할 수 있습니다.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## 매개 변수 {#section-0531294341f7483d89dacaa393dd659a}

**입력(setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>이름 </p> </th> 
   <th colname="col2" class="entry"> <p>유형 </p> </th> 
   <th colname="col3" class="entry"> <p>필수 </p> </th> 
   <th colname="col4" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>사용자 핸들. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 암호 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>암호. </p> <p>선택한 암호에는 다음 요구 사항이 적용됩니다. </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">암호는 대/소문자를 구분합니다. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">최소 암호 길이는 8자입니다. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">암호에는 다음 문자 클래스의 문자가 하나 이상 포함되어야 합니다. 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">소문자 영어 문자 예: <span class="codeph"> a b c d e </span> 등 </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">대문자 영문. 예를 들어 <span class="codeph"> A B C D E </span> 등입니다. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">숫자. 예를 들어 <span class="codeph"> 1 2 3 4 5 </span> 등입니다. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">특수 기호 문자 예를 들어 <span class="codeph"> &amp;grave; ~ ! 중 하나를 사용할 수 있습니다. @ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>암호 만료일을 결정합니다. <p>참고: 이 필드에 대한 요청이 포함된 시간대를 제공하십시오. 시간대는 중부 표준시로 조정됩니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(setPasswordReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-23a6fbabdb3c4c3180076057e47ae567}

이 코드 샘플은 사용자 암호를 만듭니다. `passwordExpires`이(가) 생략되어 암호가 만료되지 않습니다.

**요청**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**응답**

없음.
