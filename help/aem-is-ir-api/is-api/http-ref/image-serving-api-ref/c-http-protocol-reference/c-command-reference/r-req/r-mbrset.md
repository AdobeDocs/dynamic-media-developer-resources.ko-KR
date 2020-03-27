---
description: 멀티비트 전송률 데이터
seo-description: 멀티비트 전송률 데이터
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mbrSet{#mbrset}

멀티비트 전송률 데이터

`req=mbrSet[,text|xml[, *`encoding`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 인코딩</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m| m3u8</span> </p></td> 
 </tr> 
</table>

net path ID와 연결된 비디오 세트의 유효한 비디오 항목에 해당하는 URL(및 해당 비트 전송률) 목록이 포함된 텍스트 또는 xml 응답을 반환합니다.

유효한 비디오 항목에 에 값이 들어 있다는 이전의 요구 사항이 `catalog::VideoBitRate` 이제 완화되었습니다. 항목에 `catalog::VideoBitRate`*또는&#x200B;*`catalog::AudioBitRate`*의* 값이 포함될 수 있습니다 `catalog::TotalStreamBitRate`. 비디오 항목이 유효하려면 이러한 항목 중 하나만 정의해야 합니다. 유효한 비디오 파일 확장명에 대한 요구 사항은 변경되지 `catalog::Path` 않았습니다.

응답은 Apple 및 Flash Streaming Server에서 사용하기 위한 것으로 이러한 사양에 구조적으로 부합됩니다. URL은 접두사와 `attribute::HttpAppleStreamingContext` 를 사용하여 생성됩니다 `attribute::HttpFlashStreamingContext`.

m3u8 응답에는 비디오 세트에 있는 경우 mp4 파일만 포함됩니다. mp4 파일이 없는 경우 이러한 응답에는 f4v 파일만 포함됩니다. mp4 파일 또는 f4v 파일이 없는 경우 응답은 비어 있습니다.

f4m 응답에는 비디오 세트에 있는 경우 f4v 파일만 포함됩니다. f4v 파일이 없는 경우 이러한 응답에는 mp4 파일만 포함됩니다. f4v 파일 또는 mp4 파일이 없는 경우 응답은 비어 있습니다.

f4m/m3u8 응답에 나타나는 비트 전송률은 의 값(적절한 단위로 `catalog::TotalStreamBitRate` 변환됨)에 해당합니다. 이 `catalog::TotalStreamBitRate` 정의되지 않은 경우, `catalog::VideoBitRate` 및 의 합계가 `catalog::AudioBitRate` 사용됩니다.

The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.
