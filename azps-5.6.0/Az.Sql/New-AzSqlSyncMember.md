---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: c26cb74f1d9f9c30e63bb39ec7668216a5f3a297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961427"
---
# <span data-ttu-id="940e6-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="940e6-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="940e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="940e6-102">SYNOPSIS</span></span>
<span data-ttu-id="940e6-103">Создает участник синхронизации базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="940e6-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="940e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="940e6-104">SYNTAX</span></span>

### <span data-ttu-id="940e6-105">AzureSqlDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="940e6-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="940e6-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="940e6-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="940e6-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="940e6-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="940e6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="940e6-108">DESCRIPTION</span></span>
<span data-ttu-id="940e6-109">Для этого создается член синхронизации базы данных Azure SQL **AzSqlSyncMember.**</span><span class="sxs-lookup"><span data-stu-id="940e6-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="940e6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="940e6-110">EXAMPLES</span></span>

### <span data-ttu-id="940e6-111">Пример 1. Создание участника синхронизации для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="940e6-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="940e6-112">Эта команда создает участник синхронизации для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="940e6-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="940e6-113">Пример 2. Создание участника синхронизации для локальной базы SQL Server</span><span class="sxs-lookup"><span data-stu-id="940e6-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="940e6-114">Эта команда создает участник синхронизации для локальной SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="940e6-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="940e6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="940e6-115">PARAMETERS</span></span>

### <span data-ttu-id="940e6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="940e6-116">-DatabaseName</span></span>
<span data-ttu-id="940e6-117">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="940e6-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="940e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940e6-118">-DefaultProfile</span></span>
<span data-ttu-id="940e6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="940e6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="940e6-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="940e6-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="940e6-121">Учетные данные (имя пользователя и пароль) базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="940e6-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="940e6-122">-MemberDatabaseName</span></span>
<span data-ttu-id="940e6-123">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="940e6-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="940e6-124">-MemberDatabaseType</span></span>
<span data-ttu-id="940e6-125">Тип базы данных базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="940e6-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="940e6-126">-MemberServerName</span></span>
<span data-ttu-id="940e6-127">Azure SQL Server имя базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="940e6-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="940e6-128">-Name</span></span>
<span data-ttu-id="940e6-129">Имя участника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-129">The sync member name.</span></span>

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

### <span data-ttu-id="940e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="940e6-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="940e6-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="940e6-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="940e6-132">-ServerName</span></span>
<span data-ttu-id="940e6-133">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="940e6-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="940e6-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="940e6-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="940e6-135">Id базы SQL сервера, подключенной агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="940e6-136">-SyncAgentName</span></span>
<span data-ttu-id="940e6-137">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940e6-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="940e6-139">Имя группы ресурсов, в которой находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="940e6-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="940e6-141">ИД ресурса агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="940e6-142">-SyncAgentServerName</span></span>
<span data-ttu-id="940e6-143">Имя azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="940e6-144">-SyncDirection</span></span>
<span data-ttu-id="940e6-145">Направление синхронизации этого члена синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="940e6-146">-SyncGroupName</span></span>
<span data-ttu-id="940e6-147">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-147">The sync group name.</span></span>

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

### <span data-ttu-id="940e6-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="940e6-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="940e6-149">ИД ресурса для базы данных участника синхронизации, который используется, если для usePrivateLinkConnection установлено true.</span><span class="sxs-lookup"><span data-stu-id="940e6-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="940e6-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="940e6-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="940e6-151">Используйте личную связь при подключении к этому участнику синхронизации.</span><span class="sxs-lookup"><span data-stu-id="940e6-151">Use a private link connection when connecting to this sync member.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940e6-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="940e6-152">-Confirm</span></span>
<span data-ttu-id="940e6-153">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="940e6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="940e6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="940e6-154">-WhatIf</span></span>
<span data-ttu-id="940e6-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="940e6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="940e6-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="940e6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="940e6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940e6-157">CommonParameters</span></span>
<span data-ttu-id="940e6-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940e6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940e6-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="940e6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940e6-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="940e6-160">INPUTS</span></span>

### <span data-ttu-id="940e6-161">System.String</span><span class="sxs-lookup"><span data-stu-id="940e6-161">System.String</span></span>

## <span data-ttu-id="940e6-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="940e6-162">OUTPUTS</span></span>

### <span data-ttu-id="940e6-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="940e6-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="940e6-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="940e6-164">NOTES</span></span>

## <span data-ttu-id="940e6-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="940e6-165">RELATED LINKS</span></span>

[<span data-ttu-id="940e6-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="940e6-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="940e6-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="940e6-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="940e6-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="940e6-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

