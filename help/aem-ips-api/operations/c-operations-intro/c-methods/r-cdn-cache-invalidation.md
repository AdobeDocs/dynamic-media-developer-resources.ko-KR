---
description: 제공된 URL 목록을 Dynamic Media CDN(Content Distribution Network) 공급자에게 전달하여 HTTP 응답의 기존 캐시를 무효화합니다.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

제공된 URL 목록을 Dynamic Media CDN(Content Distribution Network) 공급자에게 전달하여 HTTP 응답의 기존 캐시를 무효화합니다.

## cdnCacheInvalidation: 정보 {#section-4f70d2bc79d64288b961836ab17e9690}

CDN 캐시 무효화는 이 무효화 요청이 CDN 네트워크를 통해 처리된 후 Dynamic Media 네트워크의 현재 게시된 데이터에 대해 이러한 URL에 대한 모든 HTTP 요청의 유효성을 다시 검사하도록 강제합니다. Dynamic Media 서비스 URL 구조에 연결되어 있지 않고 회사가 생성될 때 할당된 Dynamic Media 회사 루트 ID와 직접 일치하는 모든 URL은 전체 요청에 대한 API 오류를 발생시킵니다. CDN이 지원하지 않고 잘못된 것으로 간주하는 잘못된 URL은 전체 요청에 대한 API 오류를 발생시키기도 합니다.

**사용 빈도: 규칙**

이 기능의 사용 빈도를 제어하는 규칙은 Dynamic Media의 CDN 파트너에 의해 제어됩니다. CDN은 사용자에게 최적의 서비스 성능을 유지하기 위해 이러한 무효화의 응답성을 저하하는 재량권을 갖습니다. Dynamic Media에 이 기능의 과다 사용에 대한 알림이 전송되면 Adobe은 회사별로 또는 전체 서비스에서 기능을 비활성화해야 합니다.

**확인 전자 메일**

Dynamic Media CDN 파트너의 확인 이메일은 목록 작성자 또는 최대 5개의 다른 이메일 주소로 보낼 수 있습니다. API는 이메일에 참조된 URL이 지워졌다는 알림을 전체 CDN 네트워크에 받으면 확인을 전송합니다. 제공된 URL 수가 단일 알림에서 Dynamic Media이 CDN 파트너에게 전달할 수 있는 수를 초과하는 경우 `cdnCacheInvalidation`에 대한 단일 호출로 여러 이메일을 보낼 수 있습니다. 현재, 요청이 100개의 URL을 초과하지만 CDN 파트너의 요청에 따라 변경될 수 있습니다.

**다음 날짜 이후에 지원됨**

6.0

## 승인된 사용자 유형 {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## 매개 변수 {#section-bd1ed2b7419945d19a2ebd5668499f72}

**입력**( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 이름</b> </th> 
   <th class="entry"> <b> 유형</b> </th> 
   <th class="entry"> <b> 필요</b> </th> 
   <th class="entry"> <b> 설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> 예 </p> </td> 
   <td> <p> 무효화할 URL과 연결된 회사에 대한 핸들입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 유형:UrlArray</span> </p> </td> 
   <td> <p> 예 </p> </td> 
   <td> <p> CDN 캐시에서 무효화할 최대 1000개의 URL 목록. 모든 URL에는 무효화할 Dynamic Media 회사 루트 ID가 포함되어 있어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**출력**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 이름</b> </th> 
   <th class="entry"> <b> 유형</b> </th> 
   <th class="entry"> <b> 필요</b> </th> 
   <th class="entry"> <b> 설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>삭제 요청을 참조하는 핸들. </p> <p><span class="codeph"> cdnCacheInvalidation</span> API가 이제 캐시를 거의 즉시 무효화합니다(~5초). 따라서 무효화 상태에 대한 폴링은 일반적으로 더 이상 필요하지 않습니다. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>예 </p> </td> 
   <td colname="col4"> <p>제거 요청 완료까지의 예상 시간(초)입니다. 클라이언트는 상태를 폴링하기 전에 이 시간 동안 기다려야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-f414361a58e84dfcbbac30a358d02125}

이 예에서는 CDN 캐시에서 4개의 URL이 무효화되도록 요청합니다. 응답에는 작업 성공에 대한 요약 카운트와 클라이언트가 이 기능을 사용할 수 있도록 CDN에서 직접 제공한 오류 세부 정보 목록이 포함되어 있습니다.

`getCdnCacheInvalidationStatus` 작업입니다.

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
