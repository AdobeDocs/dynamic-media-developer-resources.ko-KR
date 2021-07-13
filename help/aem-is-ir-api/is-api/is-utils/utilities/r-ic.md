---
description: 이미지 변환 유틸리티입니다.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 2%

---

# ic {#ic}

이미지 변환 유틸리티입니다.

`ic` 는 이미지 파일을 최적화된 피라미드 TIFF 형식(PTIFF)으로 변환하는 명령줄 도구입니다. 이미지 제공 서비스는 변환 없이 이미지를 처리할 수 있지만 512x512픽셀보다 큰 모든 이미지를 PTIFF로 변환하는 것이 좋습니다. 이렇게 변환하면 최적의 서버 성능과 리소스 사용이 보장되며 응답 시간이 최소화됩니다.

사진 내용이 포함된 PTIFF 파일은 JPEG로 인코딩되는 것이 좋습니다( `-jpegcompress` 지정). 컴퓨터에서 생성한 콘텐츠는 손실 없는 압축(`-deflatecompress` 또는 `-lzwcompress`)을 통해 얻을 수 있습니다. 색상 변환이나 픽셀 유형 변환이 필요하지 않으면 JPEG 소스 이미지 데이터가 디코딩 없이 PTIFF로 전송되어 품질 저하를 방지합니다. 이 경우 지정된 압축 옵션은 낮은 해상도 피라미드에만 적용됩니다.

큰 이미지를 변환하지 않는 경우 사용할 메모리 양을 제어하는 매개 변수를 설정할 필요가 없습니다. 그러나 필요한 경우 아래 설명된 `-maxmem` 설정을 사용하여 `ic` 메모리를 더 제공하십시오. 필요한 메모리 양을 계산하기 위한 좋은 경험의 법칙은 이미지 너비와 이미지 높이를 채널 수와 곱하는 것입니다. 예를 들어, 알파 곱이 3인 RGB 이미지의 경우 4입니다. 또한 채널이 최종 결과의 8배 대신 구성 요소당 16비트인 경우

## 사용 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>옵션</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>명령 옵션(아래 참조). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>단일 입력 이미지 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>단일 출력 PTIFF 파일(SourceDirectory에서 사용하는 경우 유효하지 않음)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>입력 이미지가 포함된 폴더입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>출력 PTIFF 파일이 작성된 폴더입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-36a2dcfa39824d29b69547c432366219}

성공할 경우 0입니다. 오류가 발생하면 0이 아닌 값이 반환되고 오류 세부 정보가 `stderr`으로 전송됩니다.

