﻿---
title: Lync Server 2013으로 대규모 모임 지원
TOCTitle: Lync Server 2013으로 대규모 모임 지원
ms:assetid: 509a424f-a33d-4e72-8f87-a3ec7bb1ddeb
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/JJ204894(v=OCS.15)
ms:contentKeyID: 49303622
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013으로 대규모 모임 지원

 

_**마지막으로 수정된 항목:** 2012-10-03_

대규모 모임은 다음과 같은 특성을 갖기 때문에 이전 섹션에서 설명한 테스트 모델을 따르지 않습니다.

  - 모임 형식이 일대다 프레젠테이션입니다.

  - 한 명 또는 소수의 사용자가 발표자이고 그외 모든 사람은 참석자로만 모임에 참가합니다.

  - PowerPoint 프레젠테이션 공유가 기본 데이터 공동 작업 활동입니다.

  - 오디오가 필요하고 비디오를 사용할 수도 있습니다.

  - 모임 이끌이 또는 이끌이의 보조 등 전담 사용자가 미리 모임을 설정합니다.

  - 전담 직원(발표자가 아님)이 온라인 모임에 연결하고, 오디오, 비디오 및 슬라이드 공유가 작동하는지 확인하고, 대기실 및 사용자 역할을 관리하고, 참가자를 음소거하거나 음소거를 해제하고, 질문을 받고, 기록을 관리하는 등 모임을 적절하게 운영합니다.

최대 1000명의 사용자를 포함하는 대규모 모임을 지원하기 위해서는 공유 하드웨어 모델 및 비예약 모델 모두와 관련된 문제를 해결해야 합니다.

최대 1000명의 사용자로 구성된 모임에 충분한 CPU 및 메모리 리소스를 확보하기 위해서는 호스팅 프런트 엔드 서버가 다른 IM(인스턴트 메시징) 및 현재 상태 또는 Enterprise Voice 작업 부하를 호스팅하지 않아야 합니다. 또한 다른 모임의 크기에 관계없이 다른 모임을 호스팅해서도 안됩니다. 즉, 최대 1000명의 사용자로 구성된 모임을 호스팅하기 위해서는 최대 1000명의 사용자로 구성된 대규모 모임의 호스트를 전담하는 별도의 Lync Server 풀을 설정해야 합니다.

대규모 모임 호스트를 전담하는 Lync Server 풀은 동시에 최대 1000명의 사용자로 구성된 모임을 반드시 하나만 호스팅해야 합니다. 따라서 프런트 엔드 서버로부터 전담 지원을 받을 수 있도록 대역 외 예약 프로세스를 통해 모임 시간을 미리 예약해야 합니다. 동시에 두 개 이상의 대규모 모임을 지원하기 위해서는 여러 개의 전용 대규모 풀을 설정하는 것이 좋습니다.

대규모 모임의 온라인 부분은 전담 사용자가 실행하고 모니터링하는 것이 좋습니다. 이 사용자는 조직의 상황에 따라 이끌이거나 이끌이 또는 발표자의 대리인 또는 전담 대규모 모임 지원 팀의 구성원일 수 있습니다.

다음 섹션에서는 대규모 모임 시나리오를 지원하기 위해 Lync Server 2013 사용에 대한 최선의 방법을 포함하여 대규모 모임의 전용 풀 구현 방법에 대해 설명합니다.

## 이 단원의 내용

  - [대규모 모임을 위한 지원 설정](lync-server-2013-setting-up-support-for-large-meetings.md)

  - [대규모 모임 관리](lync-server-2013-managing-large-meetings.md)
