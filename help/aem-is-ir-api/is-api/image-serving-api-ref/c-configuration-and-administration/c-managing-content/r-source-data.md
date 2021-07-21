---
description: 이미지 제공 소스 데이터 파일에는 이미지 및 마스크 파일, 글꼴 및 ICC 프로필이 포함됩니다.
solution: Experience Manager
title: 소스 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 소스 데이터{#source-data}

이미지 제공 소스 데이터 파일에는 이미지 및 마스크 파일, 글꼴 및 ICC 프로필이 포함됩니다.

모든 소스 데이터 파일은 이미지 서버에서 액세스할 수 있어야 합니다. Image Serving은 데이터 파일의 위치를 지정하는 많은 대체 요소를 제공합니다.

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그::경로|카탈로그::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 이미지 제공 HTTP 요청에 지정된 상대 이미지 파일 경로 및 이름</span> </p></td> 
 </tr> 
</table>

서버는 절대 파일 경로가 설정될 때까지 경로 세그먼트를 오른쪽에서 왼쪽으로 결합합니다.

모든 `*`rootPath`*` 세그먼트는 비어 있거나, 상대 또는 절대 경로 세그먼트일 수 있습니다.

`*``*` catalog절대 또는 상대 파일 경로/이름을 붙여 넣습니다. `*``*` requestPath는 상대 파일 경로/이름이어야 합니다.

`Multiple IS::RootPath` 값은 ImageServerRegistry.xml(또는 admin interface)에서 정의할 수 있습니다. 이렇게 하면 소스 데이터 파일을 여러 파일 시스템 간에 배포할 수 있습니다. 이미지 서버는 데이터 파일을 찾을 때까지 지정된 순서대로 대체 경로를 시도합니다.

서버를 중지하지 않고도 언제든지 모든 종류의 새 데이터 파일을 추가할 수 있습니다.
