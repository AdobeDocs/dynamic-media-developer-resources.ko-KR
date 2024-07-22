---
description: 비네팅 게시 형식 설정을 업데이트합니다.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 5%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

비네팅 게시 형식 설정을 업데이트합니다.

## 승인된 사용자 유형 {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**입력(updateVignettePublishFormatParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 회사 핸들. |
| 비네팅 형식 핸들 | `xsd:string` | 예 | Publish 형식 핸들. |
| name | `xsd:string` | 아니요 | Publish 형식 이름입니다. |
| targetWidth | `xsd:int` | 예 | 결과 비네팅 보기의 대상 너비를 픽셀 단위로 지정합니다. 출력 비네팅이 기본 비네팅과 크기가 동일하도록 0을 사용합니다. |
| 대상 높이 | `xsd:int` | 예 | 결과 비네팅 보기의 대상 높이를 픽셀 단위로 지정합니다. 출력 비네팅이 기본 비네팅과 크기가 동일하도록 0을 사용합니다. |
| createPyramid | `xsd:boolean` | 예 | 이미지 렌더링 서버에서의 확대/축소에 최적화된 피라미드형 비네팅을 만듭니다. 대상 비네팅 크기 필드에서 설정한 최대 크기부터 단일 비네팅 출력 파일에 여러 크기의 보기가 만들어집니다. 각 후속 보기 크기는 너비 및 높이가 128x128 픽셀 이내가 될 때까지 반으로 줄어듭니다. |
| thumbWidth | `xsd:int` | 예 | 각 결과 썸네일의 너비를 픽셀 단위로 지정합니다. 이 설정은 선택 사항입니다. 썸네일 파일이 없으면 0으로 둡니다. |
| 다른 이름으로 저장 | `xsd:int` | 예 | 게시된 비네팅의 파일 형식을 지정합니다. 이미지 작성의 새 버전과 이미지 렌더링 서버의 이전 버전이 주어지면 이미지 렌더링 서버에서 읽을 수 있는 비네팅 버전을 지정해야 합니다. 상위 버전을 지정하면 이미지 렌더링 서버에서 게시된 비네팅을 읽을 수 없습니다. 최신 버전에서 비네팅을 게시하려면 0으로 설정합니다. |
| sizeSuffixSeparator | `xsd:string` | 예 | 비네팅 이름과 너비를 나타내는 접미사를 구분하는 문자를 지정합니다. |
| 선명하게 | `xsd:int` | 아니요 | 각 게시 비네팅 크기에 대한 기본 보기 이미지에 선명하게 하기를 적용합니다. 비네팅 크기 조정 시 선명하게 하기를 통해 흐림 효과를 보상할 수 있습니다. |
| usmAmount | `xsd:double` | 예 | 디지털 언샵 마스킹은 특히 스캔한 이미지에서 선명도를 높일 수 있는 유연하고 강력한 방법입니다. 각 오버슛의 크기(가장자리 테두리가 얼마나 어둡고 밝아지는지)를 제어합니다. |
| usmRadius | `xsd:double` | 예 | 향상할 가장자리 크기 또는 가장자리 테두리의 너비에 영향을 주므로 반지름이 작을수록 더 작은 크기의 세부 묘사가 향상됩니다. 반지름 값이 높을수록 가장자리에서 반동이 발생할 수 있습니다. 미세 세부 영역은 동일한 크기의 작은 세부 영역이나 반지름보다 작은 세부 영역이 손실되므로 더 작은 반지름이 필요합니다. |
| usmThreshold | `xsd:int` | 예 | 최소 밝기 변경을 선명하게 하거나 필터가 작동하기 전에 인접한 색조 값이 얼마나 멀리 떨어져 있어야 하는지 제어합니다. 이 설정을 사용하면 보다 미세한 가장자리를 그대로 유지하면서 보다 선명한 가장자리를 선명하게 할 수 있습니다. 허용 가능한 임계값 범위는 0~255입니다. |

**출력(updateVignettePublishFormatReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 비네팅 형식 핸들 | `xsd:string` | 예 | 업데이트된 비네팅 게시 형식에 대해 처리합니다. |

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
