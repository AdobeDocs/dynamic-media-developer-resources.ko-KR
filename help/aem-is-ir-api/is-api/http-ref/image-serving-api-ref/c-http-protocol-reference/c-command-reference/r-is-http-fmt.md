---
title: fmt
description: 응답 이미지 형식.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 9ed415c5ab4444a2d404782bfd96ded3c47c26cd
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 2%

---

# fmt{#fmt}

응답 이미지 형식.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | 높이 | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf 알파 | swf | swf3-alpha | swf3 | tif-alpha | tif | 웹 알파 | webp

| *`format`* | 설명 |
|---|---|
| `avif-alpha` | 알파 채널을 사용한 손실 및 무손실 AVIF. |
| `avif` | 손실 및 무손실 AVIF. |
| `eps` | 압축 해제된 바이너리 캡슐화된 PostScript입니다. |
| `f4m` | Flash 스트리밍 서버 매니페스트 형식입니다. |
| `gif-alpha` | 2~255색 및 키 색상 투명도가 포함된 GIF. |
| `gif` | 2~256색 GIF. |
| `heic` | 무손실 높이. 이 형식은 지원되지 않는 경우 브라우저에서 기본적으로 다운로드됩니다. |
| `jpeg` | 손실 JPEG. |
| `jpeg2000-alpha` | 알파 채널이 있는 손실 및 무손실 JPEG 2000. |
| `jpeg2000` | 손실 및 손실 없는 JPEG 2000. |
| `jpegxr-alpha` | 알파 채널이 있는 손실 및 무손실 JPEG XR. |
| `jpegxr` | 손실 및 무손실 JPEG XR. |
| `jpg` | 손실 JPG. |
| `m3u8` | Apple 스트리밍 서버 매니페스트 형식입니다. |
| `pdf` | 이미지가 PDF에 포함되었습니다. |
| `pjpeg` | 점진적 JPEG. |
| `png-alpha` | 알파 채널을 사용한 24비트 무손실 PNG. |
| `png` | 24비트 무손실 PNG. |
| `png8-alpha` | 알파 채널이 포함된 8비트 무손실 PNG. |
| `png8` | 8비트 무손실 PNG. |
| `swf-alpha` | 손실 JPEG과 수축 압축된 마스크가 Adobe AS2 swf 파일에 포함되어 있습니다. |
| `swf` | Adobe AS2 swf 파일에 포함된 손실 JPEG. |
| `swf3-alpha` | 손실 JPEG과 수축 압축된 마스크가 Adobe AS3 swf 파일에 포함되어 있습니다. **참고:** swf 및 swf 알파 형식은 ActionScript 2 응용 프로그램(Flash Player 8 이하)에 가장 잘 사용됩니다. swf3 및 swf3-alpha 형식은 ActionScript3 응용 프로그램(Flash Player 9 이상)에 사용하는 것이 좋습니다. |
| `swf3` | Adobe AS3 swf 파일에 포함된 손실 JPEG. |
| `tif-alpha` | 알파 채널을 사용하는 TIFF. |
| `tif` | TIFF. |
| `webp-alpha` | 알파 채널이 있는 손실 및 무손실 WebP. |
| `webp` | 손실 및 손실 없는 WebP. |

| *`pixelType`* - rgb | 회색 | cmyk |
| *`pixelType`* | 설명 |
|---|---|
| `cmyk` | CMYK 이미지 데이터를 반환합니다. |
| `gray` | 회색 음영 이미지 데이터를 반환합니다. |
| `rgb` | RGB 이미지 데이터를 반환합니다. |

| *`compression`* - jpeg | 손실 | 무손실 | lzw | 없음 | zip |
| *`compression`* | 설명 |
|---|---|
| `jpeg` | JPEG 압축(손실). |
| `lossy` | WebP, JPEG 2000 및 JPEG XR 압축(손실). |
| `lossless` | WebP, JPEG 2000 및 JPEG XR 압축(무손실). |
| `lzw` | LZW (Lempel-Ziv-Welch) 압축(무손실). |
| `none` | 압축이 해제되었습니다. |
| `zip` | &quot;수축&quot; 압축(무손실). |

* *`format`* 클라이언트로 보낸 이미지 데이터의 이미지 인코딩 형식을 지정하고 HTTP 응답 헤더의 해당 응답 MIME 형식을 지정합니다.
* *`pixelType`* 다음과 같은 경우에 출력 색상 공간 변환을 수행하는 데 사용할 수 있습니다. `icc=` 이(가) 지정되지 않았습니다.

  에 해당하는 기본 색상 프로파일 *`pixelType`* 이 적용됩니다. 색상 관리가 비활성화되어 있으면 순조로운 변환이 적용됩니다. *`pixelType`* 은(는) 다음의 경우 무시됩니다. `icc=` 출력 픽셀 유형을 결정하는 을 지정합니다.

