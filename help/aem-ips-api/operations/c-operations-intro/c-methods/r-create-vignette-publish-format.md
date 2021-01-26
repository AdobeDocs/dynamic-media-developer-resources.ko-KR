---
description: 비네팅에 대한 새 게시 형식을 만듭니다.
seo-description: 비네팅에 대한 새 게시 형식을 만듭니다.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Dynamic Media Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

비네팅에 대한 새 게시 형식을 만듭니다.

비네팅 형식은 IPS에서 이미지 렌더링 서버로 게시되는 기본 비네팅에서 만든 비네팅의 파일 형식 버전과 확대/축소 레벨, 선명하게 하기 매개 변수 및 파일 형식 버전을 지정할 수 있을 뿐만 아니라 게시된 비네팅 및 해당 축소판의 크기를 지정합니다.

최신 이미지 렌더링 서버 버전은 게시에 특정 비네팅 형식 크기를 정의할 필요가 없는 피라미드 비네팅을 지원할 수 있습니다.

## 인증된 사용자 유형 {#section-f5c563e3695c4dba8df41e2a965aace7}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:문자열</span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅이 속한 회사를 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 게시 형식을 식별하는 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> <p>결과 비네팅 보기의 대상 너비를 픽셀 단위로 지정합니다. </p> <p>출력 비네팅의 크기가 기본 비네팅과 같도록 0을 사용합니다. </p> </td> 
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
   <td colname="col4"> 각각의 결과 축소판의 너비를 픽셀 단위로 지정합니다.이 설정은 선택 사항입니다. 축소판 파일이 없으면 0으로 두십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 게시된 비네팅의 파일 형식을 지정합니다. 새 버전의 이미지 작성과 이전 버전의 이미지 렌더링 서버가 있는 경우 ImageRendering 서버가 읽을 수 있는 비네팅 버전을 지정해야 합니다. 더 높은 버전을 지정하면 이미지 렌더링 서버가 게시된 비네팅을 읽을 수 없습니다. 최신 버전에 비네팅을 게시하려면 0으로 설정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 이름과 너비를 나타내는 접미어를 분리하는 문자를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 비네팅 이름과 너비를 나타내는 접미어를 분리하는 문자를 지정합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 선명 효과</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 아니요 </td> 
   <td colname="col4"> 비네팅 크기를 조정할 때 선명도가 기본 보기 이미지에 적용되며 각 푸티지 비네팅 크기에 대해 [선명하게 하기]가 흐림 효과를 보상할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 디지털 언샵 마스크는 특히 스캔한 이미지에서 선명도를 높이는 유연하고 강력한 방법입니다. 이렇게 하면 각 오버샷의 크기를 제어할 수 있습니다(가장자리 테두리의 어둡고 밝기는 얼마나 클지). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 개선할 가장자리 크기나 가장자리 다듬기의 폭에 영향을 주므로 더 작은 라디움에서 세부 묘사를 더 작게 할 수 있습니다. 반경 값이 높으면 가장자리에서 후광이 발생할 수 있습니다. 세부 묘사는 반지보다 작거나 같은 크기의 작은 세부 묘사와 같은 작은 반경이 필요합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 코드 구문  </span> </td> 
   <td colname="col3"> 예 </td> 
   <td colname="col4"> 선명하게 할 최소 명도 변경 사항을 제어하거나 필터가 작동되기 전에 인접한 색조 값이 얼마나 멀리 떨어져야 하는지를 제어합니다. 이 설정을 사용하면 보다 미세한 가장자리는 그대로 유지하면서 더 많은 발음 가장자리를 선명하게 할 수 있습니다. 허용되는 임계값은 0에서 255까지입니다. </td> 
  </tr> 
 </tbody> 
</table>

**출력(createVignettePublishFormatReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 예 | 만든 비네팅 형식의 핸들입니다. |

## 예제 {#section-0564752d439642b9bb8de2903db6de1e}

이 코드는 비네팅 게시 형식을 만듭니다. 생성 요청은 이름, 대상 너비 및 높이, 기타 필수 값을 지정합니다.

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

