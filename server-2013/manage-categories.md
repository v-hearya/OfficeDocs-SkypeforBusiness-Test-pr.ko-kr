﻿---
title: 범주 관리
TOCTitle: 범주 관리
ms:assetid: 1b118d91-b4c4-4b2f-b842-b451417ec2c6
ms:mtpsurl: https://technet.microsoft.com/ko-kr/library/JJ204719(v=OCS.15)
ms:contentKeyID: 49302962
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 범주 관리

 

_**마지막으로 수정된 항목:** 2012-10-06_

새 영구 채팅 서버 범주를 만들려면

    New-CsPersistentChatCategory -Name Foo -PersistentChatPoolFqdn client.contoso1b118d91-b4c4-4b2f-b842-b451417ec2c6.com [other parameters]


> [!IMPORTANT]
> PersistentChatPoolFqdn은 영구 채팅 서버 풀이 둘 이상인 경우에만 필요합니다.



기존 영구 채팅 서버 범주를 변경하려면

    Set-CsPersistentChatCategory -Identity testCat -AllowedMembers @{Add="sip:user1@contoso.com", "CN=container,DC=contoso,DC=com"}  -DeniedMembers @{Add="sip:user2@contoso.com"}
    Set-CsPersistentChatCategory -Identity testCat -Creators @{Add="sip:user1@contoso.com"}

Windows PowerShell: AllowedMembers, DeniedMembers 및 Creators를 동시에 설정할 수 있습니다. Creators는 AllowedMembers에서 DeniedMembers를 제외한 구성원이어야 합니다. 범주의 속성을 구성원과 작성자로 동시에 설정할 수도 있습니다.

## 범주 작성, 가져오기, 설정 또는 제거

새 범주를 만들려면

    New-CsPersistentChatCategory -Name <String> [-PersistentChatPoolFqdn <String>] [-Description <String>] [-EnableInvitations<Switch Parameter>] [-EnableFileUpload <Switch Parameter>] [-RemoveChatHistory <Switch Parameter>] [-MaxContentSize <Integer>]

범주를 가져오려면

    Get-CsPersistentChatCategory -Identity <String>

또는

    Get-CsPersistentChatCategory -PersistentChatPoolFqdn <String>

범주를 설정하려면

    Set-CsPersistentChatCategory -Instance <CategoryObject> [-WhatIf] [-Confirm] [<CommonParameters>]

또는

    Set-CsPersistentChatCategory [-Identity] <string> [-Name <string>] [-Description <string>] [-Invitations <bool>] [-FileUpload <bool>] [-ChatHistory <bool>] [-AllowedMembers <PSListModifier[string]>] [-DeniedMembers <PSListModifier[string]>] [-Creators <PSListModifier[string]>] [-WhatIf] [-Confirm]  [<CommonParameters>]

범주를 제거하려면

    Remove-CsPersistentChatCategory -Instance <CategoryObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

또는

    Remove-CsPersistentChatCategory -Identity <String> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