## 옵션 {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -압축 해제됨 </span> </p> </td> 
   <td colname="col2"> <p>출력 이미지를 압축하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress  </span> </p> </td> 
   <td colname="col2"> <p>deflate(zip) 압축(기본값)을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>Lempel-Ziv-Welch(LZW) 압축을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>JPEG 인코딩을 사용하십시오. <span class="codeph"> <span class="varname"> sourceFile </span> </span>에 알파 데이터가 포함된 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>JPEG 품질(0-100; 기본값은 95)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplecrominance  </span> </p> </td> 
   <td colname="col2"> <p>JPEG 색상 다운샘플링을 사용하지 않도록 설정합니다(색상 텍스트 및 그래픽의 품질을 향상시킬 수 있음). CMYK 또는 회색 명암 출력 이미지에는 영향을 주지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt;  &lt;&gt; threshold  </span>&gt;  &lt;&gt; monochrome  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>하위 샘플링된 피라미드 레벨에 언샵 마스킹을 적용합니다. 자세한 내용은 <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> 을 참조하십시오. (전체 해상도 이미지에는 적용되지 않습니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>소스 파일의 클립 경로(있는 경우)를 사용하여 연결된 알파 데이터를 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span>에 대한 인쇄 해상도(dpi) 지정하지 않으면 <span class="codeph"> srcFile </span>의 인쇄 해상도가 <span class="codeph"> <span class="varname"> destFile </span> </span>에 복사됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop  &lt;&gt; 코너  </span>&gt;  &lt;&gt; 모드  </span>&gt;  &lt;&gt; tolerance  </span>&gt;  &lt;&gt; infoFile  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>자르기 사각형을 계산하여 단색 배경을 최소화합니다. 자동 자르기 알고리즘으로 전체 이미지가 잘리는 경우 자르기 정보가 출력되지 않습니다. </p> <p>이미지를 변환하지 않고 자르기 사각형을 계산하려면 <span class="codeph"> -autocrop </span> 없이 <span class="codeph"> -convert </span> <span class="codeph"> <span class="varname"> destFile.</span> </span> 을 지정하지 마십시오</p>

<p><i><b>모퉁이</b></i>  - ul | url | ll | lr </p>
   <p> 시드 점을 사용할 이미지의 모서리를 지정합니다. 모드가 1이면 무시됩니다.</p>
   <p><i><b>모드</b></i>  - 0 | 1</p>
   <p>지정된 코너 픽셀의 색상을 기준으로 자르려면 0으로 설정합니다. 알파 데이터가 소스 이미지와 연결된 경우 미리 곱된 색상 데이터에서 작동합니다.</p>
   <p>알파 데이터를 기반으로 자르려면 1로 설정합니다. 모서리는 무시되고 0은 항상 시드 값입니다. 소스 이미지와 연결된 알파 데이터가 없으면 자르기가 적용되지 않습니다.</p> 
   <p><i><b>허용치</b></i>  - 일치 허용치. 실수 값 0.0에서 1.0까지 일치하는 픽셀 구성 요소 값에 대한 허용치를 지정합니다. 정확히 일치하려면 0으로 설정합니다.</p>
   <p><i><b>infoFile</b></i>  - 자르기 정보 데이터를 쓸 XML 출력 파일의 경로 및 이름입니다.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>가능한 경우 XMP 메타데이터를 <span class="codeph"> <span class="varname"> sourceFile </span> </span>에서 <span class="codeph"> <span class="varname"> destFile </span> </span>로 수정 없이 복사합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> 사용 가능한 경우 <span class="codeph"> <span class="varname"> destFile </span> </span>에 ICC 색상 프로파일을 포함합니다(기본적으로 프로필이 포함되지 않음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; 파일  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICC 프로필 파일의 경로 및 이름입니다. <span class="codeph"> <span class="varname"> sourceFile </span> </span>의 색상 공간을 정의하며 해당 픽셀 유형과 일치해야 합니다. 이 경우 포함된 프로필을 재정의하므로 <span class="codeph"> <span class="varname"> sourceFile </span> </span>에 포함된 프로필이 없는 경우에만 지정해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile  &lt;&gt; 파일  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>ICC 프로필 파일의 경로 및 이름입니다. <span class="codeph"> <span class="varname"> destFile </span> </span>의 픽셀 유형 및 색상 공간을 정의합니다. <span class="codeph"> <span class="varname"> sourceFile </span> </span>에 포함된 프로필이 있거나 <span class="codeph"> -imageprofile </span>도 지정된 경우 IC가 이 프로필로 변환됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual  </span> </p> </td> 
   <td colname="col2"> <p>색상 공간 변환에 대한 지각 렌더링 의도 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimmetric  </span> </p> </td> 
   <td colname="col2"> <p> 색상 공간 변환을 위한 상대적 색상 지표 렌더링 의도(기본값). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimmetric  </span> </p> </td> 
   <td colname="col2"> <p>색상 공간 변환을 위한 절대 색상 지표 렌더링 의도 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>채도 렌더링은 색상 공간 변환에 대한 의도 렌더링입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>특정 색상 변환에 대한 블랙포인트 보상 비활성화 </p> <p>기본적으로 활성화됨. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>색상 변환 시 디더링(오류 확산)을 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintaxeltype  </span> </p> </td> 
   <td colname="col2"> <p> CMYK에서 RGB로 자동 변환을 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>JPEG 입력 이미지의 강제 디코딩 및 재인코딩. </p> <p> <b>주의:</b> 이 옵션을 적용하면 이미지 품질이 저하될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>표준 품질(양방향) 리샘플링 필터를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>고품질(Lanczos 창) 재샘플링 필터(기본값)를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>고품질(FlashPix) 리샘플링 필터를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp  </span> </p> </td> 
   <td colname="col2"> <p>Photoshop 스타일 8x8 쌍방-예프 필터를 사용한 다운샘플입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> 첫 번째 옵션으로 지정되면 잘못된 옵션이 발생할 때 사용 정보의 출력을 억제합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -덮어쓰기 </span> </p> </td> 
   <td colname="col2"> <p>기존 <span class="codeph"> <span class="varname"> destFile </span> </span>을(를) 덮어쓸 수 있습니다. 기본적으로 파일 이름에 숫자 접미사가 추가되어 덮어쓰기를 방지합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden  </span> </p> </td> 
   <td colname="col2"> <p>숨겨진 소스 파일을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror  </span> </p> </td> 
   <td colname="col2"> <p>오류가 발생할 때 처리를 중지하지 마십시오. 은 여러 파일을 처리할 때만 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; 파일  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>로그 파일의 경로 및 이름(기본값은 <span class="codeph"> stdout </span>)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel  &lt;&gt; level  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>로그 수준. </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 - 처리할 파일을 나열합니다.</p>
   <p>1 - 불필요한 파일에 대한 보고 추가.</p>
   <p>2 - 진행률 보고 추가</p>
   <p>3 - 발생한 모든 파일에 대한 보고를 추가합니다.</p>
   <p>4 - 파일 수준에서 진행 보고를 추가합니다.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>로그 파일에 추가(기본값). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>로그 파일을 덮어씁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>로그 수준 2 이상의 로깅 간격(기본값은 3000)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; 바이트  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>메모리 사용 제한. 10MB 이상이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent  &lt;&gt; 퍼센트  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>메모리 사용 제한. 기본값은 실제 메모리의 25%입니다. <span class="codeph"> maxmem </span> 및 <span class="codeph"> maxmempercent </span>가 명시적으로 설정되지 않으면 maxmempercent 기본값을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -버전 </span> </p> </td> 
   <td colname="col2"> <p> 이 유틸리티에 대한 버전 정보를 반환합니다. 다른 옵션 없이 을 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 지원되는 입력 이미지 형식 {#section-ab13d941d6724e65b9f84b62d949d31c}

다음 표에는 IC에서 지원하는 이미지 파일 형식 및 형식 옵션이 나와 있습니다.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 형식</b> </p> </th> 
   <th class="entry"> <p> <b> 픽셀 </b> <b> 유형Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> 비트/찬</b> </p> </th> 
   <th class="entry"> <p> <b> 압축</b> </p> </th> 
   <th class="entry"> <p> <b> 주의</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows 비트맵) </p> </td> 
   <td> <p> RGB | 색인화됨 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 압축되지 않음 | RLE </p> </td> 
   <td> <p> 5/6비트/채널은 16비트 RGB(5-5-5 및 5-6-5 비트/채널)에 대한 지원을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (캡슐화된 포스트스크립트) </p> </td> 
   <td> <p> CMYK | RGB | 회색 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | 이진 | JPEG </p> </td> 
   <td> <p> Photoshop에서 생성한 EPS 파일만 지원됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> 인덱싱된 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 있는 경우 팔레트의 투명도 값이 알파로 변환됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | 회색 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | 회색 | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 압축되지 않음 | 압축 </p> </td> 
   <td> <p> 병합된 이미지만 레이어 및 추가 채널은 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> 비트맵 데이터 전용, 벡터 데이터는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | 회색 | grayA | 색인화됨 </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 압축 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | 회색 | grayA | 색인화됨 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 압축되지 않음 | ZIP | LZW | JPEG | CCITT RLE | CCITT G3 | CCITT G4 | Packbit </p> </td> 
   <td> <p> 연결된 첫 번째 알파 채널을 제외하고 추가 채널은 무시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

포함된 ICC 프로파일은 EPS, JPG, PSD, PNG 및 TIFF 파일에서 인식됩니다.

포함된 경로 및 XMP 메타데이터는 EPS, JPG, PSD 및 TIFF 파일에서 인식됩니다.

## 예제 {#section-3c1986b30315431989bd76b1ee5bef6d}

단일 이미지를 최상의 품질로 변환하여 동일한 폴더에 유지합니다.

`ic -convert src/myFile.png src/myFile.tif`

*`srcFolder`*&#x200B;의 모든 이미지를 JPEG로 인코딩된 피라미드 TIFF로 변환하고 *`destFolder`*&#x200B;에 배치합니다.

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

*`srcFolder`*&#x200B;의 모든 이미지를 변환합니다. JPG 파일의 인코딩된 이미지 데이터는 모든 JPG 입력 파일의 전체 출력 이미지와 이 이미지의 나머지 이미지 피라미드의 전체 해상도, 손실 없는 LZW 압축에 사용됩니다. 픽셀 유형, 포함된 색상 프로필, XMP 메타데이터 등 가 유지 관리됩니다.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
