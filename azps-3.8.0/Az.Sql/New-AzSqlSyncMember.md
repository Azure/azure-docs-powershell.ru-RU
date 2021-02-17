---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 793962db73fd053764a794b64bea8e68edadd73b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413257"
---
# <span data-ttu-id="e48bb-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e48bb-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="e48bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e48bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e48bb-103">Создает участник синхронизации базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e48bb-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e48bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e48bb-104">SYNTAX</span></span>

### <span data-ttu-id="e48bb-105">AzureSqlDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e48bb-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e48bb-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="e48bb-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e48bb-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="e48bb-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e48bb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e48bb-108">DESCRIPTION</span></span>
<span data-ttu-id="e48bb-109">Для этого создается член синхронизации базы данных Azure SQL **AzSqlSyncMember.**</span><span class="sxs-lookup"><span data-stu-id="e48bb-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e48bb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e48bb-110">EXAMPLES</span></span>

### <span data-ttu-id="e48bb-111">Пример 1. Создание участника синхронизации для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e48bb-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="e48bb-112">Эта команда создает участник синхронизации для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e48bb-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="e48bb-113">Пример 2. Создание участника синхронизации для локальной базы SQL Server</span><span class="sxs-lookup"><span data-stu-id="e48bb-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="e48bb-114">Эта команда создает участник синхронизации для локальной SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="e48bb-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="e48bb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e48bb-115">PARAMETERS</span></span>

### <span data-ttu-id="e48bb-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e48bb-116">-DatabaseName</span></span>
<span data-ttu-id="e48bb-117">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e48bb-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e48bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48bb-118">-DefaultProfile</span></span>
<span data-ttu-id="e48bb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e48bb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e48bb-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e48bb-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="e48bb-121">Учетные данные (имя пользователя и пароль) базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e48bb-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e48bb-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e48bb-122">-MemberDatabaseName</span></span>
<span data-ttu-id="e48bb-123">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e48bb-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="e48bb-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="e48bb-124">-MemberDatabaseType</span></span>
<span data-ttu-id="e48bb-125">Тип базы данных базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="e48bb-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="e48bb-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="e48bb-126">-MemberServerName</span></span>
<span data-ttu-id="e48bb-127">Azure SQL Server имя базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="e48bb-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="e48bb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e48bb-128">-Name</span></span>
<span data-ttu-id="e48bb-129">Имя участника синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-129">The sync member name.</span></span>

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

### <span data-ttu-id="e48bb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e48bb-130">-ResourceGroupName</span></span>
<span data-ttu-id="e48bb-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e48bb-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="e48bb-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e48bb-132">-ServerName</span></span>
<span data-ttu-id="e48bb-133">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e48bb-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e48bb-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="e48bb-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="e48bb-135">Id базы SQL сервера, подключенной агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="e48bb-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="e48bb-136">-SyncAgentName</span></span>
<span data-ttu-id="e48bb-137">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="e48bb-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e48bb-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="e48bb-139">Имя группы ресурсов, в которой находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="e48bb-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="e48bb-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="e48bb-141">ИД ресурса агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="e48bb-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="e48bb-142">-SyncAgentServerName</span></span>
<span data-ttu-id="e48bb-143">Имя azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="e48bb-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="e48bb-144">-SyncDirection</span></span>
<span data-ttu-id="e48bb-145">Направление синхронизации этого члена синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="e48bb-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e48bb-146">-SyncGroupName</span></span>
<span data-ttu-id="e48bb-147">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e48bb-147">The sync group name.</span></span>

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

### <span data-ttu-id="e48bb-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e48bb-148">-Confirm</span></span>
<span data-ttu-id="e48bb-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e48bb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e48bb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e48bb-150">-WhatIf</span></span>
<span data-ttu-id="e48bb-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e48bb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e48bb-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e48bb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e48bb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48bb-153">CommonParameters</span></span>
<span data-ttu-id="e48bb-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e48bb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48bb-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e48bb-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48bb-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e48bb-156">INPUTS</span></span>

### <span data-ttu-id="e48bb-157">System.String</span><span class="sxs-lookup"><span data-stu-id="e48bb-157">System.String</span></span>

## <span data-ttu-id="e48bb-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e48bb-158">OUTPUTS</span></span>

### <span data-ttu-id="e48bb-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e48bb-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e48bb-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e48bb-160">NOTES</span></span>

## <span data-ttu-id="e48bb-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e48bb-161">RELATED LINKS</span></span>

[<span data-ttu-id="e48bb-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e48bb-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


[<span data-ttu-id="e48bb-163">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e48bb-163">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

