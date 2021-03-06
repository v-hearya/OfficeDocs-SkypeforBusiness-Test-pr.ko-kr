﻿---
title: 'Lync Server 2013: 질문과 대답: Skype 연결을 위한 Lync Server 프로비전'
TOCTitle: '질문과 대답: Skype 연결을 위한 Lync Server 프로비전'
ms:assetid: 4d1b2bfc-780b-4b8c-afd5-11c2e59203b5
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Dn440172(v=OCS.15)
ms:contentKeyID: 59602771
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 질문과 대답: Skype 연결을 위한 Lync Server 2013 프로비전

 

_**마지막으로 수정된 항목:** 2015-07-22_

**질문: Microsoft Lync 및 Skype 간 지원되는 기능은 무엇인가요?**

**답변:** Skype가 Microsoft 제품군의 일부가 되면서, 통합 통신 방식을 수억 명의 Skype 사용자로 확장할 수 있는 새로운 가능성이 열렸습니다. 이러한 조합으로 Lync 고객은 Lync의 풍부한 기능과 Skype의 액세스 기능을 기반으로 공급자, 고객, 파트너와 연락 및 공동 작업을 할 수 있습니다.

  - 메신저 및 음성/비디오 통화 - Lync 사용자와 Skype 사용자 간에 연결된 음성/비디오 통화 및 메신저 대화

  - 현재 상태 공유 - 연동된 대화 상대 간에 현재 상태 정보 교환

  - 간편한 관리 - 조직의 정책 및 기준에 따라 페더레이션 통신을 구성하는 설정 및 제어

**질문: Lync 배포와 Skype를 연결하기 위한 자격 요건은 어떻게 되나요?**

**답변:** 다음 중 하나를 충족하는 경우 Skype 연결을 사용할 수 있습니다.

  - Skype에 연결할 조직의 사용자 및/또는 장치에 Lync Server(2010 또는 2013) 및 Lync Server 표준 클라이언트 액세스 라이선스("CALs" 2010 또는 2013)가 있음

  - Lync Online(독립 실행형 라이선스 또는 Office 365 제품군의 일부).  하지만 이 서비스(pic.lync.com)는 Lync Server, 하이브리드 Lync Server, Lync Online 배포 프로비저닝을 위한 것입니다.  Lync Online PIC 프로비저닝은 Lync Online 제어판(LOCP)에서 수행됩니다.

**질문: Skype 대화 상대와 연결하기 위해 Lync 사용자는 무엇을 해야 하나요?**

**답변:** 조직의 Lync 관리자가 도메인을 활성화하고 기능을 사용할 수 있도록 설정하면 Lync 사용자는 Skype 대화 상대를 Lync 클라이언트의 대화 상대 목록에 추가할 수 있습니다.

**질문: Lync 대화 상대와 연결하기 위해 Skype 사용자는 무엇을 해야 하나요?**

**답변:** Lync 사용자와 연결하고자 하는 모든 Skype 사용자는 Skype ID와 연결된 Microsoft 계정이 있어야 하며 Microsoft 계정을 사용하여 로그인해야 합니다. 이는 Skype 클라이언트에서 사용할 수 있습니다.

**질문: Windows Live와의 페더레이션을 계속 사용할 수 있나요?**

**답변:** 2012년 10월부터 Microsoft는 Windows Live Messenger(WLM) 사용자에게 WLM 서비스가 종료될 예정이고 Skype로 이동할 것을 알렸습니다. Lync는 WLM 서비스가 제공될 때까지 WLM과 Lync 간 페더레이션을 지원합니다. 하지만 추가적인 Windows Live 도메인 활성화는 허용되지 않습니다. WLM 사용자 전환은 Mac 및 Windows Skype 6.0(2012년 10월 25일 출시)부터 가능하며, 이 버전부터 Microsoft 계정(WLM과 동일한 자격 증명)을 사용한 로그인이 가능합니다. Skype에 로그인하면 WLM의 친구 목록은 자동으로 Skype에 추가되며, 유선, 휴대폰, 화면 공유, 그룹 비디오 통화, 다양한 장치 지원 등 Skype의 확장된 통신 기능을 사용할 수 있습니다. 아울러, WLM 사용자의 페더레이션된 Lync 대화 상대가 나머지 친구 목록과 함께 Skype로 전환되면 해당 대화 상대 간 Skype 및 Lync 간 메신저 대화를 즉시 사용할 수 있습니다. Lync 고객이 서비스를 계속 사용하기 위해 해야 할 일은 없습니다.

