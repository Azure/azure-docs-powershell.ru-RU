---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912443"
---
# <span data-ttu-id="7924e-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7924e-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="7924e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7924e-102">SYNOPSIS</span></span>
<span data-ttu-id="7924e-103">Обновляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7924e-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="7924e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7924e-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7924e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7924e-105">DESCRIPTION</span></span>
<span data-ttu-id="7924e-106">Командлет **Update-AzSqlSyncGroup** изменяет свойства члена синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7924e-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="7924e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7924e-107">EXAMPLES</span></span>

### <span data-ttu-id="7924e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7924e-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="7924e-109">Эта команда сбрасывает пароль администратора для базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="7924e-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="7924e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7924e-110">PARAMETERS</span></span>

### <span data-ttu-id="7924e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7924e-111">-DatabaseName</span></span>
<span data-ttu-id="7924e-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7924e-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7924e-113">-DefaultProfile</span></span>
<span data-ttu-id="7924e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7924e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="7924e-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="7924e-116">Учетные данные (имя пользователя и пароль) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7924e-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7924e-117">-Name</span></span>
<span data-ttu-id="7924e-118">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7924e-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7924e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7924e-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7924e-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7924e-121">-ServerName</span></span>
<span data-ttu-id="7924e-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7924e-122">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7924e-123">-SyncGroupName</span></span>
<span data-ttu-id="7924e-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7924e-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7924e-125">-Confirm</span></span>
<span data-ttu-id="7924e-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7924e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7924e-127">-WhatIf</span></span>
<span data-ttu-id="7924e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7924e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7924e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7924e-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7924e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7924e-130">CommonParameters</span></span>
<span data-ttu-id="7924e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7924e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7924e-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7924e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7924e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7924e-133">INPUTS</span></span>

### <span data-ttu-id="7924e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7924e-134">System.String</span></span>

## <span data-ttu-id="7924e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7924e-135">OUTPUTS</span></span>

### <span data-ttu-id="7924e-136">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="7924e-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="7924e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7924e-137">NOTES</span></span>

## <span data-ttu-id="7924e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7924e-138">RELATED LINKS</span></span>

[<span data-ttu-id="7924e-139">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7924e-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="7924e-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7924e-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="7924e-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="7924e-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

