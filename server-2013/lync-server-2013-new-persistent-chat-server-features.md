﻿---
title: 'Lync Server 2013: 새 영구 채팅 서버 기능'
TOCTitle: 새 영구 채팅 서버 기능
ms:assetid: c3ec6f33-6261-4bf5-aa31-baa8ab2a87d8
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg412965(v=OCS.15)
ms:contentKeyID: 49304948
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013의 새 영구 채팅 서버 기능

 

_**마지막으로 수정된 항목:** 2012-10-29_

Lync Server 2013의 영구 채팅 서버을 사용하면 특정 주제에 관한 지속적인 단체 대화에 참가할 수 있습니다. 영구 채팅 서버는 조직이 다음을 수행하는 데 도움이 될 수 있습니다.

  - 지리적으로 분산되고 업무가 연관된 팀 간의 통신을 향상시킵니다.

  - 보다 많은 구성원과 정보를 보다 많이 공유할 수 있습니다.

  - 조직 내외부에서 광범위하게 정보를 공유할 수 있습니다.

  - 효율적인 정보 공유로 정보 오버로드를 줄여 줍니다.

  - 정보 인식을 향상시킵니다.

  - 중요한 지식과 정보의 배포를 향상시킵니다.

Lync Server 2013의 영구 채팅 서버는 Microsoft Office 365에서 사용할 수 없으며, 현재 온-프레미스 Lync 2013 고객만 사용할 수 있습니다.

Lync 2013에서 영구 채팅 기능은 Lync 2013 클라이언트에 통합됩니다. 따라서 메신저, 현재 상태, 오디오/비디오, 회의, 영구 채팅을 모두 Lync 2013 클라이언트에서 액세스할 수 있습니다. Lync 2013 클라이언트에 대한 자세한 내용은 <http://go.microsoft.com/fwlink/p/?linkid=270877>을 참고하세요.

이 항목에서는 다음을 포함하여 새 버전( Lync Server 2013영구 채팅 서버) 및 이전 버전( Microsoft Lync Server 2010, 그룹 채팅) 간 기능 변경 사항에 대해 설명합니다.

  - Lync Server 제어판에 관리 환경을 제공하고 그룹 채팅 관리 도구를 제거했습니다.

  - 그룹 채팅 구성 도구를 제거하여 영구 채팅 서버의 구성 설정을 토폴로지 작성기에 통합했습니다.

  - 이전 버전의 영구 채팅 서버에서 쉽게 마이그레이션 및 업그레이드할 수 있습니다.

  - 고가용성 및 재해 복구 솔루션을 제공합니다.

