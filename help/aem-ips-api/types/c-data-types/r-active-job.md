---
description: 서버에서 실행되는 작업. 또한 예약된 작업의 인스턴스입니다.
seo-description: 서버에서 실행되는 작업. 또한 예약된 작업의 인스턴스입니다.
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

서버에서 실행되는 작업. 또한 예약된 작업의 인스턴스입니다.

작업은 3개 주에 있습니다.

* 실행이 예약되었습니다.
* 현재 실행 중입니다.
* 실행을 완료했으며 작업 로그에 정보를 이미 기록했습니다.

작업 유형을 반환할 작업 유형 값을 지정합니다. 다음 작업을 반환할 수 있습니다.

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## 매개 변수 {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 회사 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 회사를 담당하세요. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 작업 <span class="varname"> 핸들</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 작업을 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 작업의 고유 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 원본</span> 이름 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">작업과 함께 제출된 <span class="codeph"> ActiveJob</span> 유형의 원래 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 유형</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 시스템에서 반환되는 작업 유형 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 도</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 시스템에서 반환되는 활성 작업 상태 선택 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> submitUserEmail <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 작업을 예약한 사용자의 이메일 주소입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 로케일</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">작업 로그 세부 사항 및 이메일 현지화를 위한 로케일입니다. <p>언어 코드가 ISO-639에서 지정한 소문자, 두 문자 코드인 소문자, ISO-3166에서 지정한 대소문자, 두 문자 코드인 &lt;language_code&gt;[-&lt;country_code&gt;] <span class="codeph"></span>로 로케일을 지정합니다. 예를 들어 영어(미국)의 로케일 문자열은 다음과 같습니다.en- <span class="codeph"> US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 설명</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3">submitJob에 원래 지정된 작업 <span class="codeph"> 설명입니다</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> server <span class="varname"> Name</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 작업을 실행하는 서버의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 시작</span> 날짜 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 활성 작업의 날짜, 시간 및 표준 시간대 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 총 <span class="varname"> 크기</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 활성 작업의 총 크기입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 진행</span> 상황 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 작업 진행(즉, 작업이 완료되는 시점). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 작업 진행 상황을 설명하는 텍스트 메시지입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 마지막 진행률 업데이트의 날짜, 시간 및 시간대입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> taskProgressArray <span class="varname"> 작업</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:TaskProgressArray</span> </td> 
   <td colname="col3"> 비동기 작업 진행 정보를 참조하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageServingPublishJob</span> </td> 
   <td colname="col3"> 이미지 제공 게시 작업에 대한 작업 세부 정보입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageServingRenderJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageServingRenderJob</span> </td> 
   <td colname="col3"> 게시 작업을 렌더링하는 이미지에 대한 작업 세부 정보입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 비디오 <span class="varname"> 게시</span> 작업 </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:VideoPublishJob</span> </td> 
   <td colname="col3"> 비디오 게시 작업의 작업 세부 정보입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> serverDirectoryPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ImageServingPublishJob</span> </td> 
   <td colname="col3"> 서버 디렉토리 게시 작업에 대한 작업 세부 정보입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> uploadUrlJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UploadUrlJob</span> </td> 
   <td colname="col3"> 업로드 URL 작업에 대한 작업 세부 정보입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> PDF <span class="varname"> 리핑작업</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:RipPdfs작업</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imagesJob <span class="varname"> 최적화</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 재처리자산작업 <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 업로드 <span class="varname"> PostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:UploadPostJob</span> </td> 
   <td colname="col3"> 데스크톱 업로드를 추적하는 작업 세부 사항. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 내보내기 <span class="varname"> 작업</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ExportJob</span> </td> 
   <td colname="col3">이전에 업로드한 파일의 인증된 내보내기를 허용합니다. 내보내기 <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"> 작업을 참조하십시오</a>. </td> 
  </tr> 
 </tbody> 
</table>

