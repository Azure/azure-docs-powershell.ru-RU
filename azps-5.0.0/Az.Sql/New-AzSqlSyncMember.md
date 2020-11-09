---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: f7fc860711c5037e6ce6390f9fb7d79ddfa7d6ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246650"
---
# <span data-ttu-id="dc13b-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dc13b-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="dc13b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc13b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc13b-103">Создает элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc13b-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="dc13b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc13b-104">SYNTAX</span></span>

### <span data-ttu-id="dc13b-105">AzureSqlDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc13b-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc13b-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="dc13b-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc13b-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="dc13b-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc13b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc13b-108">DESCRIPTION</span></span>
<span data-ttu-id="dc13b-109">Командлет **New-AzSqlSyncMember** создает член синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc13b-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="dc13b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc13b-110">EXAMPLES</span></span>

### <span data-ttu-id="dc13b-111">Пример 1: создание элемента синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc13b-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="dc13b-112">Эта команда создает участника синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc13b-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="dc13b-113">Пример 2: создание члена синхронизации для локальной базы данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="dc13b-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="dc13b-114">Эта команда создает элемент синхронизации для локальной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="dc13b-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="dc13b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc13b-115">PARAMETERS</span></span>

### <span data-ttu-id="dc13b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc13b-116">-DatabaseName</span></span>
<span data-ttu-id="dc13b-117">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc13b-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="dc13b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc13b-118">-DefaultProfile</span></span>
<span data-ttu-id="dc13b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dc13b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc13b-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="dc13b-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="dc13b-121">Учетные данные (имя пользователя и пароль) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc13b-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="dc13b-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc13b-122">-MemberDatabaseName</span></span>
<span data-ttu-id="dc13b-123">Имя базы данных Azure SQL для базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="dc13b-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="dc13b-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="dc13b-124">-MemberDatabaseType</span></span>
<span data-ttu-id="dc13b-125">Тип базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="dc13b-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="dc13b-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="dc13b-126">-MemberServerName</span></span>
<span data-ttu-id="dc13b-127">Имя сервера Azure SQL Server для базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="dc13b-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="dc13b-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc13b-128">-Name</span></span>
<span data-ttu-id="dc13b-129">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-129">The sync member name.</span></span>

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

### <span data-ttu-id="dc13b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc13b-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc13b-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc13b-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc13b-132">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="dc13b-132">-ServerName</span></span>
<span data-ttu-id="dc13b-133">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc13b-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="dc13b-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="dc13b-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="dc13b-135">Идентификатор базы данных SQL Server, связанной с агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="dc13b-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="dc13b-136">-SyncAgentName</span></span>
<span data-ttu-id="dc13b-137">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="dc13b-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc13b-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="dc13b-139">Имя группы ресурсов, в которой находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="dc13b-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="dc13b-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="dc13b-141">Идентификатор ресурса агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="dc13b-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="dc13b-142">-SyncAgentServerName</span></span>
<span data-ttu-id="dc13b-143">Имя сервера Azure SQL Server, на котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="dc13b-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="dc13b-144">-SyncDirection</span></span>
<span data-ttu-id="dc13b-145">Направление синхронизации для этого элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="dc13b-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="dc13b-146">-SyncGroupName</span></span>
<span data-ttu-id="dc13b-147">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-147">The sync group name.</span></span>

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

### <span data-ttu-id="dc13b-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="dc13b-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="dc13b-149">Идентификатор ресурса для базы данных элемента синхронизации, который используется, если UsePrivateLinkConnection имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="dc13b-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="dc13b-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="dc13b-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="dc13b-151">Используйте подключение к частной ссылке при подключении к этому члену синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc13b-151">Use a private link connection when connecting to this sync member.</span></span>

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

### <span data-ttu-id="dc13b-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc13b-152">-Confirm</span></span>
<span data-ttu-id="dc13b-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc13b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc13b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc13b-154">-WhatIf</span></span>
<span data-ttu-id="dc13b-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc13b-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc13b-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc13b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc13b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc13b-157">CommonParameters</span></span>
<span data-ttu-id="dc13b-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc13b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc13b-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc13b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc13b-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc13b-160">INPUTS</span></span>

### <span data-ttu-id="dc13b-161">System. String</span><span class="sxs-lookup"><span data-stu-id="dc13b-161">System.String</span></span>

## <span data-ttu-id="dc13b-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc13b-162">OUTPUTS</span></span>

### <span data-ttu-id="dc13b-163">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="dc13b-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="dc13b-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc13b-164">NOTES</span></span>

## <span data-ttu-id="dc13b-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc13b-165">RELATED LINKS</span></span>

[<span data-ttu-id="dc13b-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dc13b-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="dc13b-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dc13b-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="dc13b-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="dc13b-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)
