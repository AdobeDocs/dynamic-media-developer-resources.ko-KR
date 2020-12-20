---
description: 모니터링/경고 시스템에 대한 설정을 포함합니다.
seo-description: 모니터링/경고 시스템에 대한 설정을 포함합니다.
seo-title: monitor.conf
solution: Experience Manager
title: monitor.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 31949797-df2c-4b7c-841b-4c623299a228
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# monitor.conf{#monitor-conf}

모니터링/경고 시스템에 대한 설정을 포함합니다.

이 파일은 JAVA 속성 파일입니다. 적절한 규약을 준수하기 위해서는 세심한 주의를 기울여야 한다.그렇지 않으면 플랫폼 서버를 시작하지 못할 수 있습니다. 특히 Windows 파일 경로에서 백슬래시 &#39;\&#39; 대신 이중 백슬래시 &#39;/&#39; 또는 단일 슬래시(&#39;/&#39;)를 사용해야 합니다. 백슬래시는 이 유형의 파일에서 이스케이프 문자로 사용됩니다.

이 파일에 대한 변경 사항은 파일을 저장한 후 바로 적용됩니다.

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>일반 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false  </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1  </span> </p> <p> <span class="codeph"> mailSender.port=25  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=60000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=60000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>경고 임계값 </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>

