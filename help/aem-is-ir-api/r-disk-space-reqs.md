---
description: '소프트웨어 설치에 필요한 공간 외에도 이미지 제공 장치의 디스크 공간 요구 사항은 다음과 같습니다 '
solution: Experience Manager
title: 디스크 공간 요구 사항 및 권장 사항
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# 디스크 공간 요구 사항 및 권장 사항{#disk-space-requirements-and-recommendations}

Image Serving은 소프트웨어 설치에 필요한 공간 외에도 다음과 같은 디스크 공간 요구 사항이 있습니다.

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>설명/기본 위치/설정</b> </th> 
   <th class="entry"> <b>계산/권장 사항</b> </th> 
   <th class="entry"> <b>설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>소스 이미지, 글꼴, ICC 프로파일</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>다음과 같이 달라집니다. 아래 주석을 참조하십시오. </p> </td> 
   <td> <p>이미지 서버에서만 액세스할 수 있어야 합니다. 서버는 데이터를 수정하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP 응답 데이터 캐시</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2 최소 2GB가 권장됩니다. </p> </td> 
   <td> <p>이 캐시는 중첩된/포함된 데이터와 외부 소스 이미지도 저장합니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>이미지 카탈로그 데이터 캐시</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>카탈로그 폴더가 1.5배의 공간을 사용할 수 있도록 허용합니다. </p> </td> 
   <td> <p>카탈로그를 처음에 로드할 때 채워집니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>로그 데이터</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100MB 이상 </p> </td> 
   <td> <p>로깅 구성 및 서버 사용에 따라 달라집니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>이미지 서버 임시 파일</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100MByte는 대부분의 용도로 충분합니다. </p> </td> 
   <td> <p>단기 데이터 PTIFF 및 특정 응답 이미지 형식이 아닌 소스 이미지에 필요할 수 있습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 소스 이미지에 대한 디스크 공간 요구 사항 {#section-317da75099ad480d9a461c7e706d4f1c}

이미지 변환기 명령줄 도구(IC)를 사용하여 모든 소스 이미지를 피라미드형 TIFF 파일 형식(PTIFF)으로 변환하는 것이 좋습니다. 이러한 변환은 모든 응용 프로그램에 대해 최적의 이미지 제공 런타임 성능을 보장합니다. 이미지 서버는 IC에서 허용하는 모든 소스 파일 형식을 처리할 수 있지만 Dynamic Media은 이러한 사용에 대한 지원을 제공하지 않습니다.

PTIFF 파일을 사용할 때 다음 엄지 규칙 덕분에 공간 요구 사항을 결정할 수 있습니다.

*`total_space`* (바이트) = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* 모든 원본 소스 이미지의 평균 픽셀 크기(너비 x 높이)입니다. 예를 들어 원래 이미지가 일반적으로 약 2k x 2k 픽셀인 경우 4M 픽셀입니다.
* *`avg_num_components`* 이미지의 유형에 따라 달라집니다. 대부분 RGB 이미지의 경우 3이며, 대부분 CMYK 또는 RGBA 이미지의 경우 4입니다. 이미지의 절반이 RGB이고 나머지 절반은 RGBA인 경우 3.5를 사용합니다.
* *`p_factor`* 이미지가 IC로 변환될 때 압축 유형 및 품질 세트에 따라 달라집니다.

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
   <td> <p>변형 압축 </p> </td> 
   <td> <p> 이미지에 따라 25-0.75 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG 압축 </p> </td> 
   <td> <p> 1(JPEG 품질 95의 경우 일반) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이러한 추정치로는 파일 시스템 오버헤드를 고려하지 않습니다. 디스크의 실제 공간은 훨씬 더 클 수 있습니다.

**예**

이미지 제공 배포에서는 평균 크기가 500x500 RGB 픽셀인 30,000개의 저해상도 레거시 이미지를 사용할 예정입니다. 새로운 인쇄 품질 이미지 데이터는 매년 10,000의 비율로 추가될 것으로 예상된다. 일반적인 CMYK 이미지 크기는 4k x 6k 바이트입니다. 모든 데이터는 고품질로 압축되어 JPEG 됩니다. 3년 사용 후 총 디스크 공간 크기는 다음과 같습니다.

*`total_space`* = 30,000x(2k + 0.5k x 0.5k x 3 x 0.1) + 10,000x(2k + 4k x 4x 0.1) = 2.2G + 268GB = 약 270GB

최상의 품질을 보장하려면 deflate(zip) 압축을 사용할 수 있습니다. 다음과 같은 *`p_factor`* 0.4 중 필요한 총 디스크 공간 크기는 약 4배 더 큽니다. 이 경우, 1TB가 약간 넘습니다.
