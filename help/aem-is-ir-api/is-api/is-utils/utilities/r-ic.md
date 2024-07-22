---
description: 이미지 변환 유틸리티.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# ic {#ic}

이미지 변환 유틸리티.

`ic`은(는) 이미지 파일을 최적화된 PTIFF(피라미드 TIFF 형식)로 변환하는 명령줄 도구입니다. 이미지 제공은 변환 없이 이미지를 처리할 수 있지만 512x512 픽셀보다 큰 모든 이미지를 PTIFF로 변환하는 것이 좋습니다. 이 변환은 최적의 서버 성능과 리소스 사용을 보장하며 응답 시간을 최소화합니다.

사진 콘텐츠가 포함된 PTIFF 파일은 JPEG 인코딩되는 것이 좋습니다(`-jpegcompress` 지정). 컴퓨터 생성 콘텐츠는 무손실 압축(`-deflatecompress` 또는 `-lzwcompress`)을 활용할 수 있습니다. 컬러 변환 또는 픽셀 타입 변환이 필요하지 않는 한, JPEG 소스 이미지 데이터는 품질 저하를 피하기 위해 디코딩 없이 PTIFF로 전달된다. 이 경우, 지정된 압축 옵션은 낮은 해상도 피라미드 레벨에만 적용됩니다.

큰 이미지를 변환하지 않는 경우에는 사용할 메모리 양을 제어하는 매개 변수를 설정할 필요가 없습니다. 그러나 필요한 경우 아래에 설명된 `-maxmem` 설정을 사용하여 `ic`에 더 많은 메모리를 제공하십시오. 필요한 메모리의 양을 계산하는 좋은 방법은 이미지의 폭과 이미지의 높이를 곱하고 채널 수를 곱하는 것입니다. 예를 들어 알파 곱하기 3이 있는 RGB 이미지의 경우 4입니다. 또한 채널이 구성 요소당 8개가 아닌 16비트인 경우 최종 결과의 두 배가 됩니다.

## 사용 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>옵션</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>명령 옵션(아래 참조) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>단일 입력 이미지 파일입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>단일 출력 PTIFF 파일(SourceDirectory와 함께 사용되는 경우 유효하지 않음). </p> </td> 
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

성공하면 0입니다. 오류가 발생하면 0이 아닌 값이 반환되고 오류 세부 정보가 `stderr`(으)로 전송됩니다.

