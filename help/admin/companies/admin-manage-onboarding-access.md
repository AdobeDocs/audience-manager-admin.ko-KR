---
description: 파일 및 데이터가 실수로 다른 파트너나 고객이 소유한 대상 데이터 소스에 온보딩되는 것을 방지하기 위해 Audience Manager은 파트너 ID(PID)와 다른 파트너가 소유한 데이터 소스 간의 매핑 요구 사항을 추가했습니다.
title: 타사 데이터에 대한 온보딩 액세스 관리
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
TQID: https://experienceleague.adobe.com/ajdpBCvsikCo-lxT98GNrwCyc2IW-AZCg73oU18leTY
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 0%

---

# 타사 데이터에 대한 온보딩 액세스 관리 {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> 이 페이지의 대상은 Adobe 내부 직원입니다. 이 페이지에 설명된 대로 타사 데이터 소스 매핑을 요청하는 Audience Manager 고객인 경우 고객 지원 센터 또는 기술 계정 관리자에게 문의하십시오.
> 기존 데이터 공유 관계에 대한 매핑을 요청할 필요는 없습니다. PID에 속하는 대상 데이터 소스에 데이터를 온보딩할 때도 매핑이 필요하지 않습니다.

파일 및 데이터가 실수로 다른 파트너가 소유한 대상 데이터 소스에 온보딩되는 것을 방지하기 위해 Audience Manager은 파트너 ID(PID)와 다른 파트너가 소유한 데이터 소스(DPID) 간의 매핑 요구 사항을 추가했습니다. Audience Manager ID의 [인덱스](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html)에서 PID 및 DPID에 대해 자세히 알아보십시오.

제2자 데이터 공유를 위해 Audience Manager 파트너 또는 고객이 소유하지 않은 대상 데이터 소스로 파일을 수집하려는 경우 파트너 ID(PID)와 특정 데이터 소스(DPID) 간의 매핑을 요청해야 합니다. 매핑이 누락된 경우 인바운드 데이터 작업에 의해 파일이 처리되지 않고 데이터가 Audience Manager에 온보딩되지 않습니다.

이러한 매핑을 생성하려면 Audience Manager 엔지니어링 팀에 Jira 티켓을 제출하십시오. 샘플 Jira 티켓 [여기](https://jira.corp.adobe.com/browse/AAM-60353)를 확인하십시오. 기존 데이터 공유 관계에 대해 매핑을 생성하도록 요청할 필요가 없습니다.
