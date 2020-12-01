---
description: 베타 환경은 Audience Manager 구현을 테스트하는 것입니다. 베타에서 변경한 내용은 프로덕션 데이터에 영향을 주지 않습니다. Audience Manager 베타 환경은 제작 환경의 소규모 독립 실행형 버전입니다. 테스트할 모든 데이터는 이 환경에서 입력 및 수집되어야 합니다.
seo-description: 베타 환경은 Audience Manager 구현을 테스트하는 것입니다. 베타에서 변경한 내용은 프로덕션 데이터에 영향을 주지 않습니다. Audience Manager 베타 환경은 제작 환경의 소규모 독립 실행형 버전입니다. 테스트할 모든 데이터는 이 환경에서 입력 및 수집되어야 합니다.
seo-title: 베타 환경
solution: Audience Manager
title: 베타 환경
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
translation-type: tm+mt
source-git-commit: 7765dbf79c2fb6ca8c4b52fe8090c1fd11f9db27
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 3%

---


# 베타 환경 {#beta-environment}

베타 환경은 Audience Manager 구현을 테스트하는 것입니다. 베타에서 변경한 내용은 프로덕션 데이터에 영향을 주지 않습니다. Audience Manager 베타 환경은 제작 환경의 소규모 독립 실행형 버전입니다. 테스트할 모든 데이터는 이 환경에서 입력 및 수집되어야 합니다.

## 개요 {#overview}

<!-- beta_environment_admin.xml -->

| 서비스 | URL/호스트 이름 | 프로비전 단계 |
|--- |--- |--- |
| S3 |  | [Amazon S3 버킷 제공](admin-beta-environment.md#provision-s3-buckets)을 참조하십시오. |
| DCS | https&amp;콜론;//dcs-beta.demdex.net/.. | 우리 쪽에서는 추가 작업이 필요하지 않습니다. 베타 환경에서 [DCS 액세스](admin-beta-environment.md#access-dcs-beta-environment)를 참조하십시오. |
| UI | https&amp;콜론;//bank-beta.demdex.com | 데이터는 매월 프로덕션 환경에서 베타 환경으로 복사됩니다. 프로덕션 자격 증명은 베타에 사용할 수 있습니다. |
| API | https&amp;콜론;//api-beta.demdex.com/.. | 데이터는 매월 프로덕션 환경에서 베타 환경으로 복사됩니다. 프로덕션 자격 증명은 베타에 사용할 수 있습니다. |

## Amazon S3 버킷 제공 {#provision-s3-buckets}

>[!NOTE]
>
>[!DNL FTP/SFTP]을(를) 사용하지 않고 있습니다. 또한 아웃바운드 데이터 전송은 베타 환경에서 작동하지 않습니다.

인바운드 데이터에 대해 [!DNL S3] 버킷을 제공하려면:

1. [**SKMS 요청 TechOps 도움말**](https://skms.adobe.com/) 기능을 사용하십시오.
1. 왼쪽 탐색 레일의 **[!UICONTROL Request TechOps Help]**&#x200B;으로 이동합니다.
1. **[!UICONTROL Request Search]**&#x200B;에 검색 필드에 Audience Manager을 입력합니다.
1. 검색 결과에서 아래로 스크롤하고 **Audience Manager - S3 인바운드/아웃바운드 계정 프로비저닝**&#x200B;을 클릭합니다.
1. 프로비저닝 창의 필드를 채우고 **[!UICONTROL Environment]** 필드에 **샌드박스 환경**&#x200B;을 지정합니다.

>[!NOTE]
>
>[!DNL FTP/SFTP]의 사용을 중단하고 [!UICONTROL Amazon S3]의 사용을 권장합니다. [!UICONTROL Amazon S3]의 사용을 권장하는 이유는 [Amazon S3:About](https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/amazon-s3.html)에 나열되어 있습니다.

## 베타 환경에서 DCS에 액세스 {#access-dcs-beta-environment}

베타 환경에서 [!UICONTROL DCS]에 액세스하려면:

1. [!DNL curl] [command](https://curl.haxx.se/docs/manpage.html)를 사용하여 [!UICONTROL DCS] 호출을 만듭니다. [!DNL Curl] 은 지원되는 여러 프로토콜 중 하나를 사용하여 서버로부터 데이터를 전송하는 도구입니다.

   예: `curl -v https://dcs-beta.demdex.net/event`

1. [!UICONTROL DCS] 응답 헤더에서 &quot;[!DNL sandbox]&quot;을 검색하여 베타 [!UICONTROL DCS]에서 요청이 제공되었는지 확인하십시오.

   예:

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->