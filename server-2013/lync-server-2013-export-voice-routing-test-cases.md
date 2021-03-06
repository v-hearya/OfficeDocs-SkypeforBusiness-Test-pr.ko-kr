﻿---
title: 'Lync Server 2013: 음성 라우팅 테스트 사례 내보내기'
TOCTitle: 음성 라우팅 테스트 사례 내보내기
ms:assetid: 489ac472-1a35-4755-b390-48f7cdf31e94
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg425957(v=OCS.15)
ms:contentKeyID: 49303519
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013에서 음성 라우팅 테스트 사례 내보내기

 

_**마지막으로 수정된 항목:** 2012-11-01_

테스트 사례를 사용하면 조직에서 음성 경로를 테스트할 수 있습니다. 다이얼할 번호 및 적용할 다이얼 플랜과 음성 정책 등으로 테스트 사례를 정의하면 Lync Server에서 특정 조건에 따라 제공된 번호가 PSTN 네트워크로 성공적으로 라우팅되는지 확인할 수 있습니다.

Lync Server 제어판을 사용해서 만들 수 있는 테스트 사례는 일반적으로 원래 테스트 사례가 만들어졌고 실행되는 서버에만 저장됩니다. 하지만 이러한 테스트 사례를 XML 파일(.vtest 확장명)로 내보내고 다른 서버에서 가져올 수 있습니다. 이러한 방식을 통해 토폴로지의 여러 지점에 있는 서로 다른 컴퓨터에서 동일한 테스트를 실행할 수 있습니다.

## 음성 라우팅 테스트 사례를 내보내려면

1.  Lync Server 제어판에서 **음성 라우팅** 을 클릭한 후 **테스트 음성 라우팅** 을 클릭합니다.

2.  **음성 라우팅 테스트** 탭에서 내보낼 테스트 사례를 선택합니다. 여러 테스트 사례를 선택하려면 내보낼 첫 번째 테스트 사례를 클릭한 후 Ctrl 키를 누른 상태로 내보낼 다른 테스트 사례를 계속 선택합니다.

3.  **동작** 에서 **테스트 사례 내보내기** 를 클릭합니다.

4.  **다른 이름으로 저장** 대화 상자에서 내보낸 테스트 사례를 저장할 폴더를 선택하고 **파일 이름** 상자에 결과 XML 파일의 이름을 입력합니다. 여러 테스트 사례를 내보낼 경우 모든 테스트 사례가 단일 XML 파일로 저장됩니다.

5.  테스트 사례를 저장하려면 **저장** 을 클릭합니다.

## 참고 항목

#### 작업

[Lync Server 2013에서 음성 라우팅 테스트 사례 가져오기](lync-server-2013-import-voice-routing-test-cases.md)

