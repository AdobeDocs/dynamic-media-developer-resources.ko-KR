---
description: 사용자가 볼 수 있는 내용을 결정하는 사전 설정 보기를 만듭니다. 뷰어는 IPS에서 사용할 수 있는 모든 유형이 될 수 있습니다. 사전 설정 보기는 자산이 게시될 때 적용됩니다.
seo-description: 사용자가 볼 수 있는 내용을 결정하는 사전 설정 보기를 만듭니다. 뷰어는 IPS에서 사용할 수 있는 모든 유형이 될 수 있습니다. 사전 설정 보기는 자산이 게시될 때 적용됩니다.
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
topic: Scene7 Image Production System API
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createViewerPreset{#createviewerpreset}

사용자가 볼 수 있는 내용을 결정하는 사전 설정 보기를 만듭니다. 뷰어는 IPS에서 사용할 수 있는 모든 유형이 될 수 있습니다. 사전 설정 보기는 자산이 게시될 때 적용됩니다.

구문

## 인증된 사용자 유형 {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-aa6dc37e327541ebbfed7685cd8071ff}

**입력(createViewerPresetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 예 | 뷰어 사전 설정과 에셋이 포함된 회사의 핸들 |
| ` *`folderHandle`*` | `xsd:string` | 예 | 에셋이 포함된 폴더의 핸들 |
| ` *`name`*` | `xsd:string` | 예 | 뷰어 이름입니다. |
| ` *`type`*` | `xsd:string` | 예 | 뷰어 유형. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | 아니요 | 사전 설정을 적용할 이미지의 이름, 값 및 핸들이 들어 있는 배열입니다. |

**출력(createViewerPresetReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| ` *`viewerPresetHandle`*` | `xsd:string` | 예 | 뷰어에 대한 사전 설정 핸들 |

## 예제 {#section-c88ea63536f3461cbe4677ba53f875dd}

이 코드 샘플에서는 비디오 플레이어 사전 설정을 만듭니다. 이 응답은 사전 설정에 대한 핸들을 반환합니다.

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

