---
description: 사용자가 볼 수 있는 내용을 결정하는 사전 설정 보기를 만듭니다. 뷰어는 IPS에서 사용할 수 있는 모든 유형일 수 있습니다. 사전 설정 보기는 자산이 게시될 때 적용됩니다.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

사용자가 볼 수 있는 내용을 결정하는 사전 설정 보기를 만듭니다. 뷰어는 IPS에서 사용할 수 있는 모든 유형일 수 있습니다. 사전 설정 보기는 자산이 게시될 때 적용됩니다.

구문

## 승인된 사용자 유형 {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-aa6dc37e327541ebbfed7685cd8071ff}

**입력(createViewerPresetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 뷰어 사전 설정 및 에셋이 포함된 회사의 핸들입니다. |
| folder핸들 | `xsd:string` | 예 | 에셋이 포함된 폴더의 핸들입니다. |
| name | `xsd:string` | 예 | 뷰어 이름. |
| 유형 | `xsd:string` | 예 | 뷰어 유형. |
| configSettingArray | `types:ConfigSettingArray` | 아니요 | 사전 설정을 적용하는 이미지의 이름, 값 및 핸들을 포함하는 배열입니다. |

**출력(createViewerPresetReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | 예 | 뷰어에 대한 사전 설정 핸들. |

## 예제 {#section-c88ea63536f3461cbe4677ba53f875dd}

이 코드 샘플은 비디오 플레이어 사전 설정을 만듭니다. 응답은 사전 설정에 대한 핸들을 반환합니다.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**응답**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
