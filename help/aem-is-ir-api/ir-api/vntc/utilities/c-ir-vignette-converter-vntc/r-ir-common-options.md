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
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---


# 일반 옵션{#common-options}

sourceFile 유형에 관계없이 다음 옵션을 적용할 수 있습니다.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath  <span class="varname"> 문자열  </span> </span> </p> </td> 
  <td class="stentry"> <p>출력 파일을 가져올 폴더(로그 파일이 지정된 경우 로그 파일 포함) <span class="codeph"></span> 절대 경로이거나 현재 작업 디렉토리를 기준으로 할 수 있습니다. 폴더 계층 구조는 존재하지 않으면 만들어집니다. <span class="codeph"> -log </span>로 지정된 파일에는 적용되지 않습니다. 지정하지 않으면 출력 파일이 <span class="varname"> sourceFile </span>이(가) 있는 폴더에 기록됩니다. <span class="varname"> destFile </span>이 지정되어 있으면 항상 해당 위치에 기록되고 <span class="codeph"> -destpath </span>는 보조 출력 파일에만 적용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -이미지 </span> </p> </td> 
  <td class="stentry"> <p>지정된 경우 (첫 번째) 보기 이미지는 비네팅, 캐비닛 스타일의 적합한 패널 이미지 또는 스타일을 포함하는 윈도우의 첫 번째 조명 이미지에서 추출됩니다. 추출된 이미지는 전체 해상도 TIFF 파일로 저장됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>대상 파일의 생성을 방지합니다. <span class="varname"> sourceFile </span>에서 속성을 빠르게 추출하는 데 유용합니다. 선택 사항 축소판( <span class="codeph"> -thumbwidth </span>), 이미지( <span class="codeph"> -image </span>) 및 로그 파일( <span class="codeph"> -log </span>)만 생성됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>손실 없는 PNG 대신 출력 파일에 포함된 RGB 및 회색 비율 이미지 데이터의 손실 JPEG 인코딩을 선택합니다. 알파(RGBA)가 있는 이미지는 항상 PNG 인코딩을 사용하여 저장됩니다. <span class="varname"> ival </span> 은 JPEG 품질(1...100);85 이상이 권장됩니다. 기본값은 PNG 인코딩을 선택하는 <span class="codeph"> -jpegquality 0 </span>입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -로그  <span class="varname"> 경로  </span> </span> </p> </td> 
  <td class="stentry"> <p>지정된 경로/이름으로 로그 파일 만들기 대상 폴더에 기록된 모든 출력 파일의 전체 경로는 로그 파일에 기록되고 버전 정보 및 발생한 경고나 오류 등 일부 추가 설정도 기록합니다(자세한 내용은 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> 출력 </a> 참조). <span class="codeph"> -log </span>이(가) 지정되지 않은 경우 로그 파일이 생성되지 않습니다.이 경우 모든 텍스트 출력이 <span class="codeph"> stdout </span>에 기록됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -낮은 우선 순위  <span class="varname"> 값  </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span> 프로세스의 우선 순위를 낮춥니다. 비네팅을 처리하는 동안 <span class="filepath"> vntc </span>이(가) 전체 CPU를 차지하지 않도록 이 옵션을 사용할 수 있습니다. 운영 체제가 더 많은 시간을 다른 중요한 프로세스에 할애할 수 있도록 해줍니다. <span class="varname"> ival </span> 은 낮은 우선 순위 비율(0..100)을 지정합니다. 기본값은 <span class="codeph"> -lower priority 0 </span>입니다. 이 값은 <span class="filepath"> vntc </span> 프로세스의 우선 순위를 낮추지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span>이(가) 바이트 단위로 사용할 수 있는 최대 메모리 양을 지정합니다. <span class="filepath"> vntc </span>이(가) 최대 메모리 제한에 도달하면 처리가 중지되고 오류가 발생합니다. <span class="varname"> ival </span> 은 최대 메모리 제한(바이트 수)을 지정합니다. 3,758,096,384(3.5GB)). <span class="varname"> 변수 </span>이 0이면 최대 메모리 제한이 해제됩니다. 기본값은 <span class="codeph"> -maxmem 3221225472 </span>입니다. 이는 최대 메모리 제한은 3GB입니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "  <span class="varname"> string  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>자동으로 생성된 출력 파일 이름에 대한 파일 이름과 크기/해상도 접미어 사이에 있는 구분 기호를 지정합니다. 지정하지 않을 경우 기본값은 "-"입니다. <span class="varname"> destFile </span> 또는 <span class="codeph"> -info </span>이(가) 지정된 경우 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -선명  <span class="varname"> 효과  </span> </span> </p> </td> 
  <td class="stentry"> <p>처리하는 동안 이미지를 선명하게 할 수 있습니다(크기 조절). 캐비닛 스타일 파일의 경우 축소판 선명도 적용에만 적용됩니다. </p> <p>선명 효과를 비활성화하려면 0(기본값), 표준 선명 효과를 활성화하려면 1, 밝기에만 언샵 마스킹을 활성화하려면 2, 각 색상 구성 요소에 대해 언샵 마스킹을 활성화하려면 3)을 지정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>로그 수준을 설정합니다. 기본값은 1이며, 모든 정보, 경고 및 오류 메시지를 출력합니다. 오류 메시지를 제외한 모든 메시지를 비활성화하려면 0으로 설정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm  <span class="varname"> 양  </span> <span class="varname"> 반경  </span> <span class="varname"> 임계값  </span> </span> </p> </td> 
  <td class="stentry"> <p>언샵 마스킹 매개 변수를 설정합니다. <span class="codeph"> -sharpen </span>이 0 또는 1로 설정된 경우 무시됩니다.<span class="codeph"> -sharpen </span>이(가) 2 또는 3으로 설정된 경우 필요합니다. <span class="varname"> amount </span> 는 0.0...500.0 범위의 실제 값입니다. radius <span class="varname"> 는 0.0...10.0 범위의 실제 값이며  </span> 임계값은 0에서 255 사이의 정수 <span class="varname">   </span> 입니다. 자세한 내용은 이미지 제공 프로토콜 참조 설명서의 <span class="codeph"> op_usm= </span>에 대한 설명을 참조하십시오. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validate production  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>주어진 비네팅이 올바른 프로덕션 비네팅인지 확인합니다. <span class="varname"> ival </span> 은 비네팅의 최소 파일 버전을 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>출력 파일의 파일 버전입니다. 지정된 경우 0이거나 유효한 비네팅 파일 버전이어야 합니다(기본 파일 버전보다 크지 않음). 0으로 설정되어 있거나 지정되지 않은 경우 출력 파일은 최신 파일 버전을 사용하여 만들어집니다. <span class="codeph"> -info </span>가 지정된 경우 무시됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>이 유틸리티에 대한 버전 정보를 반환합니다. 파일 이름 및 기타 옵션 없이 지정합니다. </p> </td> 
 </tr> 
</table>

