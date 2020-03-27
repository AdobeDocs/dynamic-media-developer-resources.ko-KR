---
description: 사용자 핸들 지정 여부에 따라 특정 사용자 또는 기본 사용자의 암호를 특정 값으로 설정합니다.
seo-description: 사용자 핸들 지정 여부에 따라 특정 사용자 또는 기본 사용자의 암호를 특정 값으로 설정합니다.
seo-title: setPassword
solution: Experience Manager
title: setPassword
topic: Scene7 Image Production System API
uuid: 78067f8d-4191-4580-a5a8-adb6edfcfab8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setPassword{#setpassword}

사용자 핸들 지정 여부에 따라 특정 사용자 또는 기본 사용자의 암호를 특정 값으로 설정합니다.

암호 만료 날짜는 선택 사항입니다. 생략하면 암호가 만료되지 않습니다.

## 인증된 사용자 유형 {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*사용자* 유형만 다른 사용자에 대해 setPassword 호출을 실행할 수 있습니다 `IpsAdmin` .

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
   <td colname="col1"> <p> <span class="codeph"> 사용자 <span class="varname"> 핸들 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열 </span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>사용자 핸들 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 암호 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:문자열 </span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>암호. </p> <p>다음 요구 사항은 선택한 암호에 적용됩니다. </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">암호는 대소문자를 구분합니다. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">최소 암호 길이는 8자입니다. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">암호는 다음 문자 클래스의 문자를 하나 이상 포함해야 합니다. 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">소문자 영어. 예를 들어 <span class="codeph"> a b c d e </span> 등 </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">대문자 영어. 예를 들어 <span class="codeph"> A B C D E </span> 등이 있습니다. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">숫자. 예를 들어 <span class="codeph"> 1 2 3 4 5 </span> 등이 있습니다. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">특수 기호 문자. 예를 들어 다음 중 하나를 사용할 수 있습니다.' ~ ! <span class="codeph"> @ # $ %^ * ( ) _ + - = { }| [ ] &amp; \ :" ;' &lt; &gt; ?,/ </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 암호 <span class="varname"> 만료 </span> 날짜 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>아니요 </p> </td> 
   <td colname="col4"> <p>암호 만료 날짜를 결정합니다. <p>참고: 이 필드에 대한 요청을 표준 시간대를 제공합니다. 시간대는 중앙 시간으로 조정됩니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력(setPasswordReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다.

## 예제 {#section-23a6fbabdb3c4c3180076057e47ae567}

이 코드 샘플은 사용자 암호를 만듭니다. 암호를 생략했기 때문에 암호가 만료되지 `passwordExpires` 않습니다.

**요청**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**응답**

없음.
