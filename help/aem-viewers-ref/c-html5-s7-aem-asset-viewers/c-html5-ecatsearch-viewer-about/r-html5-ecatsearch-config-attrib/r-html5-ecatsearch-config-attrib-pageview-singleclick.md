---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: b08b605e-5ffc-42cc-931d-d67750a8dca8
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# PageView.singleclick{#pageview-singleclick}

[!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정  </span> </p> </td> 
   <td colname="col2"> <p> 한 번 클릭/탭으로 확대/축소 동작 매핑을 구성합니다.<span class="codeph"> none </span>으로 설정하면 한 번의 클릭/탭 확대/축소가 비활성화됩니다. <span class="codeph"> 확대/축소 </span>로 설정된 경우 이미지를 클릭하면 한 확대/축소 단계로 확대/축소됩니다.Ctrl 키를 누른 상태에서 클릭하여 한 단계 확대/축소 <span class="codeph"> 재설정 </span>으로 설정하면 이미지를 한 번 클릭하면 확대/축소 레벨이 초기 확대/축소 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 확대/축소 요소가 지정된 제한 범위 내에 있거나 그 범위를 초과하는 경우 재설정이 적용되며, 그렇지 않은 경우 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-edcfcd6c0bd24ac093442c56450b3c97}

선택 사항입니다.

## 기본값 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

[!DNL `zoomReset`] 데스크톱 컴퓨터에; [!DNL `none`] 터치 디바이스에서 사용

## 예 {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]