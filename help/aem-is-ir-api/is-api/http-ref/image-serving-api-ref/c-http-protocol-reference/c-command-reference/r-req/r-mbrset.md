---
description: 다중 비트 전송률 데이터.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# mbrSet{#mbrset}

다중 비트 전송률 데이터.

`req=mbrSet[,text|xml[, *`인코딩`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

네트 경로 ID와 연관된 비디오 세트의 유효한 비디오 항목에 해당하는 URL(및 해당 비트율) 목록이 포함된 텍스트 또는 xml 응답을 반환합니다.

유효한 비디오 항목에 대한 값이 있어야 하는 이전 요구 사항 `catalog::VideoBitRate` 이(가) 이제 완화되었습니다. 항목은 값을 포함할 수 있습니다. `catalog::VideoBitRate`*또는* `catalog::AudioBitRate`*또는* `catalog::TotalStreamBitRate`. 비디오 항목이 유효하려면 이 중 하나만 정의하면 됩니다. 의 요구 사항을 참조하십시오. `catalog::Path` 올바른 비디오 파일 확장명이 변경되지 않았습니다.

응답은 Apple 및 Flash 스트리밍 서버에서 사용하기 위한 것이므로 구조적으로 해당 사양을 따릅니다. URL은 접두사를 사용하여 생성됩니다 `attribute::HttpAppleStreamingContext` 및 `attribute::HttpFlashStreamingContext`.

m3u8 응답에는 비디오 세트에 mp4 파일이 있는 경우에만 포함됩니다. mp4 파일이 없는 경우 이러한 응답에는 f4v 파일만 포함됩니다. mp4 파일 또는 f4v 파일이 없는 경우 응답이 비어 있습니다.

f4m 응답에는 비디오 세트에 f4v 파일이 있는 경우에만 포함됩니다. f4v 파일이 없으면 이러한 응답에는 mp4 파일만 포함됩니다. f4v 파일과 mp4 파일이 없는 경우 응답이 비어 있습니다.

f4m/m3u8 응답에 나타나는 비트율은 의 값에 해당합니다. `catalog::TotalStreamBitRate` (적절한 단위로 변환됨). If `catalog::TotalStreamBitRate` 가 정의되지 않은 경우 `catalog::VideoBitRate` 및 `catalog::AudioBitRate` 를 사용합니다.

HTTP 응답은 다음을 기반으로 하는 TTL로 캐시할 수 있습니다. `catalog::NonImgExpiration`.