**질문: Yahoo\! 또는 AOL과의 페더레이션을 계속 사용할 수 있나요?**

**답변:** Lync 및 Office Communications Server 고객을 대상으로 한 Yahoo\! 및 AOL과의 페더레이션은 종료될 예정입니다. 이 서비스에 대한 Microsoft의 지원 가능 여부는 현재 Yahoo\! 및 AOL의 지원 여부에 따라 달라지며, 이 계약은 곧 종료될 예정입니다. Yahoo\! 및 AOL 서비스 모두 2014년 6월까지 지속될 예정입니다. 

  - Yahoo - 서비스가 2014년 6월까지 지속되며 고객은 이전과 마찬가지로 Microsoft Lync 공용 메신저 연결 사용자 구독 라이선스("PIC USL")를 사용해 사용 허가를 받아야 합니다.  2012년 9월 1일을 기준으로 신규 계약이나 갱신 계약의 경우 PIC USL이 더 이상 제공되지 않습니다.  이 날짜 전에 라이선스를 구입한 고객은 서비스 종료 또는 라이선스 만료 중 더 빠른 날짜까지 Yahoo\!와의 페더레이션을 계속할 수 있습니다.  라이선스 계약이 2014년 6월 30일을 지나서도 유효한 고객에게는 2014년 6월 30일부터 해당되는 기간에 상응하는 금액을 계산해 크레딧을 지급해 드립니다.

  - AOL - 2014년 6월 30일에 Lync의 메신저 연결("PIC") 서비스 제공이 중단됩니다. 서비스가 종료될 때 고객의 불편을 최소화하기 위해 Microsoft는 추가 고객 도메인의 프로비저닝을 중단했습니다. 2014년 6월 30일까지 고객은 AIM과의 페더레이션된 통신을 계속해서 지원하기 위해 아무것도 하지 않아도 됩니다. 이 날짜 이후(또는 그 사이에 추가 도메인을 프로비저닝하려는 고객의 경우)에는 AOL에서 직접 대체 서비스를 제공합니다. AOL의 새로운 서비스에 대한 자세한 내용은 <http://aimenterprise.aol.com/pic.php>(영문, AOL.com에서 새 페이지가 열림)를 참고하세요.

**질문: Lync 구매 전에 Skype 연결을 평가해 볼 수 있나요?**

**답변:** Skype 연결은 평가판에서는 제공되지 않습니다. 적격 라이선스를 보유한 Lync 고객은 평가판 대신 서비스에 등록하여 테스트할 수 있습니다.

**질문: 프로비저닝에는 어떤 정보가 필요한가요?**

**답변:** 적격 라이선스별 프로비저닝 요청을 제출하려면 다음 사항이 필요합니다.

  - Microsoft 계약 번호:
    
      - Microsoft 볼륨 라이선싱 지원: Microsoft 볼륨 라이선싱 계약 번호
    
      - Microsoft 파트너 네트워크: 본사 파트너 ID
    
      - 서비스 공급자 라이선싱 계약: 최초 등록 번호
    
      - 고용량 서비스: 제품 등록 번호

  - 액세스 에지 서비스용 정규화된 도메인 이름(FQDN)
    
      - 하나 이상의 액세스 에지 서비스에 대한 FQDN이 필요합니다.
    
      - 조직에서 하나 이상의 서버에서 액세스 에지 서비스를 실행하는 경우 추가 액세스 에지 서비스마다 FQDN을 지정해야 합니다. 중요: 액세스 에지 서비스에 대해 이전에 지정한 FQDN을 변경하는 경우, 변경 사항에 대한 프로비저닝이 완료되는 데 수일이 소요될 수 있으며 서비스 중단으로 이어질 수 있습니다. 서비스 중단을 방지하려면 액세스 에지 서비스에 대해 이전에 지정한 FQDN을 유지하는 것이 좋습니다.

  - SIP(Session Initiation Protocol) 도메인. 사용자가 현재 메신저에 사용하는 SIP URI의 도메인 접미사입니다. 조직에 하나 이상의 SIP 도메인이 있는 경우, 메신저에 사용된 각 도메인에 대한 접미사를 지정해야 합니다. 예를 들어 user1@contoso.com의 경우 contoso.com을 SIP 도메인으로 지정하고, user1@example.fabrikam.com의 경우 example.fabrikam.com을 SIP 도메인으로 지정합니다.
    

    > [!NOTE]
    > SIP 도메인의 도메인 접미사만 지정합니다. 액세스 에지 서비스의 FQDN을 포함하여 SIP 도메인의 FQDN은 지정하지 않습니다.



  - 연락처 정보. 지정한 각 SIP 도메인 관리자의 전자 메일 주소를 지정합니다.