## 옵션 {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -압축되지 않음 </span> </p> </td> 
   <td colname="col2"> <p>출력 이미지를 압축하지 마십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>수축(zip) 압축(기본값)을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Lempel-Ziv-Welch(LZW) 압축을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG 인코딩을 사용하십시오. <span class="codeph"> <span class="varname"> sourceFile </span> </span>에 알파 데이터가 포함된 경우 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> 품질 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG 품질(0~100, 기본값은 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>JPEG 크로마 다운샘플링을 비활성화합니다(색상 텍스트 및 그래픽의 품질을 향상시킬 수 있음). 이는 CMYK 또는 회색 음영인 출력 이미지에는 영향을 주지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> 금액 </span>&gt; &lt; <span class="varname"> 반경 </span>&gt; &lt; <span class="varname"> 임계값 </span>&gt; &lt; <span class="varname"> 단색 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>하위 샘플링된 피라미드 레벨에 언샵 마스킹을 적용합니다. 자세한 내용은 <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a>을(를) 참조하십시오. (전체 해상도 이미지에는 적용되지 않습니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>소스 파일의 클립 경로(있는 경우)를 사용하여 연결된 알파 데이터를 생성합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> <span class="varname"> destFile </span> </span>에 대한 dpi(인쇄 해상도)입니다. 지정하지 않으면 <span class="codeph"> srcFile </span>의 인쇄 해상도가 <span class="codeph"> <span class="varname"> destFile </span> </span>에 복사됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> 모드 </span>&gt; &lt; <span class="varname"> tolerance </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>자르기 사각형을 계산하여 단색 배경을 최소화합니다. 자동 자르기 알고리즘으로 인해 전체 이미지가 잘리는 경우 자르기 정보가 출력되지 않습니다. </p> <p>이미지를 변환하지 않고 자르기 사각형을 계산하려면 <span class="codeph"> -autocrop </span>을(를) <span class="codeph"> -convert </span> 없이 지정하고 <span class="codeph"> <span class="varname"> destFile 없이 지정하십시오.</span> </span></p>

<p><i><b>모퉁이</b></i> - ul | 우르 | ll | lr </p>
   <p> 시드 점을 사용할 이미지의 모서리를 지정합니다. 모드가 1인 경우 무시됩니다.</p>
   <p><i><b>모드</b></i> - 0 | 1</p>
   <p>지정된 모서리 픽셀의 색상을 기준으로 자르려면 0으로 설정합니다. 알파 데이터가 소스 이미지와 연결되어 있으면 미리 곱해진 색상 데이터에서 작동합니다.</p>
   <p>알파 데이터를 기반으로 자르려면 1로 설정합니다. 코너는 무시되고 항상 0이 시드 값입니다. 소스 이미지와 연결된 알파 데이터가 없으면 자르기가 적용되지 않습니다.</p> 
   <p><i><b>허용 오차</b></i> - 일치 허용 오차입니다. 실수 값 0.0 ~ 1.0. 일치하는 픽셀 구성 요소 값에 대한 공차를 지정합니다. 정확히 일치하려면 0으로 설정합니다.</p>
   <p><i><b>infoFile</b></i> - 자르기 정보 데이터가 기록되는 XML 출력 파일의 경로 및 이름입니다.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>가능한 경우 수정 없이 <span class="codeph"> <span class="varname"> sourceFile </span> </span>에서 <span class="codeph"> <span class="varname"> destFile </span> </span>(으)로 XMP 메타데이터를 복사합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 사용 가능한 경우 <span class="codeph"> <span class="varname"> destFile </span> </span>에 ICC 색상 프로파일을 포함하십시오(기본적으로 포함된 프로파일이 없음). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> 파일 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC 프로파일 파일의 경로 및 이름입니다. <span class="codeph"> <span class="varname"> sourceFile </span> </span>의 색상 공간을 정의하며 해당 픽셀 유형과 일치해야 합니다. <span class="codeph"> <span class="varname"> sourceFile </span> </span>에 포함된 프로필이 없는 경우에만 지정해야 합니다. 이는 포함된 프로필을 무시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> 파일 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC 프로파일 파일의 경로 및 이름입니다. <span class="codeph"> <span class="varname"> destFile </span> </span>의 픽셀 유형과 색상 공간을 정의합니다. <span class="codeph"> <span class="varname"> sourceFile </span> </span>에 포함된 프로필이 있거나 <span class="codeph"> -imageprofile </span>이(가) 지정된 경우 IC가 이 프로필로 전환됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>색상 공간 변환에 대한 가시 범위 렌더링 의도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> 색상 공간 변환에 대한 상대 색상 지표 렌더링 의도(기본값). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>색상 공간 변환에 대한 절대 색상 지표 렌더링 의도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>색상 공간 변환에 대한 채도 렌더링 의도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>특정 색상 변환에 대한 검은 점 보상 비활성화 </p> <p>기본적으로 활성화되어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>색상 변환 시 디더링(오류 확산)을 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> CMYK에서 RGB으로 자동 전환을 비활성화합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>JPEG 입력 이미지의 강제 디코딩 및 다시 인코딩. </p> <p> <b>주의:</b> 이 옵션을 적용하면 이미지 품질이 저하될 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>표준 품질(이중선형) 리샘플링 필터를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>고품질(Lanczos 창) 리샘플링 필터(기본값)를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>고품질(FlashPix) 리샘플링 필터를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Photoshop 스타일 8x8 bicubic-sharp 필터를 사용하여 다운샘플링합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> 첫 번째 옵션으로 지정한 경우 잘못된 옵션이 발견되면 사용 정보의 출력을 억제합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -덮어쓰기 </span> </p> </td> 
   <td colname="col2"> <p>기존 <span class="codeph"> <span class="varname"> destFile </span> </span>을(를) 덮어쓸 수 있습니다. 기본적으로 덮어쓰기를 방지하기 위해 파일 이름에 숫자 접미사가 추가됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>숨겨진 소스 파일 무시. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>오류가 발생할 때 처리를 중지하지 마십시오. 은 여러 파일을 처리할 때에만 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> 파일 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>로그 파일의 경로 및 이름(기본값: <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> 수준 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>로그 수준. </p> 
   <p>&lt; 0 - 로깅이 비활성화되었습니다.</p>
   <p>0 - 처리할 파일을 나열합니다.</p>
   <p>1 - 불필요한 파일에 대한 보고를 추가합니다.</p>
   <p>2 - 진행 상황 보고를 추가합니다.</p>
   <p>3 - 발생한 모든 파일에 대한 보고를 추가합니다.</p>
   <p>4 - 파일 수준에서 진행 상황 보고를 추가합니다.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>로그 파일에 추가(기본값). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>로그 파일을 덮어씁니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogresmsec &lt; <span class="varname">밀리초 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>로그 수준 2 이상에 대한 로깅 간격(밀리초)(기본값은 3000)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname">바이트 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>메모리 사용 제한. 10MB 이상이어야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>메모리 사용 제한. 기본값은 물리적 메모리의 25%입니다. <span class="codeph"> maxmem </span>과(와) <span class="codeph"> maxmempercent </span>이(가) 명시적으로 설정되지 않은 경우 maxmempercent 기본값을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -버전 </span> </p> </td> 
   <td colname="col2"> <p> 이 유틸리티의 버전 정보를 반환합니다. 다른 옵션을 사용하지 않고 을(를) 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 지원되는 입력 이미지 형식 {#section-ab13d941d6724e65b9f84b62d949d31c}

다음 표에는 IC에서 지원되는 이미지 파일 형식과 형식 옵션이 나와 있습니다.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 형식</b> </p> </th> 
   <th class="entry"> <p> <b> 픽셀 유형</b> <b>비트/Chan</b> </p> </th> 
   <th class="entry"> <p> <b>비트/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> 압축</b> </p> </th> 
   <th class="entry"> <p> <b>개 메모</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows 비트맵) </p> </td> 
   <td> <p> RGB | 색인화됨 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 압축 해제됨 | RLE </p> </td> 
   <td> <p> 5/6비트/채널은 16비트 RGB(5-5-5 및 5-6-5비트/채널)에 대한 지원을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
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
   <td> <p> 컴푸서브 </p> <b>GIF</b> </td> 
   <td> <p> 색인화됨 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 팔레트의 투명도 값이 있으면 알파로 변환됩니다. </p> </td> 
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
   <td> <p> CMYK | CMYKA | RGB | RGBA | 회색 | 회색 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 압축 해제됨 | 압축됨 </p> </td> 
   <td> <p> 병합된 이미지만 포함되고 레이어와 추가 채널은 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> 비트맵 데이터만 포함되고, 벡터 데이터는 무시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | 회색 | 회색 | 색인화됨 </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 압축 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | 회색 | 회색 | 색인화됨 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 압축 해제됨 | ZIP | LZW | JPEG | CCITT 규칙 | CCITT G3 | CCITT G4 | 패키지 비트 </p> </td> 
   <td> <p> 첫 번째 연결된 알파 채널을 제외하고 추가 채널은 무시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

포함된 ICC 프로파일은 EPS, JPG, PSD, PNG 및 TIFF 파일에서 인식됩니다.

포함된 경로와 XMP 메타데이터는 EPS, JPG, PSD 및 TIFF 파일에서 인식됩니다.

## 예제 {#section-3c1986b30315431989bd76b1ee5bef6d}

최상의 품질로 단일 이미지를 변환하고 동일한 폴더에 보관합니다.

`ic -convert src/myFile.png src/myFile.tif`

*`srcFolder`*&#x200B;의 모든 이미지를 JPEG으로 인코딩된 피라미드 TIFF으로 변환하고 *`destFolder`*&#x200B;에 배치합니다.

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

*`srcFolder`*&#x200B;의 모든 이미지를 변환합니다. JPG 파일의 인코딩된 이미지 데이터는 이러한 이미지의 나머지 이미지 피라미드뿐만 아니라 모든 비 JPG 입력 파일의 전체 출력 이미지에 대해 전체 해상도 레벨의 손실 없는 LZW 압축에 사용됩니다. 픽셀 유형, 임베드된 색상 프로파일, XMP 메타데이터 등. 유지 관리됩니다.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
