---
description: PDF 작업 옵션 적용 작업 옵션 파일 또는 PDF 사전 설정은 InDesign의 [PDF 옵션] 대화 상자 또는 PDF 사전 설정에서 Illustrator에서 생성된 파일입니다.
seo-description: PDF 작업 옵션 적용 작업 옵션 파일 또는 PDF 사전 설정은 InDesign의 [PDF 옵션] 대화 상자 또는 PDF 사전 설정에서 Illustrator에서 생성된 파일입니다.
seo-title: 작업 옵션
solution: Experience Manager
title: 작업 옵션
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7288cf29-850f-4121-8425-5f995daac22d
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 42%

---


# 작업 옵션{#joboption}

PDF 작업 옵션 적용 작업 옵션 파일 또는 PDF 사전 설정은 InDesign의 [PDF 옵션] 대화 상자 또는 PDF 사전 설정에서 Illustrator에서 생성된 파일입니다.

` joboption= *`value`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span></span> </p> </td> 
  <td class="stentry"> <p>작업 옵션 파일의 IPSID입니다. </p></td> 
 </tr> 
</table>

작업 옵션 파일은 IPS/Dynamic Media Classic에서 업로드하고 게시할 수 있습니다. 작업 옵션 파일에 포함된 PDF 옵션은 PDF가 생성될 때 사용됩니다.

현재 지원되는 옵션은 다음과 같습니다.

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>일반 </p></td> 
  <td class="stentry"> <p> 호환성 </p> <p> 개체 수준 압축 </p> <p> 썸네일 포함 </p> <p> 빠른 웹 보기를 위해 최적화 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>이미지 </p></td> 
  <td class="stentry"> <p> 다운샘플링색상, 회색 및 모노를 위한 , 해상도, 임계값 및 압축 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>글꼴 </p></td> 
  <td class="stentry"> <p> 모든 글꼴 포함 </p> <p> OpenType 글꼴 포함 </p> <p> 사용된 문자의 비율이 다음보다 적을 때 서브세트 글꼴 포함 </p> <p> 항상 포함 목록 </p> <p> 포함 안 함 목록 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>색상 </p></td> 
  <td class="stentry"> <p> 색상 전략(이미지에만 태그 지정은 모든 항목에 태그 지정으로 처리됨) </p> <p> 문서 렌더링 의도 </p> <p> 4.2.5에서는 다음 작업 공간만 지원됩니다. </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> 인코딩 범위가 [-4.0, 4.0]인 scRGB </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> 평면 XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">선형 ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8비트 </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC 8비트 </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">회색 <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">회색 감마 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">회색 감마 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">점 게인 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">점 게인 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">점 게인 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> 점 게인 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">점 게인 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> 보정된 CMYK 색상 공간의 CMYK 값 유지 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>고급 </p></td> 
  <td class="stentry"> <p>[OPI 설명 유지]가 항상 켜져 있음. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>표준 </p></td> 
  <td class="stentry"> <p>규정 준수 표준. </p></td> 
 </tr> 
</table>

