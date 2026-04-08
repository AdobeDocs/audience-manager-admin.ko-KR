---
description: '[OAuth2 클라이언트] 페이지에서는 Audience Manager 구성의 OAuth2 클라이언트 목록을 확인할 수 있습니다. 적절한 사용자 역할이 할당되면 기존 클라이언트를 편집 또는 삭제하거나 새 클라이언트를 만들 수 있습니다.'
seo-description: Use the OAuth2 Clients page to view a list of OAuth2 clients in your Audience Manager configuration. You can edit or delete existing clients or create new clients, providing that you have the appropriate user roles assigned.
seo-title: OAuth2 Clients
title: OAuth2 클라이언트
uuid: 3e654053-fb2f-4d8f-a53c-b5c3b8dbdaaa
exl-id: 993eae04-02e8-4554-a6fe-cf599053bfc9
TQID: https://experienceleague.adobe.com/8thJUCb1zoj8trr-6Zw4Uyq89KvJcw2xb8dRz8W7oVE
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: baaa0dd2-d27e-4921-aae3-7888623a5fa5
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 572
ht-degree: 1%

---

# OAuth2 클라이언트 {#oauth-clients}

[!DNL Audience Manager] 구성에서 [!UICONTROL OAuth2] 클라이언트 목록을 보려면 [!UICONTROL OAuth2 Clients] 페이지를 사용하십시오. 적절한 사용자 역할이 할당되면 기존 클라이언트를 편집 또는 삭제하거나 새 클라이언트를 만들 수 있습니다.

## 개요 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>고객이 Audience Manager 사용 안내서의 [OAuth2](https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) 설명서를 읽는지 확인하십시오.

[!DNL OAuth2]은(는) 리소스 소유자를 대신하여 [!DNL Audience Manager] 리소스에 대한 보안 위임된 액세스를 제공하기 위한 인증 개방형 표준입니다.

![](assets/oauth.png)

원하는 열의 헤더를 클릭하여 각 열을 오름차순 또는 내림차순으로 정렬할 수 있습니다.

[!UICONTROL Search] 상자나 목록 하단의 페이지 매김 컨트롤을 사용하여 원하는 클라이언트를 찾습니다.

## OAuth2 클라이언트 만들기 또는 편집 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Audience Manager [!UICONTROL Admin] 도구의 [!UICONTROL OAuth2 Clients] 페이지를 사용하여 새 [!UICONTROL Oauth2] 클라이언트를 만들거나 기존 클라이언트를 편집합니다.

1. 새 [!UICONTROL OAuth2] 클라이언트를 만들려면 **[!UICONTROL OAuth2 Clients]** > **[!UICONTROL Add OAuth2 Client]**&#x200B;을(를) 클릭합니다. 기존 [!UICONTROL OAuth2] 클라이언트를 편집하려면 **[!UICONTROL Client ID]** 열에서 원하는 클라이언트를 클릭합니다.
1. 이 [!UICONTROL OAuth2] 클라이언트에 대해 원하는 이름을 지정하십시오. 이 이름은 레코드에 대해서만 사용됩니다.
1. [!UICONTROL OAuth2] 클라이언트의 전자 메일 주소를 지정하십시오. 이메일 주소는 한 개로 제한됩니다.
1. **[!UICONTROL Partner]** 드롭다운 목록에서 원하는 파트너를 선택합니다.
1. **[!UICONTROL Client ID]** 상자에서 원하는 ID를 지정합니다. [!DNL API]개의 요청을 제출할 때 사용되는 값입니다. 이전 단계의 드롭다운 목록에서 [!UICONTROL Partner]을(를) 선택한 후 입력을 시작하면 접두사가 자동으로 채워집니다. 올바른 형식은 &lt; *`partner subdomain`*> - &lt; *`Audience Manager username`*>입니다.
1. 원하는 대로 **[!UICONTROL Restrict to Partner Users]** 확인란을 선택하거나 선택 취소하십시오. 이 확인란을 선택한 경우 사용자는 선택한 파트너에 대해 나열된 [!DNL Audience Manager] 사용자여야 합니다. 가장 좋은 방법은 이 옵션을 선택하는 것입니다.
1. **[!UICONTROL Scope]** 섹션에서 원하는 대로 **[!UICONTROL Read]** 및 **[!UICONTROL Write]** 확인란을 선택하거나 선택 취소합니다.
1. **[!UICONTROL Grant Type]** 섹션에서 원하는 인증 수단을 선택합니다. [!UICONTROL Password] 및 [!UICONTROL Refresh-token] 옵션의 기본 설정을 사용하는 것이 좋습니다.

   * **[!UICONTROL Implicit]**: 이 옵션을 선택하면 [!UICONTROL Redirect URI] 상자가 활성화됩니다. 사용자는 인증된 후 자동 액세스 토큰을 받게 되고 즉시 리디렉션 [!DNL URI]&#x200B;(으)로 전송됩니다.
   * **[!UICONTROL Authorization Code]**: 이 옵션을 선택하면 [!UICONTROL Redirect URI] 상자가 활성화됩니다. 사용자가 인증되면 클라이언트로 반환되고 리디렉션 [!DNL URI]&#x200B;(으)로 전송됩니다.
   * **[!UICONTROL Password]**: 사용자가 인증 서버를 통한 자동 유효성 검사 시도 대신 사용자가 입력한 암호로 인증되었습니다.
   * **[!UICONTROL Refresh_token]**: 만료된 액세스 토큰을 장기간 새로 고치는 데 사용됩니다.

1. **[!UICONTROL Redirect URI]** 상자에서 원하는 [!DNL URI]을(를) 지정합니다. 이 옵션은 **[!UICONTROL Implicit]** 및 **[!UICONTROL Authorization_code]** 부여 유형을 선택한 경우에만 활성화됩니다. **[!UICONTROL Redirect URI]** 상자를 사용하면 허용되는 [!DNL URI] 값을 쉼표로 구분한 값을 지정할 수 있습니다. [!DNL API] 액세스를 위해 클라이언트를 승인한 후 클라이언트의 [!DNL URI] 사용자가 리디렉션됩니다.
1. 액세스 및 새로 고침 토큰 만료에 대해 원하는 만료 시간(초)을 지정합니다.

   * **[!UICONTROL Access Token Expiration Time]**: 액세스 토큰이 발급된 후 유효한 시간(초)입니다. 플랫폼 기본값(12시간)을 사용하려면 null일 수 있습니다. 또한 액세스 토큰이 만료되지 않았음을 나타내는 -1일 수도 있습니다.
   * **[!UICONTROL Refresh Token Expiration Time]**: 새로 고침 토큰이 발급된 후 유효한 시간(초)입니다. 플랫폼 기본값(30일)을 사용하려면 null일 수 있습니다.

1. **[!UICONTROL Save]** 아이콘을 클릭합니다.

[!UICONTROL OAuth2] 클라이언트를 삭제하려면 **[!UICONTROL OAuth2 Clients]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Actions]** 열의 ![](assets/icon_delete.png)을(를) 클릭하여 원하는 클라이언트를 찾습니다.

>[!MORELIKETHIS]
>
>* [API 요구 사항 및 권장 사항](../admin-oauth2/aam-admin-api-requirements.md)
