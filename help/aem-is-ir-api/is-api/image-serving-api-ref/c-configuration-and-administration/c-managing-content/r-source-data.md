---
description: 이미지 제공 소스 데이터 파일에는 이미지 및 마스크 파일, 글꼴 및 ICC 프로파일이 포함됩니다.
seo-description: 이미지 제공 소스 데이터 파일에는 이미지 및 마스크 파일, 글꼴 및 ICC 프로파일이 포함됩니다.
seo-title: 소스 데이터
solution: Experience Manager
title: 소스 데이터
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 소스 데이터{#source-data}

이미지 제공 소스 데이터 파일에는 이미지 및 마스크 파일, 글꼴 및 ICC 프로파일이 포함됩니다.

모든 소스 데이터 파일은 이미지 서버에서 액세스할 수 있어야 합니다. 이미지 제공에서는 데이터 파일의 위치를 지정할 수 있는 여러 가지 대체 요소를 제공합니다.

` *`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 파일 <span class="varname"> 경로 </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 요청 <span class="varname"> 경로</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 이미지 제공 HTTP 요청에 지정된 상대 이미지 파일 경로 및 이름</span> </p></td> 
 </tr> 
</table>

서버는 절대 파일 경로가 설정될 때까지 경로 세그먼트를 오른쪽에서 왼쪽으로 결합합니다.

모든 ` *`rootPath`*` 세그먼트는 비어 있거나 상대 또는 절대 경로 세그먼트일 수 있습니다.

` *`catalogPath`*` 는 절대 또는 상대 파일 경로/이름입니다. ` *`requestPath`*` 는 상대 파일 경로/이름이어야 합니다.

`Multiple IS::RootPath` 값은 ImageServerRegistry.xml(또는 관리 인터페이스)에서 정의할 수 있습니다. 이를 통해 소스 데이터 파일을 여러 파일 시스템에 배포할 수 있습니다. 이미지 서버는 데이터 파일을 찾을 때까지 지정된 순서대로 대체 경로를 시도합니다.

서버를 중지하지 않고도 언제든지 새로운 데이터 파일을 추가할 수 있습니다.
