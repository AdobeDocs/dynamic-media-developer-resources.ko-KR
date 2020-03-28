---
description: sourceFile 유형에 관계없이 다음 옵션을 적용할 수 있습니다.
seo-description: sourceFile 유형에 관계없이 다음 옵션을 적용할 수 있습니다.
seo-title: 일반적인 옵션
solution: Experience Manager
title: 일반적인 옵션
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 일반적인 옵션{#common-options}

sourceFile 유형에 관계없이 다음 옵션을 적용할 수 있습니다.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>출력 파일을 배치할 폴더( <span class="codeph"> -log가 </span> 지정된 경우 로그 파일 포함). 절대 경로이거나 현재 작업 디렉토리의 상대 경로일 수 있습니다. 폴더 계층 구조는 존재하지 않으면 만들어집니다. -log로 지정된 파일에는 적용되지 <span class="codeph"> 않습니다 </span>. 지정하지 않으면 소스 파일이 <span class="varname"> 있는 폴더에 출력 파일이 </span> 작성됩니다. dest <span class="varname"> 파일을 </span> 지정하면 항상 해당 위치에 기록되며 <span class="codeph"> -destpath는 보조 출력 파일에만 </span> 적용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -이미지 </span> </p> </td> 
  <td class="stentry"> <p>If specified, the (first) view image is extracted from the vignette, a suitable panel image from a cabinet style, or the first illumination image of a window covering style. 압축을 푼 이미지는 전체 해상도 TIFF 파일로 저장됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>대상 파일의 생성을 방지합니다. 소스 파일에서 속성을 빠르게 추출하는 데 <span class="varname"> 유용합니다 </span>. 선택적인 축소판( <span class="codeph"> -thumbwidth </span>), 이미지( <span class="codeph"> -image </span>) 및 로그 파일( <span class="codeph"> -log </span>)만 생성됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>손실 없는 PNG 대신 출력 파일에 임베드된 RGB 및 회색 음영 이미지 데이터의 손실 JPEG 인코딩을 선택합니다. 알파(RGBA)가 있는 이미지는 항상 PNG 인코딩을 사용하여 저장됩니다. <span class="varname"> ival </span> 은 JPEG 품질(1...100)을 지정합니다.85 이상이 권장됩니다. 기본값은 <span class="codeph"> -jpegquality 0이며, PNG </span>인코딩을 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> 경로 </span></span> </p> </td> 
  <td class="stentry"> <p>Creates a log file with the specified path/name The full paths of all output files written to the destination folder are written to the log file, as well as some additional settings, such as version info and any warnings or errors encountered (see <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> for details). -log를 지정하지 않으면 <span class="codeph"> 로그 파일이 만들어지지 </span> 않습니다.이 경우 모든 텍스트 출력이 <span class="codeph"> stdout으로 기록됩니다 </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>vntc 프로세스의 우선 순위를 <span class="filepath"> 낮춥니다 </span> . This can be used so that <span class="filepath"> vntc </span> won't take over an entire CPU while processing a vignette. It allows the operating system to give more time to other, more important, processes. <span class="varname"> ival </span> specifies the lower priority percentage (0..100). 기본값은 <span class="codeph"> -lower priority 0 </span>으로, vntc <span class="filepath"> 프로세스의 우선 순위를 낮추지 않습니다 </span> . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>vntc가 바이트 단위로 사용할 수 <span class="filepath"> 있는 최대 메모리 양을 </span> 지정합니다. vntc <span class="filepath"> 가 최대 메모리 </span> 제한에 도달하면 처리가 중지되고 오류가 발생합니다. <span class="varname"> ival </span> 은 최대 메모리 제한(바이트)을 지정합니다(0... 3,758,096,384(3.5GB)). ival <span class="varname"> 이 </span> 0이면 최대 메모리 제한이 해제됩니다. 기본값은 <span class="codeph"> -maxmem 3221225472이며 </span>, 최대 메모리 제한은 3GB입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>자동 생성된 출력 파일 이름에 대한 파일 이름과 크기/해상도 접미어 사이에 배치된 구분 기호를 지정합니다. 지정하지 않은 경우 기본값은 "-"입니다. dest <span class="varname"> File </span> 또는 <span class="codeph"> -info가 </span> 지정된 경우 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -선명 <span class="varname"> 효과 </span></span> </p> </td> 
  <td class="stentry"> <p>처리 중에 다시 샘플링된(크기 조절된) 이미지를 선명하게 할 수 있습니다. 캐비닛 스타일 파일의 경우 축소판 선명하게 기능에만 적용됩니다. </p> <p>선명 효과를 비활성화하려면 0(기본값), 일반 선명 효과를 활성화하려면 1, 밝기에만 대해 언샵 마스킹을 활성화하려면 2, 각 색상 구성 요소에 대해 언샵 마스킹을 활성화하려면 3을 지정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>로그 수준을 설정합니다. Default is 1, which outputs all informational, warning, and error messages. Set to 0 to disable all but error messages. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> amount </span> <span class="varname"> radius </span> <span class="varname"> threshold </span> </span> </p> </td> 
  <td class="stentry"> <p>Sets the unsharp-masking parameters. Ignored if <span class="codeph"> -sharpen </span> is set to 0 or 1; required if <span class="codeph"> -sharpen </span> is set to 2 or 3. <span class="varname"> amount </span> is a real value in the range 0.0...500.0, <span class="varname"> radius </span> is a real value in the range 0.0…10.0, and <span class="varname"> threshold </span> is an integer between 0 and 255. 자세한 내용은 Image Serving Protocol Reference <span class="codeph"> </span> 에서 op_usm= 설명을 참조하십시오. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Validate that the given vignette is a proper production vignette. <span class="varname"> ival </span> represents the minimum file version of the vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>출력 파일의 파일 버전입니다. 지정된 경우 0이거나 유효한 비네팅 파일 버전이어야 합니다(기본 파일 버전보다 크지 않음). 0으로 설정되어 있거나 지정되지 않은 경우 출력 파일은 최신 파일 버전을 사용하여 만들어집니다. - <span class="codeph"> info가 </span> 지정된 경우 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Returns version information for this utility. 파일 이름 및 기타 옵션 없이 지정합니다. </p> </td> 
 </tr> 
</table>

