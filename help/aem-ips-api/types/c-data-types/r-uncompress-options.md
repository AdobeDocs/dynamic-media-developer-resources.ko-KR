---
description: ZIP 및 TAR 파일을 기본 자산(없음)으로 처리하거나 컨텐츠를 추출하여 업로드(압축 해제)합니다.
seo-description: ZIP 및 TAR 파일을 기본 자산(없음)으로 처리하거나 컨텐츠를 추출하여 업로드(압축 해제)합니다.
seo-title: UnCompressOptions
solution: Experience Manager
title: UnCompressOptions
topic: Scene7 Image Production System API
uuid: 1e6827db-8c5e-47db-b7ff-4e681e107e57
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 4%

---


# UnCompressOptions{#uncompressoptions}

ZIP 및 TAR 파일을 기본 자산(없음)으로 처리하거나 컨텐츠를 추출하여 업로드(압축 해제)합니다.

>[!NOTE]
>
>`None` 기본값은 기본값입니다.

## 매개 변수 {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 프로세스</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>ZIP 및 TAR 아카이브 파일 처리를 제어합니다. 다음 두 가지 옵션을 제공합니다. 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> 없음:</span> 기본 자산으로 처리 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> 압축 해제:</span> 컨텐츠 추출 및 처리 </li>
     </ul><p>참고: 문자열 상수는 대/소문자를 구분합니다. 압축해제 <span class="codeph"> 또는</span>압축해제 <span class="codeph"> 가 아니라 압축 해제</span> 를 <span class="codeph"> 사용하십시오</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## 사용한 사람 {#section-b2a829cf5511412e968bb2000f85cc31}

이 `unCompressionOptions` 유형은 다음과 같이 사용됩니다.

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

