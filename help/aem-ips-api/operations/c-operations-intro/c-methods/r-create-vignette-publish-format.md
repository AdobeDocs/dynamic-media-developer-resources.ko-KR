---
description: 비네팅에 대한 새 게시 형식을 만듭니다.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---

# createVignettePublishFormat{#createvignettepublishformat}

비네팅에 대한 새 게시 형식을 만듭니다.

비네팅 형식은 게시된 비네팅 및 그 축소판뿐만 아니라 확대/축소 수준, 선명 매개 변수 및 IPS의 이미지 렌더링 서버에 게시된 기본 비네팅에서 생성된 비네팅의 파일 형식 버전을 지정합니다.

최신 이미지 렌더링 서버 버전은 피라미드 비네팅을 지원할 수 있으므로 게시할 특정 비네팅 형식 크기를 정의할 필요가 없습니다.

## 승인된 사용자 유형 {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-3a368186ec1d4005bca056fc9d9bacc7}

**입력(createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 필수 </th> 
   <th colname="col4" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> company핸들</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅이 속한 회사를 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 게시 형식을 식별하는 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p>결과 비네팅 보기의 대상 너비를 픽셀 단위로 지정합니다. </p> <p>출력 비네팅이 기본 비네팅과 크기가 동일하도록 0을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 대상 높이</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 렌더링 서버에서의 확대/축소에 최적화된 피라미드형 비네팅을 만듭니다. Target 비네팅 크기 필드에서 설정한 최대 크기부터 시작하여 단일 비네팅 출력 파일에 여러 크기의 보기가 만들어집니다. 각 후속 보기 크기는 너비 및 높이가 128x128 픽셀 이내가 될 때까지 반으로 줄어듭니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 각 결과 썸네일의 너비를 픽셀 단위로 지정합니다. 이 설정은 선택 사항입니다. 썸네일 파일이 없으면 0으로 둡니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 게시된 비네팅의 파일 형식을 지정합니다. 이미지 작성의 새 버전과 이미지 렌더링 서버의 이전 버전이 주어지면 이미지 렌더링 서버에서 읽을 수 있는 비네팅 버전을 지정해야 합니다. 상위 버전을 지정하면 이미지 렌더링 서버에서 게시된 비네팅을 읽을 수 없습니다. 최신 버전에서 비네팅을 게시하려면 0으로 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 다른 이름으로 저장</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 이름과 너비를 나타내는 접미사를 구분하는 문자를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 이름과 너비를 나타내는 접미사를 구분하는 문자를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 선명하게</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 비네팅 크기 크기를 조정할 때 선명하게 하기가 흐려지는 것을 보상할 수 있도록 각 퍼블리싱 비네팅 크기에 대한 기본 보기 이미지에 선명하게 하기를 적용합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 디지털 언샵 마스킹은 특히 스캔한 이미지에서 선명도를 높일 수 있는 유연하고 강력한 방법입니다. 각 오버슛의 크기(가장자리 테두리가 얼마나 어둡고 밝아지는지)를 제어합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 향상할 가장자리 크기 또는 가장자리 테두리의 너비에 영향을 주므로 라듐이 작을수록 작은 크기의 세부 묘사가 향상됩니다. 반지름 값이 높을수록 가장자리에서 반동이 발생할 수 있습니다. 미세 세부 영역은 동일한 크기의 작은 세부 영역이나 반지름보다 작은 세부 영역이 손실되므로 더 작은 반지름이 필요합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구 </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 최소 밝기 변경을 선명하게 하거나 필터가 작동하기 전에 인접한 색조 값이 얼마나 멀리 떨어져 있어야 하는지 제어합니다. 이 설정을 사용하면 보다 미세한 가장자리를 그대로 유지하면서 보다 선명한 가장자리를 선명하게 할 수 있습니다. 허용 가능한 임계값 범위: 0~255. </td> 
  </tr> 
 </tbody> 
</table>

**출력(createVignettePublishFormatReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 비네팅 형식 핸들 | `xsd:string` | 예 | 생성된 비네팅 형식에 대한 핸들입니다. |

## 예제 {#section-0564752d439642b9bb8de2903db6de1e}

이 코드는 비네팅 게시 형식을 만듭니다. 만들기 요청은 이름, 대상 너비 및 높이, 기타 필수 값을 지정합니다.

**요청**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**응답**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```
