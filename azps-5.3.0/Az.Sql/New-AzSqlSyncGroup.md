---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505890"
---
# <span data-ttu-id="c5a7f-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c5a7f-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="c5a7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a7f-103">Создает группу синхронизации SQL баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="c5a7f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5a7f-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5a7f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5a7f-105">DESCRIPTION</span></span>
<span data-ttu-id="c5a7f-106">Для этого создается группа синхронизации базы данных Azure SQL **AzSqlSyncGroup.**</span><span class="sxs-lookup"><span data-stu-id="c5a7f-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="c5a7f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5a7f-107">EXAMPLES</span></span>

### <span data-ttu-id="c5a7f-108">Пример 1. Создание группы синхронизации для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="c5a7f-109">Эта команда создает группу синхронизации для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="c5a7f-110">"schema.js" — это файл на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="c5a7f-111">Она содержит гругрузку схемы в формате json.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="c5a7f-112">Пример схемы json: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Столбцы": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="c5a7f-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="c5a7f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5a7f-113">PARAMETERS</span></span>

### <span data-ttu-id="c5a7f-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="c5a7f-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="c5a7f-115">Политика устранения конфликтов между центром и базой данных членов в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a7f-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="c5a7f-116">-DatabaseCredential</span></span>
<span data-ttu-id="c5a7f-117">Учетные SQL проверки подлинности центральной базы данных.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="c5a7f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c5a7f-118">-DatabaseName</span></span>
<span data-ttu-id="c5a7f-119">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c5a7f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a7f-120">-DefaultProfile</span></span>
<span data-ttu-id="c5a7f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5a7f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5a7f-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c5a7f-122">-IntervalInSeconds</span></span>
<span data-ttu-id="c5a7f-123">Частота (в секундах) синхронизации данных.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="c5a7f-124">Значение по умолчанию — -1, то есть автоматическая синхронизация не включена.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a7f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c5a7f-125">-Name</span></span>
<span data-ttu-id="c5a7f-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5a7f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a7f-127">-ResourceGroupName</span></span>
<span data-ttu-id="c5a7f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5a7f-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="c5a7f-129">-SchemaFile</span></span>
<span data-ttu-id="c5a7f-130">Путь к файлу схемы.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="c5a7f-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c5a7f-131">-ServerName</span></span>
<span data-ttu-id="c5a7f-132">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c5a7f-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c5a7f-133">-SyncDatabaseName</span></span>
<span data-ttu-id="c5a7f-134">База данных, используемая для синхронизации связанных метаданных.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a7f-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a7f-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="c5a7f-136">Группа ресурсов, к которой относится база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a7f-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="c5a7f-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="c5a7f-138">Сервер, на котором находится база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a7f-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c5a7f-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="c5a7f-140">Используйте личную связь при подключении к центру этой группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="c5a7f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5a7f-141">-Confirm</span></span>
<span data-ttu-id="c5a7f-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5a7f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5a7f-143">-WhatIf</span></span>
<span data-ttu-id="c5a7f-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5a7f-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5a7f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a7f-146">CommonParameters</span></span>
<span data-ttu-id="c5a7f-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5a7f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a7f-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5a7f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a7f-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5a7f-149">INPUTS</span></span>

### <span data-ttu-id="c5a7f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c5a7f-150">System.String</span></span>

## <span data-ttu-id="c5a7f-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5a7f-151">OUTPUTS</span></span>

### <span data-ttu-id="c5a7f-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="c5a7f-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c5a7f-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5a7f-153">NOTES</span></span>

## <span data-ttu-id="c5a7f-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5a7f-154">RELATED LINKS</span></span>

[<span data-ttu-id="c5a7f-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c5a7f-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="c5a7f-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c5a7f-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="c5a7f-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c5a7f-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