* *`compression`* 은(는) 다음 경우에만 허용됩니다. `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`, 또는 `jpegxr-alpha` 은(는) (으)로 지정됩니다. *`format`*. 이러한 이미지 형식에 대해 지원되는 압축 옵션은 아래 표를 참조하십시오.

다음을 사용할 수 있습니다. `qlt=` JPEG, JPEG 압축을 사용한 TIFF, JPEG 압축을 사용한 PDF 및 SWF 형식에 대한 JPEG 인코딩 옵션을 설정합니다. WebP, JPEG 2000 및 JPEG XR에서도 `qlt=` 그러나 값은 다른 형식에 대해 다른 품질을 초래합니다. 사용 `quantize=` if `fmt=gif` 또는 `fmt=gif-alpha`. 자세한 내용은 명령 설명을 참조하십시오. 다른 형식에는 설정 가능한 옵션이 없습니다.

픽셀 구성 요소당 8비트가 모두 반환됩니다 *`formats`* 및 *`pixelTypes`* (GIF 시 픽셀당 8비트).

다음 표에는 유효한 * 조합이 나열되어 있습니다.`format`*및 *`pixelType`*, 해당 HTTP 응답 MIME 유형, ICC 프로필 포함 여부(참조) [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) 및 적용할 수 있는 형식별 옵션

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 형식</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> 응답 MIME 유형</b> </th> 
   <th class="entry"> <b>ICC 프로파일 포함</b> </th> 
   <th class="entry"> <b> 옵션</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>다음 <span class="codeph"> pscan= </span> 매개 변수는 pjpeg 형식에만 적용됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 압축 </span> </span> <p> ( <span class="codeph"> 없음|lzw|zip|jpeg </span>) </p> <p>'tiff'만 해당. 'tiff-alpha'는 jpeg 압축을 지원하지 않습니다. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 다음 경우가 아니면 무시됩니다. <span class="varname"> 압축 </span> 이(가) (으)로 설정됨 <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>아니요 </p> <p> <p>참고: Adobe Flash Player은 임베드된 ICC 프로파일을 무시합니다. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> 압축 </span> </span> <p> ( <span class="codeph"> 없음|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> 다음 경우가 아니면 무시됩니다. <span class="codeph"> <span class="varname"> 압축 </span> </span> 이(가) (으)로 설정됨 <span class="codeph"> jpeg </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, 회색, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>예 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, 회색 </p> <p>데이터는 회색 또는 rgb로 변환된 후 팔레트로 변환됩니다. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>아니요 </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> 압축 </span> </span> ( <span class="codeph"> 손실 </span>, <span class="codeph"> 무손실 </span>) </p> <p> <span class="codeph"> qlt= </span> 다음에 대해 무시됨 <span class="codeph"> 무손실 </span>. </p> <p>WebP 형식을 사용하는 색차 다운샘플링의 개념이 없으므로 <span class="codeph"> qlt </span> (예: <span class="codeph"> qlt=80,1 </span>) 두 번째 값( <span class="codeph"> 1 </span>)은 무시됩니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, 회색 </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p>위와 같습니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p>위와 같습니다. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>아니요 </p> </td> 
   <td> <p>위와 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

요청 속성입니다. 다음과 같은 경우 현재 레이어 설정에 관계없이 적용됩니다. `req=img` (기본값) 또는 `req=mask`; 그렇지 않으면 무시됩니다.

*`type`* 은 다음과 같은 경우 무시됩니다 `iccProfile=` 이(가) 지정되었습니다.

## 기본값 {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, 여기서 *`defaultType`* 는 다음과 같이 처리됩니다. `icc=` 을(를) 지정했습니다. *`defaultType`* 지정된 ICC 프로파일의 픽셀 유형에 해당합니다. If `icc=` 이(가) 지정되지 않았습니다. *`defaultType`* 은(는) `gray` if `req=mask`, 그렇지 않은 경우 `rgb`.

## 예제 {#section-b93222e652df404a84c69025247f07df}

**JPEG 형식(기본값)으로 작은 저품질 미리 보기 이미지 요청:**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**회색으로 변환된 동일한 이미지를 요청합니다.**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**알파 채널을 사용하여 고해상도로 손실 없는 형식으로 동일한 이미지를 요청합니다.**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**회색 음영 TIFF 이미지와 동일한 이미지에 대해 알파 채널을 요청합니다.**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**기본 ICC 프로파일을 사용하여 동일한 이미지를 cmyk로 변환합니다.**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**다른 ICC 프로파일을 사용하여 동일한 이미지를 cmyk로 변환하고 프로파일을 TIFF 이미지에 포함합니다.**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**픽셀 유형 변환 없이 JPEG 압축을 사용하여 이 이미지를 TIF 파일로 제공합니다.**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**이미지를 키 색상 투명도를 사용하는 두 가지 색상 GIF으로 변환하고 색상을 검정과 흰색으로 강제 변환합니다.**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**품질 설정이 80인 손실:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**알파 포함 무손실:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**품질 설정이 80인 손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**알파 포함 무손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**품질 설정이 80인 손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**알파 포함 무손실:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## 참조 {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
