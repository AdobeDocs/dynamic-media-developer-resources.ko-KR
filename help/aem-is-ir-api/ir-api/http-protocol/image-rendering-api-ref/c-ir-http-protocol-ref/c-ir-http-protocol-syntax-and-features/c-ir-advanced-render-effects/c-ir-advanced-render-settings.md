---
title: 고급 렌더링 설정
description: Dynamic Media 이미지 작성 패키지의 일부인 비네팅 작성 도구는 비네팅 렌더링 엔진의 낮은 수준 측면을 제어하는 메커니즘을 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ad8f4b4-dd9c-43f5-aacc-67a564e34d92
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 25%

---

# 고급 렌더링 설정{#advanced-render-settings}

Dynamic Media 이미지 작성 패키지의 일부인 비네팅 작성 도구는 비네팅 렌더링 엔진의 낮은 수준 측면을 제어하는 메커니즘을 제공합니다.

>[!NOTE]
>
>렌더링 설정은 이미지 렌더링 및 이미지 작성의 고급 기능입니다. 렌더링 설정 사용에 대한 교육, 자문 또는 둘 다에 대해서는 Adobe 기술 지원 센터 또는 Adobe 컨설팅 담당자에게 문의하십시오.

이러한 설정은 이미지 작성에서 대화식으로 제어됩니다. 를 사용하여 이미지 렌더링에서 동일한 설정을 적용할 수 있습니다. `rs=` 명령(또는 `catalog::RenderSettings` value). 이 메커니즘은 각 재료에 대해 서로 다른 선명하게 하기 옵션을 선택하고 밝은 영역의 채도나 어두운 영역의 대비를 변경하는 등 조명 렌더링 알고리즘의 동작을 수정하는 데 사용됩니다.

## 고급 렌더링 설정(rs=) 값 {#section-d9e7f341ebd44f07a4e90f1f5910726b}

