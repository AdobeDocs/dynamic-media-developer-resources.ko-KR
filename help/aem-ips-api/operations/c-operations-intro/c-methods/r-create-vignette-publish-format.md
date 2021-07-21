---
description: 비네트에 대한 새 게시 형식을 만듭니다.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 14%

---

# createVignettePublishFormat{#createvignettepublishformat}

비네트에 대한 새 게시 형식을 만듭니다.

비네팅 형식은 IPS에서 이미지 렌더링 서버에 게시된 기본 비네팅에서 생성된 비네팅의 파일 형식 버전과 확대/축소 수준, 선명하게 하기 매개 변수 및 파일 형식 버전을 비롯하여 게시된 비네팅 및 해당 축소판의 크기를 지정합니다.

최신 이미지 렌더링 서버 버전은 피라미드 비네팅을 지원할 수 있으므로 게시할 특정 비네팅 형식 크기를 정의할 필요가 없습니다.

## 인증된 사용자 유형 {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-3a368186ec1d4005bca056fc9d9bacc7}

**입력(createVignetPublishFormatParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네트가 속한 회사를 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 이름</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 게시 형식을 식별하는 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p>결과 비네팅 보기의 대상 너비를 픽셀 단위로 지정합니다. </p> <p>출력 비네트의 크기가 기본 비네트와 동일하도록 0을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 이미지 렌더링 서버에서의 확대/축소에 대해 최적화된 피라미드형 비네팅을 만듭니다. 대상 비네팅 크기 필드에서 설정된 최대 크기에서 시작되며, 단일 비네팅 출력 파일에 여러 크기의 보기가 만들어집니다. 각 후속 보기 크기는 너비 및 높이가 128x128픽셀 이내가 될 때까지 반으로 줄어듭니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 각 결과 축소판의 너비를 픽셀 단위로 지정합니다. 이 설정은 선택 사항입니다. 축소판 파일이 없으면 0으로 둡니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 게시된 비네트의 파일 형식을 지정합니다. 새 버전의 이미지 작성과 이전 버전의 이미지 렌더링 서버가 있는 경우 ImageRendering 서버가 읽을 수 있는 비네팅 버전을 지정해야 합니다. 더 높은 버전을 지정하면 이미지 렌더링 서버에서 게시된 비네팅을 읽을 수 없습니다. 최신 버전에서 비네팅을 게시하려면 0으로 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 이름과 너비를 나타내는 접미사를 구분하는 문자를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 이름과 너비를 나타내는 접미사를 구분하는 문자를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 선명</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 번영(Sharpening)은 비네팅 크기를 조정할 때 흐림 현상을 보완할 수 있는 각 번영 크기 각각에 대한 기본 보기 이미지에 선명도 적용됩니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 디지털 언샵 마스킹은 특히 스캔한 이미지에서 선명도를 높이는 유연하고 강력한 방법입니다. 이 옵션은 각 오버슈트의 크기를 제어합니다(가장자리 테두리가 얼마나 어두워지고 빛이 되는지). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 강조할 가장자리의 크기 또는 가장자리의 크기가 작아지는 정도에 영향을 주므로 더 작은 라디움은 더 작은 스케일 세부 정보를 향상시킵니다. 반경 값이 높을수록 가장자리에서 할로스가 발생할 수 있습니다. 미세 세부 사항에는 동일한 크기의 작은 세부 정보나 반지름보다 작은 반경이 필요합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 필터가 작동하기 전에 인접한 색조 값이 얼마나 멀리 떨어져 있어야 하는지를 조정하거나, 최소 밝기 변경 사항을 조정할 수 있습니다. 이 설정은 더 미세한 가장자리를 그대로 유지하면서 더 많이 발음 모서리를 선명하게 할 수 있습니다. 0에서 255까지의 임계값 허용 범위입니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(createVignettePublishFormatReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 예 | 생성된 비네팅 형식에 대한 핸들입니다. |

## 예제 {#section-0564752d439642b9bb8de2903db6de1e}

이 코드는 비네팅 게시 형식을 만듭니다. 만들기 요청에서는 이름, 대상 너비 및 높이, 기타 필수 값을 지정합니다.

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
