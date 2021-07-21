---
description: 액세스 로깅 시 이러한 서버 설정을 사용합니다.
solution: Experience Manager
title: 액세스 로깅
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 3%

---

# 액세스 로깅{#access-logging}

액세스 로깅 시 이러한 서버 설정을 사용합니다.

구문

## TC::directory - 로그 파일 폴더 {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Platform Server에서 로그 파일을 작성하는 폴더입니다. 이는 절대 경로이거나 *`install_folder`*&#x200B;에 상대적인 경로일 수 있습니다. 기본값은 [!DNL  *`install_folder`*/logs]입니다.

>[!NOTE]
>
>이 설정을 변경하기 전에 새 폴더를 만들어야 합니다. 루트 이외의 사용자 계정에서 실행되도록 이미지 제공 기능이 설치된 경우 폴더에 올바른 읽기/쓰기 액세스 권한이 있는지 확인합니다.

## TC::maxDays - 로그 파일을 보관할 일 수 {#section-45cbecffc5694c87b7d5c176a44a4885}

로그 파일을 보관할 일 수입니다. 매일 자정에 새 로그 파일이 만들어집니다. 이때 서버는 Image Server 또는 Render Server에서 작성한 파일을 포함하여 지정된 일 수보다 오래된 로그 파일 폴더의 모든 파일을 삭제합니다. 기본값은 10입니다.

## TC::prefix - 액세스 로그 파일 이름 {#section-1003856323b844049632710a5a056aa7}

액세스 로그 데이터가 기록되는 파일의 이름 접두사입니다. 날짜 및 파일 접미사( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log])가 지정된 문자열에 추가됩니다. 액세스 로그 파일의 이름은 추적 로그 파일의 이름과 달라야 합니다. 기본값은 &quot; `access-`&quot;입니다.

## TC::pattern - 액세스 로그 패턴 {#section-22775ea85cee444d8a7d7336a3b1feef}

Platform Server 액세스 로그 레코드의 데이터 패턴을 지정합니다. 패턴 문자열은 해당 값으로 대체되는 변수를 지정합니다. 패턴 문자열의 다른 모든 문자는 말 그대로 로그 레코드로 전송됩니다.

캐시 준비 유틸리티를 사용하려면 공백을 필드 구분 기호로 사용해야 합니다. Platform Server는 필드 값의 모든 공백 및 &#39;%&#39; 문자를 각각 `%20` 및 `%25`로 바꿉니다.

지원되는 패턴 변수는 다음과 같습니다.

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>패턴</b> </th> 
   <th class="entry"> <b>설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>원격 IP 주소입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>로컬 IP 주소입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>HTTP 헤더를 제외한 응답 바이트 수나 0인 경우 ' '를 제외합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>HTTP 헤더를 제외한 응답 바이트 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>요청 처리 시간(밀리초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>스레드 id(상호 참조 디버그/오류 로그 항목의 경우) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> yyyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS  </span> 오프셋  </span> </p> <p> ( <span class="varname"> SSS </span>은 msec이고, <span class="varname"> offset </span>은 GMT 시간 오프셋입니다.); 시간 값은 응답이 클라이언트에 전송될 때 캡처됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>요청 메서드( <span class="codeph"> GET </span>, <span class="codeph"> POST </span> 등). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>요청이 겹칩니다(동시에 처리된 요청 수). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>이 요청을 받은 로컬 포트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>쿼리 문자열(앞에 '?'가 붙음 있을 경우). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>첫 번째 요청 줄(요청 메서드, URI, HTTP 버전). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p><span class="codeph"> %r </span>과 동일하지만 로그 구문 분석 문제를 방지하기 위해 제한된 HTTP 인코딩을 URI에 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP 응답 상태 코드입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>사용자 세션 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>날짜 및 시간(일반 로그 형식) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>인증된 원격 사용자(있는 경우), 기타 ". </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI 경로입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>로컬 서버 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>요청 처리 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>Platform Server 캐시 키(캐시 파일 폴더/이름)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Platform Server 캐시 관리 키워드: <span class="codeph"> { REUSE | 생성됨 | 업데이트됨 | 원격 | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | 유효함 | 무시됨 | 정의되지 않음 } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>응답 MIME 유형입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{컨텍스트}r </p> </td> 
   <td> <p>컨텍스트 전달이 발생하는 경우 대상 컨텍스트. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p><span class="codeph"> 태그 </span> 응답 헤더 값(응답 데이터의 MD5 서명)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{예외}r  </span> </p> </td> 
   <td> <p>오류 메시지. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>이미지 서버에서 캐시 항목 또는 데이터를 검색하는 데 걸리는 시간입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>요청 구문 분석 및 이미지 카탈로그 조회에 걸린 시간입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>이 요청이 카탈로그 시스템 외부의 경로 기반 액세스를 시도했는지 여부를 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>캐시 항목을 전달된 캐시 클러스터의 피어 서버의 IP 주소이거나, <span class="codeph"> CacheUse </span>이 <span class="codeph"> REMOTE_CREATED </span> 또는 <span class="codeph"> REMOTE_UPDATED </span>이 아닌 경우 '-' 주소입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>오류 카테고리: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=오류가 없습니다. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=서버에 이미지가 없습니다. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS 프로토콜 사용 오류 또는 1 이외의 컨텐츠 오류입니다. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=기타 서버 오류입니다. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=임시 서버 오버로드로 인해 요청이 거부되었습니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p><span class="codeph"> req= </span>의 대문자 값. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>요청의 기본 카탈로그의 루트 ID입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>데이터를 출력 스트림에 작성한 후 Platform Server가 응답을 전송하는 데 걸리는 시간입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{크기}r  </span> </p> </td> 
   <td> <p><span class="codeph"> %B </span>과 마찬가지로 304(수정되지 않음) 응답에 대한 값이 포함됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ConvertedUrl}r  </span> </p> </td> 
   <td> <p>모든 규칙 세트 변형 후의 최종 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>지정된 HTTP 요청 헤더의 값입니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>지정된 HTTP 응답 헤더의 값입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

기본값은 입니다. `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
