---
description: ZIP 및 TAR 파일을 마스터 에셋으로 처리하거나(없음) 내용을 추출하여 업로드(압축 해제)합니다.
seo-description: ZIP 및 TAR 파일을 마스터 에셋으로 처리하거나(없음) 내용을 추출하여 업로드(압축 해제)합니다.
seo-title: 압축 해제 옵션
solution: Experience Manager
title: 압축 해제 옵션
topic: Scene7 Image Production System API
uuid: 1e6827db-8c5e-47db-b7ff-4e681e107e57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 압축 해제 옵션{#uncompressoptions}

ZIP 및 TAR 파일을 마스터 에셋으로 처리하거나(없음) 내용을 추출하여 업로드(압축 해제)합니다.

>[!NOTE]
>
>`None` 가 기본값입니다.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 프로세스</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> <p>ZIP 및 TAR 아카이브 파일 처리를 제어합니다. 다음 두 가지 옵션을 제공합니다. 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> 없음:</span> 마스터 자산으로 처리 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> 압축 해제:</span> 컨텐츠 추출 및 처리 </li>
     </ul><p>참고:문자열 상수는 대소문자를 구분합니다. 압축 <span class="codeph"> 해제</span>, <span class="codeph"> 압축</span> 해제 <span class="codeph"> 또는 압축 해제</span>대신 UnCompress를 사용하십시오. </p></p> </td> 
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

## 사용 방법 {#section-b2a829cf5511412e968bb2000f85cc31}

이 `unCompressionOptions` 유형은 다음과 같이 사용됩니다.

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrl작업](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