<table id="table_1517FC39C7344EBB9F17BE20415DB057"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Code </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
   <th colname="col3" class="entry"> <p>최소값 </p> </th> 
   <th colname="col4" class="entry"> <p>최대값 </p> </th> 
   <th colname="col5" class="entry"> <p>주의 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col2"> <p>Render Effects/Alternate Shader는 비네팅의 설정을 재정의합니다. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>A0=렌더링 효과 </p> <p>A1=대체 셰이더 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>U </p> </td> 
   <td colname="col2"> <p>USM(언샵 마스크). </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>2 </p> </td> 
   <td colname="col5"> <p>USM을 사용하려면 U가 0보다 커야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>수 </p> </td> 
   <td colname="col2"> <p>USM 금액(%). </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>500 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V </p> </td> 
   <td colname="col2"> <p>USM 반경(픽셀). </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>X </p> </td> 
   <td colname="col2"> <p>USM 임계값(레벨). </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q </p> </td> 
   <td colname="col2"> <p>크기 조정 모드. </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_87184BB93E7F46D59BA1AAAFA8455512"> 
      <li id="li_E7711C3678ED4DE09E710F7C430CEF42">가장 가까운 이웃 </li> 
      <li id="li_CAE975B91C604DA0AA493F700AEBE199">쌍1차 </li> 
      <li id="li_24E5A40B8A3F4C808A68686C27647CD5">쌍3차 </li> 
      <li id="li_42ACFCE65B4843ACAFA6A52255364642">슈퍼샘플링(기본값) </li> 
      <li id="li_34EC85C4D15145DF80F7D3DB7B6244D3">Lanczos 창 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>R </p> </td> 
   <td colname="col2"> <p>재샘플링 모드. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_FD4A9D73C32F47C3BF13776BB4D2818D"> 
      <li id="li_F08AD1D093D74059B60302374B472B52">기본값 </li> 
      <li id="li_FD4C859D975B44399475D4D93D6B05AB">가장 가까운 이웃 </li> 
      <li id="li_CA93566F5D4F4D3CAA1D0816562A3851">쌍1차 </li> 
      <li id="li_D334ACF969E749A89A464B21C96CE8A6">슈퍼샘플링 </li> 
      <li id="li_FAC72C36FF4A418F8A5B05F3B4E7C5D8">자동 선택 </li> 
      <li id="li_6E9D81045A0C4804A4D35D9B239F6486">푸아송 샘플러 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>슈퍼샘플링: 무작위 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>200 </p> </td> 
   <td colname="col5"> <p>기본값은 0입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>슈퍼샘플링: 무작위 비율입니다. </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>20 </p> </td> 
   <td colname="col5"> <p>기본값은 5입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>미듐 </p> </td> 
   <td colname="col2"> <p>적응형 크기 조정: 깊이. </p> </td> 
   <td colname="col3"> <p>4 </p> </td> 
   <td colname="col4"> <p>8 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>N </p> </td> 
   <td colname="col2"> <p>적응형 크기 조정: 폭. </p> </td> 
   <td colname="col3"> <p>2 </p> </td> 
   <td colname="col4"> <p>10 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>P </p> </td> 
   <td colname="col2"> <p>포아송: 샘플/픽셀. </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>4 </p> </td> 
   <td colname="col5"> <p>기본값은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Y </p> </td> 
   <td colname="col2"> <p>Poisson: 토글을 사용합니다. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>기본값은 1입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>렌더링 효과(이전 셰이더)</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>I </p> </td> 
   <td colname="col2"> <p>강조 표시. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>J </p> </td> 
   <td colname="col2"> <p>채도를 강조 표시합니다. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>50 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H </p> </td> 
   <td colname="col2"> <p>밝은 재료의 그림자. </p> </td> 
   <td colname="col3"> <p>50 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>K </p> </td> 
   <td colname="col2"> <p>그림자 채도. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>400 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>광택에 의한 외삽강도. </p> </td> 
   <td colname="col3"> <p>100 </p> </td> 
   <td colname="col4"> <p>600 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0 </p> </td> 
   <td colname="col2"> <p>밝기 보상(확인란) </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p>기본값은 켜기(공백)이고 선택 해제됨 = F100G0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>대체 셰이더</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Z </p> </td> 
   <td colname="col2"> <p>기본 대비. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>기본값은 50입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>a </p> </td> 
   <td colname="col2"> <p>밝기 보상. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: a36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>b </p> </td> 
   <td colname="col2"> <p>채도 조정. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: b36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>c </p> </td> 
   <td colname="col2"> <p>그림자 조정. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: c36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>d </p> </td> 
   <td colname="col2"> <p>조정을 강조 표시합니다. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: d36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>e </p> </td> 
   <td colname="col2"> <p>반사 하이라이트. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: e36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>xx </p> </td> 
   <td colname="col2"> <p>모양. </p> </td> 
   <td colname="col3"> <p>-100 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>위 값의 'xx'를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> <p>조명 조정. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: k64.138.175.60.xx.133.242 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>u &amp; s </p> </td> 
   <td colname="col2"> <p>그림자 색조 이동. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: u8.1.2.3.4.5.6.7.8.s8.1.2.3.4.5.6.7.8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>v &amp; t </p> </td> 
   <td colname="col2"> <p>색조 이동을 강조 표시합니다. </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>다른 형식: v8.1.2.3.4.5.6.7.8.t8.1.2.3.4.5.6.7.8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>w </p> </td> 
   <td colname="col2"> <p>채도 조정. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>g </p> </td> 
   <td colname="col2"> <p>낮은 채도 증폭. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 샘플 고급 렌더링 설정 {#section-56528569eae44ecd997a289b211ff256}

<table id="table_062DCF66ACCC4A6997E3CA951C0A12B8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>컴포지션 설정 중 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>H60I30J10K200L400U1V10W100X0 </p> </td> 
   <td colname="col2"> <p>이미지 작성의 기본값. 
     <ul id="ul_AA7CF1A3E6984B318265BBE8FFFBB4EE">
      <li> USM1
      <li id="li_8EC075956E2E4D5A91355122DC9BC938">H60 = 밝은 재료의 그림자(50-100). </li> 
      <li id="li_F760B65E057146A7B56673D6B1A9A304">I30 = 강조 표시(0-100). </li> 
      <li id="li_376C275FDB3548958C09BD266C77318F">J10 = 채도를 강조 표시합니다(0~50). </li> 
      <li id="li_FE26429972F544869CDFE2DD61F39CC5">K200 = 그림자 채도(0-400). </li> 
      <li id="li_FB6BAA708427428AA4A3AC2E5D3B9932">L400 = 광택도 기반 외삽강도(100-600). </li> 
      <li id="li_6B2EEEE7F0D54E078462AAFC4E4FAB42">U1 = USM(언샵 마스크) (0-2). </li> 
      <li id="li_7CD4E3662A6C48F9B5895D133D28BA2A">V10 = USM 반경(1-100픽셀). </li> 
      <li id="li_949B6DB4959B46A892787CD5B3AD7485">W100 = USM 금액(1%-500%). </li> 
      <li id="li_F39D3834D4A2478D993E5E9C9B434CFE">X0 = USM 임계값(0~255 수준). </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C6E6DD90ECAB4D2B9284A25A29923DC6"> 
      <li id="li_7B7A8C43BCEB4CB58C7074974CAB0419">USM1 </li> 
      <li id="li_A003B68023424DCABBF3A2CAF98C39A4">모든 최대 및 밝기 보상이 켜져 있습니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_AAEC098CED1C436E933B1C1B88DFB659"> 
      <li id="li_0CC34CDD796E4DFD802824FF21DB021B">USM1 </li> 
      <li id="li_E36886FB1D00444CBA19D7245E89B292">최대 및 밝기 보상이 모두 꺼져 있습니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H100I100J50K400L600U2V100W500X255 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6BB668C6C055493DAAA38F4D3B9C20A7"> 
      <li id="li_D8BAFB41CF4C4B3FAD6F89AF5D7F223A">USM2 </li> 
      <li id="li_DA685F4DE4BA427BA7BE241A75C96152">최대 및 밝기 보상이 모두 꺼져 있습니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H80I70J40L300U1V8W80X5 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7C374842312E4AD0B62692BBCE6743A8"> 
      <li id="li_CC730580B54741FBBBFF507DE0FE1F15">H80 = USM 금액 </li> 
      <li id="li_C2801B2C093444AC9401793BC571EC27">I70 = 특징 </li> 
      <li id="li_518C6A690EC34614B0806A0C6BC535FF">J40 = 채도 강조 표시 </li> 
      <li id="li_F280CF29D1E341D9AC9C0C16C2DEA1E6">L300 = 광택 기반 외삽강도 </li> 
      <li id="li_3F589F109AC94280911BD535C49E42E4">U1 = USM </li> 
      <li id="li_113FEC9B37D54511BAB3FEAC7C271858">V8 = USM 반경 </li> 
      <li id="li_E1BA7406A76B476EB1A89D6EDD87930C">W80 = 밝은 재료의 그림자 </li> 
      <li id="li_AAD479EF6A7F43B98A8C147FCD684ECA">X5 = USM 임계값 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q5R3S11T103U1V6W120X5Z80b.188.88.75.37 </p> </td> 
   <td colname="col2"> <p>선명 효과를 사용한 대체 셰이더: </p> <p> 
     <ul id="ul_93AD53BB37EA47F6A3CEE424D3AAE18C"> 
      <li id="li_9EF1DF4167164721882E4842C2E0B20C">USM1 </li> 
      <li id="li_7B5D8B7BB5544E7FA4AD702EE281086B">USM 금액(120) </li> 
      <li id="li_B3BE096BB0654A2DBADDD6832E499F2A">USM 반경(0.6) </li> 
      <li id="li_793DAB145CE7469ABC1182BCBD324657">USM 임계값(5) </li> 
      <li id="li_B1954FEBE2084726828D64E8165DA4DA">크기 조정(란초) </li> 
      <li id="li_E5ED76998C0543D8A3F9AD178CFD3C2C">재샘플링(슈퍼샘플링, 무작위=절반, 속도=절반) </li> 
      <li id="li_CCEE53544E7D48858398BF3168F1E87D">대비(강함) </li> 
      <li id="li_EB0D25C095FB4D5798AC031AB759849B">채도 조정(가운데 첫 번째 교점, 모서리를 따라 두 번째 교점, 세 번째 교점 가운데 점 낮음) </li> 
      <li id="li_5C2304DA4A4D4799AE5DCCCB1E2ECBB3">선명하게(오른쪽으로 3/4 방향) </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- RB: I don't know why this is in here; it was added by someone else: 
Alternate Shader Rendering (default on) checkbox provides a more precise Advanced Shader diffuse rendering pipeline. For a number of effects it also provides an alternate Advanced Shader rendering pipeline. Note that the underlying OpenGL hardware must provide support for the Advanced (Per-Pixel) GLSL Shaders for this option to be vailable; else this checkbox is automatically disabled. -->

<!-- RB: I don't know why this is in here; it was added by someone else:
It should probably also go into the different renders - Render Effects and Alternate Shader - or link to descriptions of each. -->
