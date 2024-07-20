---
description: 고객이 Audience Manager API를 사용할 때 인식하도록 권장해야 하는 사항.
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API 요구 사항 및 Recommendations
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# API 요구 사항 및 Recommendations {#api-requirements-and-recommendations}

클라이언트가 [!DNL API] Audience Manager을 사용하여 작업할 때 인식하도록 권장해야 하는 사항입니다.

## 요구 사항 {#requirements}

[!DNL Audience Manager] [!DNL API] 코드를 사용하여 작업할 때 다음 사항에 유의하십시오.

* **요청 매개 변수:** 달리 지정하지 않는 한 모든 요청 매개 변수가 필요합니다.
* **[!DNL JSON]콘텐츠 형식:** 코드에서 `content-type: application/json` *및* `accept: application/json`을(를) 지정합니다.

* **요청 및 응답:** 요청을 올바른 형식의 [!DNL JSON] 개체로 보냅니다. [!DNL Audience Manager]이(가) 형식이 지정된 [!DNL JSON] 데이터로 응답합니다. 서버 응답에는 요청된 데이터, 상태 코드 또는 두 가지 모두 포함될 수 있습니다.

* **액세스:** [!DNL Audience Manager] 컨설턴트가 [!DNL API]개의 요청을 할 수 있는 클라이언트 ID와 키를 제공합니다.

* **설명서 및 코드 샘플:** *기울임꼴*&#x200B;의 텍스트는 [!DNL API] 데이터를 만들거나 받을 때 제공하거나 전달하는 변수를 나타냅니다. *italicized* 텍스트를 코드, 매개 변수 또는 기타 필수 정보로 바꾸십시오.

## Recommendations: 일반 API 사용자 만들기 {#recommendations}

[!DNL API] Audience Manager 작업을 위해 별도의 기술 사용자 계정을 만드는 것이 좋습니다. 이는 클라이언트 조직의 특정 사용자에게 연결되거나 연결되지 않은 일반 계정입니다. 이 유형의 [!DNL API] 사용자 계정은 다음 두 가지 작업을 수행하는 데 도움이 됩니다.

* [!DNL API]을(를) 호출하는 서비스(예: [!DNL API]을(를) 사용하는 클라이언트 앱의 호출 또는 대량 변경을 통한 호출)를 식별합니다.
* [!DNL API]에 중단 없이 액세스하십시오. 특정 직원에 연결된 계정은 퇴사할 때 삭제할 수 있습니다. 이렇게 하면 고객이 사용 가능한 [!DNL API] 코드를 사용할 수 없습니다. 특정 직원에게 연결되지 않은 일반 계정은 이 문제를 방지하는 데 도움이 됩니다.

이 유형의 계정에 대한 사용 사례로, 고객이 [대량 관리 도구](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=en)를 사용하여 한 번에 많은 세그먼트를 변경하려고 한다고 가정해 보겠습니다. 이를 수행하려면 [!DNL API] 액세스 권한이 필요합니다. 특정 사용자에게 권한을 추가하는 대신 [!DNL API]을(를) 호출할 수 있는 적절한 자격 증명, 키 및 암호가 있는 비특정 [!DNL API] 사용자 계정을 만듭니다. 이는 클라이언트가 [!DNL Audience Manager] [!DNL API]을(를) 사용하는 자체 응용 프로그램을 개발하는 경우에도 유용합니다.