**질문: 분할 도메인 시나리오에서 Lync-Skype 연결은 어떻게 설정하나요?**

**답변:**Lync Online 2013 및 Lync Server 온-프레미스 분할 시나리오(온라인 및 온-프레미스 사용자 모두 동일한 SIP 도메인 사용)의 경우, 다음 두 단계를 다음 순서대로 수행하여 Lync-Skype 연결을 설정합니다.

1.  PIC 프로비저닝 가이드에 설명된 대로 온-프레미스 Lync-Skype 연결을 설정합니다.

2.  도메인이 프로비저닝되었음을 알리는 Microsoft의 확인 메시지가 나타날 때까지 기다립니다.

3.  확인 메시지가 표시되면 Lync 관리 센터를 사용하여 "외부 통신"을 설정합니다. 자세한 내용은 [http://office.microsoft.com/ko-kr/support/configure-external-communications-HA102817865.aspx?CTT=5\&origin=HA102817356](http://office.microsoft.com/ko-kr/support/configure-external-communications-ha102817865.aspx?ctt=5%26origin=ha102817356)를 확인하세요.

이 순서는 중요합니다.  Lync Online의 통신을 사용하기 전에 온-프레미스 연결을 설정해야 합니다. 순서가 바뀌면 <https://pic.lync.com>에 입력한 온-프레미스 정보가 처리되지 않습니다. 이 도메인을 사용하여 외부 통신용 Lync Online을 이미 설정한 경우, 설정을 해제하고 24시간 후에 다시 시작해야 합니다. 먼저 온-프레미스 정보를 <https://pic.lync.com>에 입력한 다음 Lync Online용 외부 통신을 설정하면 됩니다.

**질문: Skype 연결에 대해 여러 개의 액세스 에지 서비스 FQDN을 프로비저닝할 수 있나요?**

**답변:** 각 프로비저닝 요청에 대해 액세스 에지 서비스 FQDN을 10개까지 프로비저닝할 수 있습니다.

**질문: 프로비저닝을 요청한 조직의 Microsoft 계정 전자 메일 주소 목록을 얻을 수 있나요?**

**답변:** 아니요. 이 주소는 개인 식별 정보로 간주되며, 공유되지 않습니다.

**질문: Windows Live에서 지원하지 않는 도메인이 포함된 ID를 가진 Windows Live Messenger 대화 상대는 어떻게 추가하나요?**

**답변:** 비 Windows Live 도메인을 사용하는 계정 또는 ID를 가진 Windows Live Messenger 사용자를 추가하는 경우, \<사용자 이름\>(\<도메인 이름\>)@msn.com과 같은 형식으로 주소를 입력합니다. 여기서 \<도메인 이름\>은 사용자 전자 메일 주소의 도메인 이름입니다. 예를 들어 ted@contoso.com을 추가하려면 ted(contoso.com)@msn.com과 같은 형식을 사용합니다. Windows Live에 등록된 도메인 목록을 보려면 http://support.microsoft.com/?kbid=897567에서 "Live Communications Server 서비스 팩 1 설치 후 공용 메신저에서 발생하는 알려진 문제"의 지원되는 도메인 섹션을 확인하세요.

**질문: 프로비저닝 프로세스는 어느 정도 소요되나요?**

**답변:** 프로비저닝은 최대 30일이 소요됩니다.

**질문: 프로비저닝 완료 시기를 어떻게 알 수 있나요?**

**답변:** 프로비저닝이 완료되면 Microsoft에서 전자 메일 알림을 발송합니다.

**질문: 제출한 구성 또는 연락처 정보는 어떻게 업데이트하나요?**

**답변:** 프로비저닝이 완료되면 프로비저닝 요청 시 사용한 동일 웹 사이트에서 정보를 업데이트할 수 있습니다. 계약 번호를 입력하고 \[업데이트 서비스\]를 클릭하세요.

