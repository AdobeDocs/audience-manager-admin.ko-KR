---
description: Audience Manager 관리 툴의 [서버] 페이지를 사용하여 새 HTTP 서버를 생성하거나 기존 서버를 편집합니다.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: HTTP 서버 만들기 또는 편집
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 2%

---

# HTTP 서버 만들기 또는 편집 {#create-or-edit-an-http-server}

Audience Manager 관리 도구의 [!UICONTROL Servers] 페이지를 사용하여 새 HTTP 서버를 만들거나 기존 서버를 편집합니다.

>[!NOTE]
>
>새 서버를 만들거나 기존 서버를 편집하려면 [!UICONTROL DEXADMIN] 역할이 있어야 합니다.

1. 새 서버를 만들려면 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**(으)로 이동합니다. 기존 서버를 편집하려면 **[!UICONTROL Label]** 열에서 원하는 서버를 클릭합니다.
1. 이 서버에 대해 원하는 레이블을 지정합니다.
1. **[!UICONTROL Protocol]** 드롭다운 목록에서 원하는 프로토콜을 선택합니다. [!DNL HTTP].
1. 다음 필드를 채웁니다.

   * **[!UICONTROL Domain]:** 이 서버에 대해 원하는 도메인(호스트)을 지정하십시오.
   * **[!UICONTROL Port]:** 이 서버에 대해 원하는 포트를 지정하십시오. 기본 포트는 각 암호화 유형에 대해 표시됩니다. 필요한 경우 기본 포트를 변경할 수 있습니다
   * **[!UICONTROL Maximum Users Per Request]:** 이 서버에 허용된 요청당 최대 사용자 수를 지정합니다.
   * **[!UICONTROL URL Prefix]:** 이 서버에 사용할 [!DNL URL] 접두사를 지정합니다.
   * **[!UICONTROL Authentication URL]:** 이 `HTTP` 서버에 대해 [!UICONTROL Authentication URL]을(를) 지정하십시오.
   * **[!UICONTROL Authentication]:** 원하는 인증 방법: **[!UICONTROL None]**, **[!UICONTROL Username/Password]** 또는 **[!UICONTROL SSH Key]**&#x200B;을(를) 지정합니다.
   * **[!UICONTROL HTTP Signature Header]:** 고객이 제공한 [!DNL HTTP] 서명 키가 포함된 [!DNL HTTP] 헤더의 이름입니다. 기본값은 아래 예와 같이 [!UICONTROL X-Signature]입니다.

     ```
     * Connected to partner.website.com (127.0.0.1) port 80 (#0)
     > POST /webpage HTTP/1.1
     > Host: partner.host.com
     > Accept: */*
     > Content-Type: application/json
     > Content-Length: 20
     > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
     POST message content
     ```

   * **[!UICONTROL HTTP Signature Key]:** 고객이 제공한 [!DNL HTTP] 요청에 서명하는 데 사용되는 키입니다.
   * **[!UICONTROL Show Signature Key]:** 브라우저에서 서명을 표시할지 여부를 전환합니다.
   * **[!UICONTROL HTTP Signature Encryption Method]:** 서명을 암호화하는 데 사용하는 메서드를 지정합니다. 고객이 별도로 원하지 않는 경우 [!UICONTROL SHA1]을(를) 사용합니다.

   >[!NOTE]
   >
   >파트너의 실시간 데이터 전송에 대해 [OAuth 2.0 인증](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=en)을 활성화하려면 아래 표와 같이 필드를 채우십시오. *기울임꼴*&#x200B;의 필드는 표에서와 정확히 동일하게 입력해야 합니다.

   | 이름 | 값 |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *승인*] |
   | [!UICONTROL Password] | your_password_here |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 새 서버를 만드는 경우 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 기존 서버를 편집하는 경우 **[!UICONTROL Update]**&#x200B;을(를) 클릭합니다.
