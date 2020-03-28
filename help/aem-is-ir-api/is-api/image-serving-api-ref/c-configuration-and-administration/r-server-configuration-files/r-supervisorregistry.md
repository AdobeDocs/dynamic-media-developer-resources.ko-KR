---
description: 서버 수퍼바이저 구성 설정을 포함합니다.
seo-description: 서버 수퍼바이저 구성 설정을 포함합니다.
seo-title: SupervisorRegistry.xml
solution: Experience Manager
title: SupervisorRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 8442a3d6-5f45-48d1-8e6e-71f0ed384227
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SupervisorRegistry.xml{#supervisorregistry-xml}

서버 수퍼바이저 구성 설정을 포함합니다.

이 XML 파일을 편집할 때는 유효한 XML 구문을 유지해야 합니다. 그렇지 않으면 이미지 서버를 시작하지 못할 수 있습니다.

이 파일을 편집한 후 이미지 제공을 다시 시작하여 변경 사항을 적용합니다. 아래 강조 표시된 요소/속성 값만 수정할 수 있습니다. Scene7 기술 지원에서 권장하는 경우에만 이 파일의 다른 모든 컨텐츠를 편집합니다.

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Scene7 Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Scene7 SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Scene7 Platform Server</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```

