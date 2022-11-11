---
description: 비디오에 대한 축소판 이미지를 생성합니다.
solution: Experience Manager
title: 미디어 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f37d935d-fe74-4878-8477-d2144d58d982
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 5%

---

# [!DNL MediaOptions]{#mediaoptions}

비디오에 대한 축소판 이미지를 생성합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:HandleArray</span> </td> 
   <td colname="col3">일련의 <span class="codeph"> PropertySet</span> 비디오 코드 변환 시 비디오 인코딩 사전 설정을 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:부울</span> </td> 
   <td colname="col3"> true이면 비디오의 첫 번째 프레임이 추출되어 축소판 이미지로 사용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 유형:ThumbnailOptions</span> </td> 
   <td colname="col3">선택 사항입니다. 축소판 이미지로 사용할 특정 비디오 프레임을 선택할 수 있습니다. <p>축소판 이미지를 지정하려면 사용할 프레임에 대한 시간(비디오 시작으로부터 밀리초)을 전달합니다. 값의 범위는 0부터 비디오 끝까지 입니다. <p>참고: 시간을 잘못 지정하면 <span class="codeph"> generateThumbnail</span> 기본값은 true입니다. </p></p><p>자세한 내용은 <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> 축소판 그림 옵션</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## 사용 대상 {#section-87cb83407198432c95eaa2db9f12f9db}

다음 `mediaOptions` 유형은 다음 방법으로 사용됩니다.

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
