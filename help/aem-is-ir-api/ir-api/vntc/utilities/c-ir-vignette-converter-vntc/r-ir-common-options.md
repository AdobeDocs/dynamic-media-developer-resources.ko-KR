---
description: 다음 옵션은 sourceFile의 유형에 관계없이 적용할 수 있습니다.
solution: Experience Manager
title: 일반 옵션
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 일반 옵션{#common-options}

다음 옵션은 sourceFile의 유형에 관계없이 적용할 수 있습니다.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> 문자열 </span> </span> </p> </td> 
  <td class="stentry"> <p>출력 파일을 저장할 폴더(다음과 같은 경우 로그 파일 포함) <span class="codeph"> -log </span> 을(를) 지정했습니다. 절대 경로이거나 현재 작업 디렉토리에 대한 상대 경로일 수 있습니다. 폴더 계층 구조가 없는 경우 생성됩니다. 로 지정된 파일에는 적용되지 않습니다. <span class="codeph"> -log </span>. 지정하지 않으면 출력 파일이 <span class="varname"> sourceFile </span> 이(가) 있습니다. If <span class="varname"> destFile </span> 이(가) 지정되어 있으면 항상 해당 위치에 기록됩니다. <span class="codeph"> -destpath </span> 는 보조 출력 파일에만 적용됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -이미지 </span> </p> </td> 
  <td class="stentry"> <p>지정하면 (첫 번째) 보기 이미지가 비네팅에서 추출되거나, 캐비닛 스타일의 적절한 패널 이미지나 창 덮개 스타일의 첫 번째 조명 이미지에서 추출됩니다. 추출된 이미지는 전체 해상도 TIFF 파일로 저장됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>대상 파일을 생성하지 않습니다. 에서 속성을 빠르게 추출하는 데 유용함 <span class="varname"> sourceFile </span>. 선택적 축소판만( <span class="codeph"> -thumbwidth </span>), 이미지( <span class="codeph"> -image </span>) 및 로그 파일( <span class="codeph"> -log </span>)이 생성됩니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> 이발 </span> </span> </p> </td> 
  <td class="stentry"> <p>손실 없는 PNG 대신 출력 파일에 포함된 RGB 및 회색 음영 이미지 데이터에 대해 손실 JPEG 인코딩을 선택합니다. 알파(RGBA)가 있는 이미지는 항상 PNG 인코딩을 사용하여 저장됩니다. <span class="varname"> 이발 </span> JPEG 품질을 지정합니다(1...100). 85 이상이 권장됩니다. 기본값은 입니다 <span class="codeph"> -jpegquality 0 </span>: PNG 인코딩을 선택합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> 경로 </span> </span> </p> </td> 
  <td class="stentry"> <p>지정된 경로/이름으로 로그 파일 만들기 대상 폴더에 기록된 모든 출력 파일의 전체 경로는 로그 파일에 기록되며, 버전 정보 및 발생한 경고 또는 오류와 같은 몇 가지 추가 설정도 기록됩니다. <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> 출력 </a> 을 참조하십시오. 다음과 같은 경우 로그 파일이 만들어지지 않습니다. <span class="codeph"> -log </span> 이 지정되지 않았습니다. 이 경우 모든 텍스트 출력이 <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> 이발 </span> </span> </p> </td> 
  <td class="stentry"> <p>의 우선 순위를 낮춥니다. <span class="filepath"> vntc </span> 프로세스. 이를 사용하여 다음과 같은 작업을 수행할 수 있습니다 <span class="filepath"> vntc </span> 비네팅을 처리하는 동안 전체 CPU를 인수하지 않습니다. 운영 체제는 다른 중요한 프로세스에 더 많은 시간을 제공할 수 있습니다. <span class="varname"> 이발 </span> 우선 순위가 낮은 비율(0..100)을 지정합니다. 기본값은 입니다 <span class="codeph"> -lowerpriority 0 </span>, 이는 의 우선 순위를 낮추지 않습니다. <span class="filepath"> vntc </span> 프로세스. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> 이발 </span> </span> </p> </td> 
  <td class="stentry"> <p>최대 메모리 크기 지정 <span class="filepath"> vntc </span> 은(는) 바이트 단위로 사용할 수 있습니다. 날짜 <span class="filepath"> vntc </span> 최대 메모리 제한에 도달하면 처리가 중지되고 오류가 발생합니다. <span class="varname"> 이발 </span> 최대 메모리 한도(바이트)를 지정합니다(0.. 3,758,096,384(3.5GB). 날짜 <span class="varname"> 이발 </span> 이(가) 0이면 최대 메모리 제한이 해제됩니다. 기본값은 입니다 <span class="codeph"> -maxmem 3221225472 </span>: 최대 메모리 제한인 3GB를 의미합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> 문자열 </span>" </span> </p> </td> 
  <td class="stentry"> <p>자동 생성된 출력 파일 이름의 파일 이름과 크기/해상도 접미사 사이에 있는 구분 기호를 지정합니다. 지정하지 않은 경우 기본값은 "-"입니다. 다음과 같은 경우 무시됨 <span class="varname"> destFile </span> 또는 <span class="codeph"> -info </span> 이(가) 지정되었습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -선명하게 <span class="varname"> 이발 </span> </span> </p> </td> 
  <td class="stentry"> <p>처리 중에 리샘플링(크기 조정)된 이미지를 선명하게 할 수 있습니다. 캐비닛 스타일 파일의 경우 축소판 선명하게 만들기에만 적용됩니다. </p> <p>선명하게 하기를 비활성화하려면 0을 지정하고(기본값), 보통 선명하게 하기를 활성화하려면 1을 지정하고, 밝기에만 언샵 마스킹을 활성화하려면 2를 지정하고, 각 색상 구성 요소에 대해 언샵 마스킹을 활성화하려면 3을 지정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -트라셀벨 </span> </p> </td> 
  <td class="stentry"> <p>로그 수준을 설정합니다. 기본값은 1이며, 모든 정보, 경고 및 오류 메시지를 출력합니다. 오류 메시지를 제외한 모든 메시지를 비활성화하려면 0으로 설정합니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 금액 </span> <span class="varname"> 반경 </span> <span class="varname"> 임계값 </span> </span> </p> </td> 
  <td class="stentry"> <p>언샵 마스킹 매개 변수를 설정합니다. 다음과 같은 경우 무시됨 <span class="codeph"> -선명하게 </span> 0 또는 1로 설정되어 있는 경우 필요합니다. <span class="codeph"> -선명하게 </span> 는 2 또는 3으로 설정됩니다. <span class="varname"> 금액 </span> 는 0.0...500.0 범위의 실수 값이며, <span class="varname"> 반경 </span> 는 0.0...10.0 범위의 실수 값이며, <span class="varname"> 임계값 </span> 는 0과 255 사이의 정수입니다. 다음에 대한 설명을 참조하십시오. <span class="codeph"> op_usm= </span> 자세한 내용은 이미지 제공 프로토콜 참조 를 참조하십시오. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> 이발 </span> </span> </p> </td> 
  <td class="stentry"> <p>지정된 비네팅이 적절한 프로덕션 비네팅인지 확인합니다. <span class="varname"> 이발 </span> 비네팅의 최소 파일 버전을 나타냅니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> 이발 </span> </span> </p> </td> 
  <td class="stentry"> <p>출력 파일의 파일 버전. 지정하면 0이거나 유효한 비네팅 파일 버전(기본 파일 버전보다 크지 않음)이어야 합니다. 0으로 설정하거나 지정하지 않으면 최신 파일 버전을 사용하여 출력 파일이 만들어집니다. 다음과 같은 경우 무시됨 <span class="codeph"> -info </span> 이(가) 지정되었습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>이 유틸리티의 버전 정보를 반환합니다. 파일 이름 및 기타 옵션 없이 지정합니다. </p> </td> 
 </tr> 
</table>
