---
description: 비네팅 제작 형식 설정을 업데이트합니다.
seo-description: 비네팅 제작 형식 설정을 업데이트합니다.
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---


# updateVignettePublishFormat{#updatevignettepublishformat}

비네팅 제작 형식 설정을 업데이트합니다.

## 인증된 사용자 유형 {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**입력(updateVignettePublishFormatParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 회사 핸들. |
| ` *`vignetteFormatHandle`*` | `xsd:string` | 예 | 게시 형식 핸들. |
| ` *`name`*` | `xsd:string` | 아니요 | 게시 형식 이름입니다. |
| ` *`targetWidth`*` | `xsd:int` | 예 | 결과 비네팅 보기의 대상 너비를 픽셀 단위로 지정합니다. 출력 비네팅의 크기가 기본 비네팅과 같도록 0을 사용합니다. |
| ` *`targetHeight`*` | `xsd:int` | 예 | 결과 비네팅 보기의 대상 높이를 픽셀 단위로 지정합니다. 출력 비네팅의 크기가 기본 비네팅과 같도록 0을 사용합니다. |
| ` *`createPyramid`*` | `xsd:boolean` | 예 | 이미지 렌더링 서버에서의 확대/축소에 대해 최적화된 피라미드형 비네팅을 만듭니다. 대상 비네팅 크기 필드에서 설정된 최대 크기에서 시작되며, 단일 비네팅 출력 파일에 여러 크기의 보기가 만들어집니다. 각 후속 보기 크기는 너비 및 높이가 128x128픽셀 이내가 될 때까지 반으로 줄어듭니다. |
| ` *`thumbWidth`*` | `xsd:int` | 예 | 각각의 결과 축소판의 너비를 픽셀 단위로 지정합니다.이 설정은 선택 사항입니다. 축소판 파일이 없으면 0으로 두십시오. |
| ` *`saveAsVersion`*` | `xsd:int` | 예 | 게시된 비네팅의 파일 형식을 지정합니다. 새 버전의 이미지 작성과 이전 버전의 이미지 렌더링 서버가 있는 경우 ImageRendering 서버가 읽을 수 있는 비네팅 버전을 지정해야 합니다. 더 높은 버전을 지정하면 이미지 렌더링 서버가 게시된 비네팅을 읽을 수 없습니다. 최신 버전에 비네팅을 게시하려면 0으로 설정합니다. |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | 예 | 비네팅 이름 및 너비를 나타내는 접미어를 구분하는 문자를 지정합니다. |
| ` *`선명 효과`*` | `xsd:int` | 아니요 | 각 게시 비네팅 크기에 대한 기본 보기 이미지에 선명 효과를 적용합니다.비네팅 크기를 조정할 때 선명하게 하기를 통해 흐림 효과를 보상할 수 있습니다. |
| ` *`usmAmount`*` | `xsd:double` | 예 | 디지털 언샵 마스크는 특히 스캔한 이미지에서 선명도를 높이는 유연하고 강력한 방법입니다. 이렇게 하면 각 오버샷의 크기를 제어할 수 있습니다(가장자리 테두리가 어두워지고 밝게 되는 정도). |
| ` *`usmRadius`*` | `xsd:double` | 예 | 향상된 가장자리 크기 또는 가장자리 다듬기의 폭에 영향을 주므로 작은 반경이 작은 비율 세부 묘사를 향상합니다. 반경 값이 높으면 가장자리에서 후광이 발생할 수 있습니다. 세부 묘사는 반지보다 작거나 같은 크기의 작은 세부 묘사와 같은 작은 반경이 필요합니다. |
| ` *`usmThreshold`*` | `xsd:int` | 예 | 선명하게 할 최소 명도 변경 사항을 제어하거나 필터가 작동되기 전에 인접한 색조 값이 얼마나 멀리 떨어져야 하는지를 제어합니다. 이 설정을 사용하면 보다 미세한 가장자리는 그대로 유지하면서 더 많은 발음 가장자리를 선명하게 할 수 있습니다. 허용되는 임계값 범위는 0에서 255까지입니다. |

**출력(updateVignettePublishFormatReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | 예 | 업데이트된 비네팅 제작 형식을 처리합니다. |

## 예 {#section-fcba4bf2b7264786a676e315a35dbe43}

이 코드 샘플은 비네팅 제작 형식을 업데이트하고 핸들을 업데이트된 형식으로 반환합니다.

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

