﻿---
title: 'Lync Server 2013: 웹 팜 FQDN 구성'
TOCTitle: 웹 팜 FQDN 구성
ms:assetid: cb25dbbd-dcea-4997-8e14-e5007dd7d3ca
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/Gg429722(v=OCS.15)
ms:contentKeyID: 49305041
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013에 대한 웹 팜 FQDN 구성

 

_**마지막으로 수정된 항목:** 2013-03-29_

토폴로지 작성기에서 Standard Edition 서버, 프런트 엔드 풀, 디렉터 또는 디렉터 풀의 구성을 정의하는 경우 외부 웹 서비스의 FQDN(정규화된 도메인 이름)을 구성해야 합니다. Standard Edition 서버 또는 프런트 엔드 풀에 있는 클라이언트에 로그온하는 과정에서 구성된 웹 서비스 FQDN은 인밴드 구축 방식으로 전송됩니다. 외부 웹 서비스 URL을 추가 또는 변경해야 하는 경우 토폴로지 작성기를 사용하여 이 문서의 절차에 따라 웹 서비스 구성을 구성 또는 재구성할 수 있습니다.

## 웹 서비스에 대해 외부 풀 FQDN을 구성하려면

1.  토폴로지 작성기 시작: **시작**, **모든 프로그램**, **Microsoft Lync Server 2013**을 차례로 클릭한 다음 **Lync Server 토폴로지 작성기**를 클릭합니다.

2.  토폴로지 작성기에서 콘솔 트리의 **Standard Edition 프런트 엔드** , **Enterprise Edition 프런트 엔드** 및 **디렉터** 아래에서 편집해야 할 풀 이름을 두 번 클릭한 다음 **속성 편집** 을 클릭합니다.

3.  **웹 서비스** 섹션에서 **외부 웹 서비스 FQDN** 을 추가하거나 편집합니다.

4.  HTTP 및 HTTPS 모두에 대해 **수신 대기 포트** 를 검토하여 조정합니다. 기본값은 다음과 같습니다.
    
      - **수신 대기 포트:** HTTP 8080, HTTPS 4443
    
      - **게시된 포트:** HTTP 80, HTTPS 443
    
    **수신 대기 포트** 는 역방향 프록시로부터의 요청을 수신하도록 구성된 외부 웹 서비스의 포트이며, **게시된 포트** 는 역방향 프록시에 의해 외부적으로 게시되어 인밴드 구축 동안 클라이언트와 통신하는 포트입니다.

5.  추가 및 업데이트 작업을 완료했으면 **확인** 을 클릭하여 계속 진행합니다.

6.  **Lync Server 2013**을 마우스 오른쪽 단추로 클릭한 다음 **게시** 를 클릭합니다.
    

    > [!IMPORTANT]
    > 게시가 성공적으로 완료되면 추가적으로 진행해야 할 단계가 있음을 알려주는 링크가 나타날 수 있습니다. 링크를 클릭하면 토폴로지 작성기에서 변경한 내용의 영향을 받는 서버 목록이 열리고 나열된 각 서버에서 Lync Server 배포 마법사를 다시 실행하여 추가/제가/변경된 구성 요소의 구성을 업데이트해야 합니다.



7.  조직의 각 Standard Edition 서버, 프런트 엔드 풀, 디렉터 또는 디렉터 풀에 대해 이 단계를 반복합니다.

