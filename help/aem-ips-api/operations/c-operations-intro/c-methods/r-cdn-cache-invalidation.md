---
description: 제공된 URL 목록을 Dynamic Media CDN(Content Distribution Network) 제공자에게 전달하여 기존 HTTP 응답 캐시를 무효화합니다.
solution: Experience Manager
title: cdnCacheInvalidation
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 3%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

제공된 URL 목록을 Dynamic Media CDN(Content Distribution Network) 제공자에게 전달하여 기존 HTTP 응답 캐시를 무효화합니다.

## cdnCacheInvalidation:{#section-4f70d2bc79d64288b961836ab17e9690} 정보

CDN 캐시 무효화는 이 무효화 요청이 CDN 네트워크를 통해 처리된 후 Dynamic Media 네트워크의 현재 게시된 데이터에 대해 이러한 URL에 대한 모든 HTTP 요청의 재유효성 검사를 강제 수행합니다. Dynamic Media 서비스 URL 구조에 연결되지 않고 회사를 만들 때 할당된 Dynamic Media 회사 루트 ID와 직접 일치하는 모든 URL은 전체 요청에 대해 API 오류가 발생합니다. CDN이 무효라고 간주하는 것을 지원하지 않는 잘못된 URL은 전체 요청에 대한 API 오류도 초래할 수 있습니다.

**사용 빈도:규칙**

이 기능의 사용 빈도를 제어하는 규칙은 Dynamic Media의 CDN 파트너가 제어합니다. CDN은 사용자에게 최적의 서비스 성능을 유지하기 위해 이러한 무효화의 응답성을 저하시키는 재량을 보유합니다. Dynamic Media에 이 기능의 초과 사용에 대한 통보를 받는 경우 회사별로 또는 전체 서비스에서 해당 기능을 비활성화하는 방법을 사용해야 합니다.

**확인 이메일**

Dynamic Media CDN 파트너의 확인 이메일을 목록 작성자 또는 최대 5개의 다른 이메일 주소로 보낼 수 있습니다. 이메일에서 참조되는 URL이 지워졌다는 알림을 전체 CDN 네트워크에 보낸 경우 API는 확인을 보냅니다. 제공된 URL 수가 단일 알림에서 Dynamic Media이 CDN 파트너에게 전달할 수 있는 수를 초과하는 경우 `cdnCacheInvalidation`에 대한 단일 호출은 여러 이메일을 보낼 수 있습니다. 현재, 요청이 100개의 URL을 초과하는 경우이지만, CDN 파트너의 요청에 따라 변경될 수 있습니다.

**지원 날짜:**

6.0

## 인증된 사용자 유형 {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## 매개 변수 {#section-bd1ed2b7419945d19a2ebd5668499f72}

**입력** (  `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 이름</b> </th> 
   <th class="entry"> <b> 유형</b> </th> 
   <th class="entry"> <b> 필수</b> </th> 
   <th class="entry"> <b> 설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:문자열</span> </p> </td> 
   <td> <p> 예 </p> </td> 
   <td> <p> 무효화할 URL과 연결된 회사의 핸들입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 유형:UrlArray</span> </p> </td> 
   <td> <p> 예 </p> </td> 
   <td> <p> CDN 캐시에서 무효화할 최대 1,000개의 URL 목록. 모든 URL은 무효화하려면 Dynamic Media 회사 루트 ID를 포함해야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력**(  `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 이름</b> </th> 
   <th class="entry"> <b> 유형</b> </th> 
   <th class="entry"> <b> 필수</b> </th> 
   <th class="entry"> <b> 설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:문자열</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>제거 요청을 참조하는 핸들. </p> <p>이제 <span class="codeph"> cdnCacheInvalidation</span> API가 거의 즉시 캐시를 무효화합니다(~5초). 따라서 무효화 상태에 대한 투표는 일반적으로 더 이상 필요하지 않습니다. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> calculatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>제거 요청이 완료되는 예상 시간(초)입니다. 클라이언트는 상태 폴링 전에 이 시간을 기다려야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-f414361a58e84dfcbbac30a358d02125}

이 예에서는 CDN 캐시에서 4개의 URL을 무효화할 것을 요청합니다. 응답에는 작업의 성공 요령과 클라이언트가 이 기능을 사용할 수 있도록 지원하기 위해 CDN에서 직접 제공되는 오류 세부 정보 목록이 포함됩니다.

`getCdnCacheInvalidationStatus` 작업.

**요청**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**응답**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