최신 버전의 영구 채팅 서버에 대한 자세한 내용은 다음을 참조하십시오.

  - 영구 채팅 기능, 기능 작동 방식 및 영구 채팅 서버을 실행 중일 때 기능을 사용하는 방법에 대한 자세한 목록을 제공하는 영구 채팅 도움말(<http://go.microsoft.com/fwlink/p/?linkid=270945>)

  - 계획 설명서의 [Lync Server 2013의 영구 채팅 서버 계획](lync-server-2013-planning-for-persistent-chat-server.md), 배포 설명서의 [Lync Server 2013에서 영구 채팅 서버 배포](lync-server-2013-deploying-persistent-chat-server.md), 마이그레이션 설명서의 [Lync Server 2010, 그룹 채팅 또는 Office Communications Server 2007 R2 그룹 채팅에서 Lync Server 2013, 영구 채팅 서버로 마이그레이션](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md) 및 작업 설명서의 [Lync Server 2013, 영구 채팅 서버 관리](managing-lync-server-2013-persistent-chat-server.md). 모두 영구 채팅 서버 설정에 대한 지침을 제공합니다.

  - 영구 채팅 서버 Documentation.msi 파일(Windows Installer 파일)을 통해 사용자는 영구 채팅 서버에 대한 광범위한 오프라인 설명서에 액세스할 수 있습니다.

## 영구 채팅 서버의 주요 토폴로지 변경 사항

다음은 영구 채팅 서버의 변경 사항을 간략히 정리한 것입니다.

영구 채팅 서버는 이제 서버 역할을 수행합니다. Microsoft Lync Server 2010에서 그룹 채팅 서버는 Microsoft Lync Server 2010에 사용되는 신뢰할 수 있는 타사 응용 프로그램이었습니다. 영구 채팅은 토폴로지 작성기를 사용하여 Lync Server 2013 토폴로지에 추가될 수 있습니다. Lync Server 2013에서 영구 채팅 서버 기능은 다음과 같이 새로운 세 가지 서버 역할을 사용하여 구현됩니다.

  - **PersistentChatService :** 이는 영구 채팅을 위한 프런트 엔드 역할입니다. Standard Edition 배포에서 영구 채팅 서버 서비스 역할은 다른 Lync Server 역할과 마찬가지로 부트스트래퍼로 배포된 Standard Edition 서버에 함께 배치됩니다. Enterprise Edition 배포에서 영구 채팅 서비스 역할은 다른 Lync Server 역할과 마찬가지로 부트스트래퍼에 의해 독립 실행형 컴퓨터에 배포됩니다.

  - **PersistentChatStore :** 영구 채팅 콘텐츠 데이터베이스에 해당하는 백 엔드 서버 역할로, 여기에 모든 채팅 콘텐츠가 저장됩니다.

  - **PersistentChatComplianceStore :** 영구 채팅 준수 데이터베이스에 해당하는 백 엔드 서버 역할로, 여기에 모든 준수 이벤트가 저장됩니다.

이러한 영구 채팅 서버 역할은 선택 사항이며 포괄적인 영구 채팅 서버 기능을 원하는 고객만 설치합니다. **PersistentChatComplianceStore** 역할은 영구 채팅 규정 준수를 배포하도록 선택한 경우에만 필요합니다.

**PersistentChatService** 역할은 다음 두 서비스를 실행합니다.

  - 영구 채팅 서비스

  - 영구 채팅 Compliance Service

이러한 서비스를 각 영구 채팅 서버에서 실행하면 여러 서버의 영구 채팅 서버 풀에서 이러한 서비스의 고가용성이 제공됩니다.

또한 영구 채팅방에서 파일 업로드 및 다운로드를 지원하기 위해 영구 채팅 서버에 웹 서비스가 포함됩니다. 이전에 이 서비스는 영구 채팅 서버프런트 엔드 서버에 함께 배치되었으며 IIS(인터넷 정보 서비스)를 필수 구성 요소로 설치해야 했습니다. Lync Server 2013영구 채팅 서버에서는 파일 업로드/다운로드 웹 서비스가 Lync Server 2013프런트 엔드 서버와 함께 배치됩니다. 따라서 IIS(인터넷 정보 서비스)가 더 이상 영구 채팅 서버의 필수 구성 요소가 아닙니다. 파일 업로드/다운로드 웹 서비스는 IIS(인터넷 정보 서비스) 관리자에서 **PersistentChat**으로 식별됩니다.


> [!IMPORTANT]
> <STRONG>PersistentChatService</STRONG> 역할을 Lync Server 2013프런트 엔드 서버와 동일한 서버에서 실행할 수 있는 경우는 해당 프런트 엔드 서버가 Standard Edition프런트 엔드 서버인 경우뿐입니다. <STRONG>PersistentChatService</STRONG> 역할은 Lync Server 2013프런트 엔드 서버와 별도로 실행할 수 없으며, Lync Server 2013 배포 환경 내에서만 설치될 수 있습니다.



영구 채팅 서버에서 조회 서비스가 제거되었습니다. Lync Server 2010, 그룹 채팅에서 조회 서비스는 모든 그룹 채팅 서버프런트 엔드 서버에서 실행되었으며, 채널 서버 중 하나로의 라우팅을 수행했습니다. Lync Server 2013은 대화 상대 개체를 사용하여 라우팅을 수행하며, 여기서 각 영구 채팅 서버 풀은 Lync Server프런트 엔드 서버에 사용되는 대화 상대 개체로 표시되며, 요청을 식별하고 적합한 영구 채팅 서버 풀로 라우팅한 후 다시 풀에서 영구 채팅 서버를 실행하는 컴퓨터 중 하나로 라우팅합니다.

Lync Server 2013에서 Compliance Service가 다음과 같이 수정되었습니다.

  - Lync Server 2010에서 Compliance Service는 함께 배치되는 것이 아닌 단일 서버에서만 독립 실행형으로 실행될 수 있었습니다. 이제 Compliance Service는 모든 영구 채팅 서버프런트 엔드 서버에서 영구 채팅 서비스와 함께 실행될 수 있으므로 여러 서버의 영구 채팅 서버 풀에서 고가용성을 제공할 수 있습니다. 준수 데이터베이스에서 데이터를 추출하고 이를 다른 시스템 중 하나(XML 파일, Exchange에 호스팅된 보관 파일 등)로 보내도록 단일 준수 어댑터를 구성할 수 있습니다. 영구 채팅 서버에 XML 어댑터가 포함됩니다.

  - 각 영구 채팅 서버프런트 엔드 서버에서 영구 채팅 서비스 및 Compliance Service로 공유되는 메시지 큐(일명 MSMQ)가 이제 두 서비스에만 공유되는 비공개 큐가 되었습니다. 모든 Compliance Service는 데이터를 해당 어댑터 인스턴스에 보내기 위해 읽기/쓰기 작업을 동일한 준수 백 엔드 데이터베이스에서 수행합니다. 준수 백 엔드 서버는 새 백 엔드 서버 역할로 표시됩니다.
    

    > [!IMPORTANT]
    > 이전 버전과 마찬가지로 모든 준수 데이터는 한 번만 처리됩니다. 데이터는 다양한 Lync Server 2013영구 채팅 서버 컴퓨터에서 실행되는 Compliance Service에 의해 호출된 모든 어댑터 인스턴스에서 처리될 수 있습니다. 영구 채팅 서버에서는 어느 어댑터 인스턴스든지 데이터를 처리할 수 있습니다.

    

    > [!NOTE]
    > 메시지 큐 설치에 대한 자세한 내용은 배포 설명서의 <A href="lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md">Lync Server 2013의 서버에 운영 체제 및 필수 구성 요소 소프트웨어 설치</A>를 참조하십시오.



Lync Server 2013에서 고가용성 및 재해 복구 기능이 다음과 같이 향상되었습니다.

  - 고가용성 개선 사항: SQL Server 미러링이 사용되어 사이트의 데이터 센터 내에 있는 영구 채팅 서버 콘텐츠 데이터베이스 및 영구 채팅 준수 데이터베이스에 대해 고가용성이 보장됩니다.

  - 재해 복구 개선 사항: 영구 채팅 서버는 확장된 풀 아키텍처를 지원하므로 단일 영구 채팅 서버 풀을 두 사이트에 걸쳐 확장할 수 있습니다. 즉, 풀의 두 서버가 물리적으로 두 사이트에 위치한 경우에도 토폴로지에 단일 논리 풀로 표시됩니다. 사이트 간 재해 복구에는 SQL Server 로그 전달이 사용됩니다.

고가용성 및 재해 복구에 대한 자세한 내용은 배포 설명서의 [Lync Server 2013에서 고가용성 및 재해 복구를 위한 영구 채팅 서버 구성](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md)을 참조하십시오.

## 영구 채팅 서버의 주요 관리 기능 변경 사항

Lync Server 2013에서 영구 채팅 서버의 관리 기능이 다음 기능을 제공하면서 더 간편해졌습니다.

  - 통합된 관리 기능. Lync Server 2013에서는 Lync 관리자들에게 이미 익숙한 도구를 사용하여 영구 채팅 서버 관리 기능의 편의성을 높였습니다. 영구 채팅 서버에는 Lync Server 제어판과 통합되는 관리 사용자 인터페이스가 제공되므로 이전 버전의 그룹 채팅 서버 사용자 인터페이스에서 발생했던 성능 문제를 해결합니다. 또한 영구 채팅 서버에는 영구 채팅 서버 범주, 영구 채팅 서버 채팅방(채팅방 삭제, 오래된 내용 삭제 등) 및 추가 기능을 관리할 수 있는 다양한 Windows PowerShell cmdlet이 포함되어 있습니다.

  - 간소화된 관리 모델. 고객의 주요 요구 사항을 충족하기 위해 Lync Server 2013의 영구 채팅 서버 모델이 간소하게 변경되었습니다.
    
      - 범위 및 범주에 대해 복잡하게 중첩된 계층 구조가 제거되었습니다.
    
      - 영구 채팅 서버로의 마이그레이션을 계획하고 있는 현재 MindAlign 고객을 위해 거부 목록과 허용 목록(범위)을 정의할 수 있도록 지원합니다.

## 이전 그룹 채팅 서버 버전과의 사용자 역할 차이점

Lync Server 2010, 그룹 채팅에는 사용자 관리자 역할, 채팅방 관리자 역할 및 추가 기능을 관리할 수 있는 Lync Server 관리자가 있었습니다. 영구 채팅 서버에서는 간단하게 영구 채팅 관리자 역할을 제공하며, 이는 다른 Lync Server RBAC(역할 기반 액세스 제어) 역할과 유사합니다. 이 RBAC 역할에 속한 사용자는 채팅방, 추가 기능, 범주 및 영구 채팅 서버 풀 구성을 관리할 수 있습니다. 또한 범주를 관리하기 위해 해당 범주의 사용자 액세스 권한을 부여받습니다.

## 이전 그룹 채팅 서버 버전과의 채팅방 범주 차이점

채팅방 범주는 더 이상 중첩될 수 없으며 루트 범주는 수정될 수 없습니다. AllowedMembers/DeniedMembers는 거부됨 목록 지정을 지원하지 않던 점을 제외하고 기존 그룹 채팅 서버 버전에서 사용되던 범위로 구성됩니다. 이제 중첩된 범주가 지원되지 않으므로 범위를 더 이상 재정의할 수 없습니다. Lync Server 2013의 영구 채팅 관리자는 채팅방 범주를 만들고 관리할 수 있습니다. 채팅방 범주를 만들과 관리하는 과정에서 영구 채팅 관리자는 액세스 권한이 있는 계정(Active Directory 그룹/컨테이너/사용자)을 특정 범주의 대화방 구성원/생성자로 구성할 수 있습니다. 영구 채팅 관리자는 또한 DeniedMembers를 범주에 추가하여 이들이 허용된 목록에서 명시적으로 제외되도록 설정할 수 있습니다. DeniedMembers는 AllowedMembers보다 우선 적용됩니다.

## 이전 그룹 채팅 서버 버전과의 채팅방 속성 차이점

공개 채팅방이라는 새로운 개념이 Lync Server 2013영구 채팅 서버에 도입되었습니다. 허용되는 모든 구성원은 배타적 구성원 자격 없이 채팅방에 참여할 수 있습니다.

영구 채팅 서버의 이전 버전에 포함되던 다음 채팅방 속성이 제거되었습니다.

  - 주제: 이제는 채팅방에 대한 '설명'만 존재합니다.

  - 새 구성원 목록 만들기: 영구 채팅 서버에서 모든 채팅방은 구성원 자격이 빈 상태로 시작하여 최대 '허용된 구성원'과 동등한 구성원 자격까지 확장될 수 있습니다.

  - 파일 업로드: 파일 업로드/다운로드를 허용할지 여부를 제어하기 위해 설정이 채팅방별로 구성되었습니다. 하지만 이제 범주 수준에서 설정하여 해당 범주의 모든 채팅방에 적용할 수 있습니다.

  - 채팅 기록: 채팅 기록을 사용할지 여부를 제어하기 위해 설정이 채팅방별로 구성되었습니다. 하지만 이제 범주 수준에서 설정하여 해당 범주의 모든 채팅방에 적용할 수 있습니다.

  - 초대: 채팅방은 범주의 초대 설정을 항상 상속받지만 채팅방별로 해당 기능을 해제할 수 있습니다. 이전에 초대를 해제하도록 설정된 범주에 속한 채팅방의 경우 초대를 설정할 수 없습니다.

## 이전 그룹 채팅 서버 버전과의 정책 차이점

영구 채팅 서버에서는 사용자/풀/사이트/전역 설정별로 영구 채팅에 새로운 Lync 정책을 사용하도록 설정할 수 있습니다. Lync 2013 클라이언트에서 영구 채팅 환경은 직접적이든, 풀/사이트/전역 설정을 통하든 상관없이 영구 채팅에 대한 정책이 설정된 사용자만 사용할 수 있습니다.

이전 버전의 그룹 채팅 서버에는 Lync Server 정책에 통합되는 정책이 없었습니다. 사용자 단위 및 범주/채팅방 단위로, 사용자별 **Can Upload Files(파일 업로드 가능)** 기능을 통해 사용자를 사용자 관리자, 채팅방 관리자로 설정하거나 사용자의 파일 업로드 기능을 구성할 수 있었습니다. 영구 채팅 서버의 **파일 업로드** 기능은 범주 단위로 구성할 수 있습니다.

## 로깅

영구 채팅 서버 및 System Center Operations Manager에 대한 로깅 기능이 Lync Server 2013 추적 로깅에 통합되었습니다.

## 참고 항목

#### 기타 리소스

[Lync Server 2013의 영구 채팅 서버 계획](lync-server-2013-planning-for-persistent-chat-server.md)
