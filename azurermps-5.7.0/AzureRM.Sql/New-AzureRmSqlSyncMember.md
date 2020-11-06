---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: d2df78cc4cbf7bea7918653e310193bf013d7495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566058"
---
# <span data-ttu-id="3f4d2-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3f4d2-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="3f4d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4d2-103">Создает элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f4d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f4d2-104">SYNTAX</span></span>

### <span data-ttu-id="3f4d2-105">AzureSqlDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f4d2-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4d2-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="3f4d2-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4d2-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="3f4d2-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4d2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f4d2-108">DESCRIPTION</span></span>
<span data-ttu-id="3f4d2-109">Командлет **New-AzureRmSqlSyncMember** создает член синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="3f4d2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f4d2-110">EXAMPLES</span></span>

### <span data-ttu-id="3f4d2-111">Пример 1: создание элемента синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="3f4d2-112">Эта команда создает участника синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="3f4d2-113">Пример 2: создание члена синхронизации для локальной базы данных SQL Server</span><span class="sxs-lookup"><span data-stu-id="3f4d2-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="3f4d2-114">Эта команда создает элемент синхронизации для локальной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="3f4d2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f4d2-115">PARAMETERS</span></span>

### <span data-ttu-id="3f4d2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-116">-DatabaseName</span></span>
<span data-ttu-id="3f4d2-117">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4d2-118">-DefaultProfile</span></span>
<span data-ttu-id="3f4d2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3f4d2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="3f4d2-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="3f4d2-121">Учетные данные (имя пользователя и пароль) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-122">-MemberDatabaseName</span></span>
<span data-ttu-id="3f4d2-123">Имя базы данных Azure SQL для базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="3f4d2-124">-MemberDatabaseType</span></span>
<span data-ttu-id="3f4d2-125">Тип базы данных участника.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-125">The database type of the member database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-126">-MemberServerName</span></span>
<span data-ttu-id="3f4d2-127">Имя сервера Azure SQL Server для базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f4d2-128">-Name</span></span>
<span data-ttu-id="3f4d2-129">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-129">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-130">-ResourceGroupName</span></span>
<span data-ttu-id="3f4d2-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-132">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3f4d2-132">-ServerName</span></span>
<span data-ttu-id="3f4d2-133">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="3f4d2-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="3f4d2-135">Идентификатор базы данных SQL Server, связанной с агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-136">-SyncAgentName</span></span>
<span data-ttu-id="3f4d2-137">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-137">The name of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="3f4d2-139">Имя группы ресурсов, в которой находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="3f4d2-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="3f4d2-141">Идентификатор ресурса агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-141">The resource ID of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-142">-SyncAgentServerName</span></span>
<span data-ttu-id="3f4d2-143">Имя сервера Azure SQL Server, на котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="3f4d2-144">-SyncDirection</span></span>
<span data-ttu-id="3f4d2-145">Направление синхронизации для этого элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-145">The sync direction of this sync member.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4d2-146">-SyncGroupName</span></span>
<span data-ttu-id="3f4d2-147">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-147">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f4d2-148">-Confirm</span></span>
<span data-ttu-id="3f4d2-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4d2-150">-WhatIf</span></span>
<span data-ttu-id="3f4d2-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4d2-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4d2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4d2-153">CommonParameters</span></span>
<span data-ttu-id="3f4d2-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4d2-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4d2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4d2-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f4d2-156">INPUTS</span></span>

### <span data-ttu-id="3f4d2-157">Ничего</span><span class="sxs-lookup"><span data-stu-id="3f4d2-157">None</span></span>
<span data-ttu-id="3f4d2-158">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3f4d2-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f4d2-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f4d2-159">OUTPUTS</span></span>

### <span data-ttu-id="3f4d2-160">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="3f4d2-160">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="3f4d2-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f4d2-161">NOTES</span></span>

## <span data-ttu-id="3f4d2-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f4d2-162">RELATED LINKS</span></span>

[<span data-ttu-id="3f4d2-163">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3f4d2-163">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="3f4d2-164">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3f4d2-164">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="3f4d2-165">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="3f4d2-165">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

