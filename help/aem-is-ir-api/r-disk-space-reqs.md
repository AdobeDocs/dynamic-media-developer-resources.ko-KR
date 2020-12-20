---
description: '소프트웨어 설치에 필요한 공간 외에도 이미지 서비스에는 다음과 같은 디스크 공간 요구 사항이 있습니다 '
seo-description: '소프트웨어 설치에 필요한 공간 외에도 이미지 서비스에는 다음과 같은 디스크 공간 요구 사항이 있습니다 '
seo-title: 디스크 공간 요구 사항 및 권장 사항
solution: Experience Manager
title: 디스크 공간 요구 사항 및 권장 사항
topic: Scene7 Image Serving - Image Rendering API
uuid: a6a21886-94d6-45b3-af68-497e039bdbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---


# 디스크 공간 요구 사항 및 권장 사항{#disk-space-requirements-and-recommendations}

소프트웨어 설치에 필요한 공간 외에도 이미지 서비스에는 다음과 같은 디스크 공간 요구 사항이 있습니다.

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>설명/ 기본 위치/ 설정</b> </th> 
   <th class="entry"> <b>계산/권장 사항</b> </th> 
   <th class="entry"> <b>설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>소스 이미지, 글꼴, ICC 프로파일</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>다양함;아래 주석을 참조하십시오. </p> </td> 
   <td> <p>이미지 서버에서만 액세스할 수 있어야 합니다.서버는 데이터를 수정하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP 응답 데이터 캐시</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2;최소 2GB 권장 </p> </td> 
   <td> <p>이 캐시는 중첩된/포함된 데이터와 외부 소스 이미지도 저장합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>이미지 카탈로그 데이터 캐시</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>카탈로그 폴더에서 1.5배 공간을 사용할 수 있도록 허용합니다. </p> </td> 
   <td> <p>처음에 카탈로그를 로드할 때 채워집니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>로그 데이터</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100MB 이상 </p> </td> 
   <td> <p>로깅 구성 및 서버 사용에 따라 다릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>이미지 서버 임시 파일</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100MBytes는 대부분의 사용자에게 적합합니다. </p> </td> 
   <td> <p>단기 데이터;PTIFF 및 특정 응답 이미지 형식이 아닌 소스 이미지에 필요할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 소스 이미지 {#section-317da75099ad480d9a461c7e706d4f1c}에 대한 디스크 공간 요구 사항

이미지 변환기 명령줄 도구(IC)를 사용하여 모든 소스 이미지를 피라미드형 TIFF 파일 형식(PTIFF)으로 변환하는 것이 좋습니다. 이러한 전환으로 모든 애플리케이션에 대한 이미지 제공 서비스의 최적의 런타임 성능을 보장합니다. 이미지 서버는 IC에서 허용하는 모든 소스 파일 형식을 처리할 수 있지만 Scene7은 이러한 사용을 지원하지 않습니다.

PTIFF 파일을 사용할 때 다음 축소판 규칙을 사용하여 공간 요구 사항을 결정할 수 있습니다.

*`total_space`* (바이트) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`*  *`p_factor`* x)

* *`avg_pixel_count`* 모든 원본 소스 이미지의 평균 픽셀 크기(너비 x 높이)입니다. 예를 들어 원본 이미지가 일반적으로 약 2k x 2k 픽셀인 경우 4M 픽셀입니다.
* *`avg_num_components`* 이미지 유형에 따라 다릅니다. 대부분 RGB 이미지의 경우 3이고, 대부분 CMYK 또는 RGBA 이미지의 경우 4입니다. 이미지의 절반은 RGB이고 나머지 반은 RGBA이면 3.5를 사용합니다.
* *`p_factor`* 이미지가 IC로 변환될 때 설정된 압축 유형과 품질에 따라 달라집니다.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF 압축</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>압축 해제됨 </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>디플레이트 압축 </p> </td> 
   <td> <p> 이미지에 따라 25-0.75 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG 압축 </p> </td> 
   <td> <p> 1(일반 JPEG 품질 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이와 비슷한 추정은 파일 시스템 오버헤드에 해당되지 않습니다. 디스크의 실제 공간은 상당히 클 수 있습니다.

**예**

이미지 제공 배포에서는 평균 크기가 500x500 RGB인 30,000개의 저해상도 레거시 이미지를 사용할 것으로 예상하고 있습니다. 새로운 인쇄 품질의 이미지 데이터는 연간 10,000개 비율로 추가될 예정입니다. 일반적인 CMYK 이미지 크기는 4k x 6k 바이트입니다. 모든 데이터는 고품질로 압축된 JPEG입니다. 3년 사용 후 총 디스크 공간 크기는 다음과 같이 예상됩니다.

*`total_space`* = 30,000 x (2k + 0.5k x 0.5k x 3 x 0.1) + 3 x 10,000 x (2k + 4k x 6k x 4 x 0.1) = 2.2G + 268GB = 약 270GB

최상의 품질을 보장하려면 디플레이트(zip) 압축을 사용할 수 있습니다. 0.4의 *`p_factor`*&#x200B;을 가정할 경우 필요한 총 디스크 공간 크기는 약 4배 더 큽니다. 이 경우 1TB가 약간 넘습니다.
