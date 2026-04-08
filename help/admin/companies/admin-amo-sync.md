---
description: 기본적으로 모든 회사는 Adobe Media Optimizer(AMO)와 데이터를 동기화합니다. 관리자 UI에서 각 회사 컨테이너에는 이 프로세스를 관리하는 데이터 소스가 있습니다. 이 데이터 소스는 Adobe AMO(ID 411)입니다. 선택한 회사에 대한 컨테이너 행(컨테이너 탭 아래)을 클릭하여 이 기본 동기화를 비활성화하거나 AMO 동기화 프로세스에 다른 데이터 소스를 추가 및 제거합니다.
seo-description: By default, all companies sync data with Adobe Media Optimizer (AMO). In the Admin UI, each company container has a data source that manages this process. This data source is Adobe AMO (ID 411). Click a container row (under the Containers tab) for a selected company to disable this default sync or to add and remove other data sources to the AMO sync process.
seo-title: ID Syncing with Media Optimizer
title: Media Optimizer와 ID 동기화
uuid: b741dfa7-2947-4288-b214-79eccf18d53a
exl-id: ebd978ef-3825-4a96-94bd-5cdae269cf7c
TQID: https://experienceleague.adobe.com/R6xtPWC964J1atGK-R0g6J5AG83PYJosHNE3-5LvMVE
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 2%

---

# Media Optimizer와 ID 동기화 {#id-syncing-with-media-optimizer}

기본적으로 모든 회사는 데이터를 [!DNL Adobe Media Optimizer]&#x200B;([!DNL AMO])과(와) 동기화합니다. [!UICONTROL Admin UI]에서 각 회사 컨테이너에는 이 프로세스를 관리하는 데이터 원본이 있습니다. 이 데이터 원본은 [!UICONTROL Adobe AMO]&#x200B;([!UICONTROL ID] 411)입니다. 선택한 회사의 컨테이너 행([!UICONTROL Containers] 탭 아래)을 클릭하여 이 기본 동기화를 사용하지 않도록 설정하거나 [!DNL AMO] 동기화 프로세스에 다른 데이터 원본을 추가하고 제거하십시오.

![](assets/id-sync.png)

## ID 동기화 상태 {#id-sync-status}

다음 표에서는 데이터 소스의 동기화 상태를 설명합니다.

| 상태 | 설명 |
|------ | -------- |
| 꺼짐 | [!DNL AMO]과(와) ID 동기화를 사용하지 않도록 설정하려면 이 컨테이너의 [!UICONTROL Selected Data Sources]에서 모든 데이터 원본을 제거하십시오. |
| 켜기(ID 서비스 버전에 관계없이) | 다음과 같은 경우 ID 서비스 버전에 관계없이 데이터 원본이 [!DNL AMO]과(와) 동기화됩니다. <ul><li>데이터 원본이 [!UICONTROL Selected Data Sources] 목록에 나타납니다.</li><li>[!DNL AMO] 확인란 *이(가) 선택되지 않았습니다*.</li></ul> |
| 켜기(ID 서비스 버전에 관계없이) | 다음과 같은 경우 데이터 원본은 ID 서비스 버전 2.0 이상의 [!DNL AMO]과(와) 동기화됩니다. <ul><li>데이터 원본이 [!UICONTROL Selected Data Sources] 목록에 나타납니다.</li><li>[!DNL AMO] 확인란 *is*&#x200B;을(를) 선택했습니다.</li></ul> |

>[!MORELIKETHIS]
>
>* [컨테이너 관리](../companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967)
