---
description: 플레이로그 유틸리티를 사용하여 HTTP 응답 캐시에 대한 컨텐츠를 미리 생성할 수 있습니다.
solution: Experience Manager
title: '''playlog'' 유틸리티'
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# &#39;playlog&#39; 유틸리티{#the-playlog-utility}

플레이로그 유틸리티를 사용하여 HTTP 응답 캐시에 대한 컨텐츠를 미리 생성할 수 있습니다.

버전 번호의 첫 번째 또는 두 번째 숫자가 변경된 경우, 주 버전 업그레이드 후 기존 이미지 제공 HTTP 응답 캐시를 사용할 수 없습니다. 업그레이드 후 서버를 전체 로드 조건으로 전환하는 경우 캐시가 합리적으로 채워지고 캐시 적중률이 증가할 때까지 서버는 처음 몇 시간의 캐시 누락 요청을 처리하는 오버로드될 수 있습니다.

이러한 초기 로드 스파이크를 방지하기 위해 `playlog` 유틸리티를 사용하여 HTTP 응답 캐시에 대한 컨텐츠를 미리 생성할 수 있습니다. `playlog` 기존 액세스 로그 파일에서 HTTP 요청을 추출하여 서버로 전송하여 캐시 항목을 생성합니다. 일반적인 사용 시나리오의 경우 하루 동안의 트래픽이 포함된 단일 액세스 로그 파일을 재생하는 것으로 충분합니다.

이 유틸리티는 업그레이드 설치 후 HTTP 응답 캐시를 생성하는 것 외에도 로드 밸런싱된 환경에 새 서버를 추가할 때 캐시 컨텐츠를 미리 생성하는 데 사용됩니다.다른 서버 중 하나에서 최근 로그 파일을 재생하면 됩니다.

`playlog` 는 이전 버전의 이미지 제공 서비스에서 생성된 대부분의 액세스 로그 파일을 지원하도록 구성할 수 있습니다.

## 사용 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> 접두사  </span> </span> </p> </td> 
  <td class="stentry"> <p>로그 파일에서 추출된 요청 앞에 추가할 루트 URL입니다. </p> <p>기본값:<span class="filepath"> http://localhost:8080/is </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>로그 레코드에 요청이 들어 있는 필드(열) 번호입니다.1을 기반으로 합니다. </p> <p>기본값:16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> 구분 기호  </span> </span> </p> </td> 
  <td class="stentry"> <p>필드 구분 기호;정규 표현식 패턴입니다. </p> <p>기본값: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> 마커  </span> </span> </p> </td> 
  <td class="stentry"> <p>요청 마커;로그 파일에서 재생해야 하는 요청을 식별합니다.정규 표현식 패턴입니다. </p> <p>기본값:<span class="codeph"> 요청:</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> 접미사  </span> </span> </p> </td> 
  <td class="stentry"> <p>로그 파일에서 추출된 요청에 추가할 접미사입니다.는 로그 파일의 라이브 요청에서 재생 요청을 구분하는 데 사용할 수 있습니다.'?' 또는 '&amp;' 구분 기호가 자동으로 삽입됩니다.접미사는 중괄호 내의 위치별로 모든 로그 필드를 참조할 수 있으며, 기본값은 md5 서명 필드에 해당합니다. </p> <p>기본값:<span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>세부 정보 표시 모드에서 생성된 요청 URL을 <span class="codeph"> stdout </span>에 인쇄합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>개요 를 <span class="codeph"> stdout </span>에 인쇄합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - 사용할 HTTP 요청 메서드( <span class="codeph"> get|post|head|smart </span>). </p> <p>기본값:<span class="codeph"> smart </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - 로그 파일의 pos를 사용하여 원래 메서드를 가져옵니다. </p> <p>기본값:15 </p> </td> 
 </tr> 
</table>

Windows의 경우 파일 이름은 [!DNL playlog.bat]이고 Linux의 경우 [!DNL playlog.sh]입니다.

## 예제 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

다음 예에서는 Linux에서 이미지 제공 기능이 생성한 액세스 로그 파일의 모든 요청을 재생합니다.

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

다음 명령은 Windows에서 이미지 제공 기능이 만든 추적 로그 파일에 있는 모든 요청을 재생합니다.

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
