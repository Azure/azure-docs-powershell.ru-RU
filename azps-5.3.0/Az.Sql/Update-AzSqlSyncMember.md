---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506605"
---
# <span data-ttu-id="90391-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90391-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="90391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90391-102">SYNOPSIS</span></span>
<span data-ttu-id="90391-103">Обновляет участник синхронизации базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="90391-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="90391-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90391-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90391-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90391-105">DESCRIPTION</span></span>
<span data-ttu-id="90391-106">Командалет **Update-AzSqlSyncGroup** изменяет свойства члена синхронизации базы данных Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="90391-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="90391-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90391-107">EXAMPLES</span></span>

### <span data-ttu-id="90391-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90391-108">Example 1</span></span>
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

<span data-ttu-id="90391-109">Эта команда сбрасывает пароль администратора для базы данных.</span><span class="sxs-lookup"><span data-stu-id="90391-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="90391-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90391-110">PARAMETERS</span></span>

### <span data-ttu-id="90391-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90391-111">-DatabaseName</span></span>
<span data-ttu-id="90391-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="90391-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="90391-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90391-113">-DefaultProfile</span></span>
<span data-ttu-id="90391-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="90391-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90391-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="90391-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="90391-116">Учетные данные (имя пользователя и пароль) базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="90391-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90391-117">-Name</span><span class="sxs-lookup"><span data-stu-id="90391-117">-Name</span></span>
<span data-ttu-id="90391-118">Имя участника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="90391-118">The sync member name.</span></span>

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

### <span data-ttu-id="90391-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90391-119">-ResourceGroupName</span></span>
<span data-ttu-id="90391-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90391-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="90391-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90391-121">-ServerName</span></span>
<span data-ttu-id="90391-122">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90391-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="90391-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="90391-123">-SyncGroupName</span></span>
<span data-ttu-id="90391-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="90391-124">The sync group name.</span></span>

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

### <span data-ttu-id="90391-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="90391-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="90391-126">ИД ресурса для базы данных участника синхронизации, который используется, если для usePrivateLinkConnection установлено true.</span><span class="sxs-lookup"><span data-stu-id="90391-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90391-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="90391-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="90391-128">Следует ли использовать ли личную ссылку при подключении к этому участнику синхронизации.</span><span class="sxs-lookup"><span data-stu-id="90391-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90391-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90391-129">-Confirm</span></span>
<span data-ttu-id="90391-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="90391-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90391-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90391-131">-WhatIf</span></span>
<span data-ttu-id="90391-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90391-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90391-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="90391-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90391-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90391-134">CommonParameters</span></span>
<span data-ttu-id="90391-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90391-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90391-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90391-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90391-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90391-137">INPUTS</span></span>

### <span data-ttu-id="90391-138">System.String</span><span class="sxs-lookup"><span data-stu-id="90391-138">System.String</span></span>

## <span data-ttu-id="90391-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90391-139">OUTPUTS</span></span>

### <span data-ttu-id="90391-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="90391-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="90391-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90391-141">NOTES</span></span>

## <span data-ttu-id="90391-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90391-142">RELATED LINKS</span></span>

[<span data-ttu-id="90391-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90391-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="90391-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90391-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="90391-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90391-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

