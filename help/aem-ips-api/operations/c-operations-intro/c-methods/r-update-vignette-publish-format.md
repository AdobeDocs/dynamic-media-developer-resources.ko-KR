---
description: 비네팅 게시 형식 설정을 업데이트합니다.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 20%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

비네팅 게시 형식 설정을 업데이트합니다.

## 인증된 사용자 유형 {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**입력(updateVignettePublishFormatParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| `*`vignetteFormatHandle`*` | `xsd:string` | 예 | 게시 형식 핸들입니다. |
| `*`name`*` | `xsd:string` | 아니요 | 게시 형식 이름입니다. |
| `*`targetWidth`*` | `xsd:int` | 예 | 결과 비네팅 보기의 대상 너비를 픽셀 단위로 지정합니다. 출력 비네트의 크기가 기본 비네트와 동일하도록 0을 사용합니다. |
| `*`targetHeight`*` | `xsd:int` | 예 | 결과 비네팅 보기의 대상 높이를 픽셀 단위로 지정합니다. 출력 비네트의 크기가 기본 비네트와 동일하도록 0을 사용합니다. |
| `*`createPyramid`*` | `xsd:boolean` | 예 | 이미지 렌더링 서버에서의 확대/축소에 대해 최적화된 피라미드형 비네팅을 만듭니다. 대상 비네팅 크기 필드에서 설정된 최대 크기에서 시작되며, 단일 비네팅 출력 파일에 여러 크기의 보기가 만들어집니다. 각 후속 보기 크기는 너비 및 높이가 128x128픽셀 이내가 될 때까지 반으로 줄어듭니다. |
| `*`thumbWidth`*` | `xsd:int` | 예 | 각 결과 축소판의 너비를 픽셀 단위로 지정합니다. 이 설정은 선택 사항입니다. 축소판 파일이 없으면 0으로 둡니다. |
| `*`saveAsVersion`*` | `xsd:int` | 예 | 게시된 비네트의 파일 형식을 지정합니다. 새 버전의 이미지 작성과 이전 버전의 이미지 렌더링 서버가 있는 경우 ImageRendering 서버가 읽을 수 있는 비네팅 버전을 지정해야 합니다. 더 높은 버전을 지정하면 이미지 렌더링 서버에서 게시된 비네팅을 읽을 수 없습니다. 최신 버전에서 비네팅을 게시하려면 0으로 설정합니다. |
| `*`sizeSuffixSeparator`*` | `xsd:string` | 예 | 비네팅 이름 및 너비를 나타내는 접미어를 구분하는 문자를 지정합니다. |
| `*`선명`*` | `xsd:int` | 아니요 | 각 게시 비네팅 크기에 대한 기본 보기 이미지에 선명도 적용됩니다. 선명하게 하면 비네트의 크기가 조정될 때 흐림 효과를 보상할 수 있습니다. |
| `*`usmAmount`*` | `xsd:double` | 예 | 디지털 언샵 마스킹은 특히 스캔한 이미지에서 선명도를 높이는 유연하고 강력한 방법입니다. 이 옵션은 각 오버슈트의 크기를 제어합니다(가장자리 테두리가 얼마나 어두워지고 밝아지는지). |
| `*`usmRadius`*` | `xsd:double` | 예 | 향상 대상 가장자리 크기 또는 가장자리 영역의 넓이에 영향을 주므로 작은 반경이 작은 배율 세부 정보를 개선합니다. 반경 값이 높을수록 가장자리에서 할로스가 발생할 수 있습니다. 미세 세부 사항에는 동일한 크기의 작은 세부 정보나 반지름보다 작은 반경이 필요합니다. |
| `*`usmThreshold`*` | `xsd:int` | 예 | 필터가 작동하기 전에 인접한 색조 값이 얼마나 멀리 떨어져 있어야 하는지를 조정하거나, 최소 밝기 변경 사항을 조정할 수 있습니다. 이 설정은 더 미세한 가장자리를 그대로 유지하면서 더 많이 발음 모서리를 선명하게 할 수 있습니다. 허용 가능한 임계값 범위는 0~255입니다. |

**출력(updateVignettePublishFormatReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 예 | 업데이트된 비네팅 게시 형식을 처리합니다. |

## 예 {#section-fcba4bf2b7264786a676e315a35dbe43}

이 코드 샘플은 비네팅 게시 형식을 업데이트하고 핸들을 업데이트된 형식으로 반환합니다.

**요청**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**응답**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
