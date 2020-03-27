---
description: 카탈로그 속성 파일은 이러한 요청 속성을 인식합니다.
seo-description: 카탈로그 속성 파일은 이러한 요청 속성을 인식합니다.
seo-title: 속성 요청
solution: Experience Manager
title: 속성 요청
topic: Scene7 Image Serving - Image Rendering API
uuid: 02156b81-9f18-461e-94c1-43b1155c4ab6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Request attributes{#request-attributes}

카탈로그 속성 파일은 이러한 요청 속성을 인식합니다.

구문

<table id="simpletable_2690384A0117458DB12E4E99EFDA975A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> MaxPix</a></span> </p></td> 
  <td class="stentry"> <p>응답 이미지 크기 제한. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> DirectUrl <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-allowdirecturls.md#reference-cc649a518182497baacf9f6b19559689" type="reference" format="dita" scope="local"> 허용</a></span> </p></td> 
  <td class="stentry"> <p>절대 URL을 이미지 소스로 허용합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 루트 <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> URL</a></span> </p></td> 
  <td class="stentry"> <p>상대 이미지 소스 URL에 대한 루트 URL. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> RequestObfuscation <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> 설정</a></span> </p></td> 
  <td class="stentry"> <p>난독화 요청 모드. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> RequestLock <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"></a></span> </p></td> 
  <td class="stentry"> <p>요청 잠금 모드. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 워터마크 <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"></a></span> </p></td> 
  <td class="stentry"> <p>워터마크 템플릿 선택기. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ErrorImage <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"></a></span> </p></td> 
  <td class="stentry"> <p>오류 이미지 또는 템플릿입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 오류 <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561" type="reference" format="dita" scope="local"> 세부 사항</a></span> </p></td> 
  <td class="stentry"> <p>오류 메시지 세부 정보. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 트러스트된 <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-trusteddomains.md#reference-563bd5c54f914d9abcd2304ab292e12f" type="reference" format="dita" scope="local"> 도메인</a></span> </p></td> 
  <td class="stentry"> <p>swf 응답 이미지에 액세스할 수 있는 웹 도메인 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 기본 <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf" type="reference" format="dita" scope="local"> 만료</a></span> </p></td> 
  <td class="stentry"> <p>기본 이미지 응답에 대한 클라이언트 캐시 TTL입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> NonImgExpiration <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d" type="reference" format="dita" scope="local"></a></span> </p></td> 
  <td class="stentry"> <p>비이미지 응답에 대한 클라이언트 캐시 TTL. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 로케일 <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318" type="reference" format="dita" scope="local"> 맵</a></span> </p></td> 
  <td class="stentry"> <p>ID 번역 맵. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> LocaleStrMap <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e" type="reference" format="dita" scope="local"></a></span> </p></td> 
  <td class="stentry"> <p>문자열 현지화 맵. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> DefaultImage <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> Mode</a></span> </p></td> 
  <td class="stentry"> <p>기본 이미지 동작. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ClientAddressFilter( <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68" type="reference" format="dita" scope="local"> 클라이언트 주소 필터)</a></span> </p></td> 
  <td class="stentry"> <p>클라이언트 IP 주소 필터. </p></td> 
 </tr> 
</table>

