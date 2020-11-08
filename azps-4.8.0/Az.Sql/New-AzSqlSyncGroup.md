---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080235"
---
# <span data-ttu-id="5d6dd-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5d6dd-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="5d6dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6dd-103">Создает группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5d6dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d6dd-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d6dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="5d6dd-106">Командлет **New-AzSqlSyncGroup** создает группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="5d6dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d6dd-107">EXAMPLES</span></span>

### <span data-ttu-id="5d6dd-108">Пример 1: создание группы синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="5d6dd-109">Эта команда создает группу синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="5d6dd-110">"schema.json" — файл на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="5d6dd-111">Она включает полезные данные схемы в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="5d6dd-112">Пример JSON схемы: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"столбцы": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "", "MasterSyncMemberName".</span><span class="sxs-lookup"><span data-stu-id="5d6dd-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="5d6dd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d6dd-113">PARAMETERS</span></span>

### <span data-ttu-id="5d6dd-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d6dd-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="5d6dd-115">Политика разрешения конфликтов между центром и базой данных участников в группе "Синхронизация".</span><span class="sxs-lookup"><span data-stu-id="5d6dd-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="5d6dd-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="5d6dd-116">-DatabaseCredential</span></span>
<span data-ttu-id="5d6dd-117">Учетные данные проверки подлинности SQL для базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="5d6dd-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d6dd-118">-DatabaseName</span></span>
<span data-ttu-id="5d6dd-119">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5d6dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6dd-120">-DefaultProfile</span></span>
<span data-ttu-id="5d6dd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5d6dd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d6dd-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5d6dd-122">-IntervalInSeconds</span></span>
<span data-ttu-id="5d6dd-123">Частота выполнения синхронизации данных (в секундах).</span><span class="sxs-lookup"><span data-stu-id="5d6dd-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="5d6dd-124">По умолчанию используется значение-1, что означает, что автоматическая синхронизация не включена.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="5d6dd-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d6dd-125">-Name</span></span>
<span data-ttu-id="5d6dd-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-126">The sync group name.</span></span>

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

### <span data-ttu-id="5d6dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d6dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d6dd-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d6dd-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="5d6dd-129">-SchemaFile</span></span>
<span data-ttu-id="5d6dd-130">Путь к файлу схемы.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="5d6dd-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5d6dd-131">-ServerName</span></span>
<span data-ttu-id="5d6dd-132">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5d6dd-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d6dd-133">-SyncDatabaseName</span></span>
<span data-ttu-id="5d6dd-134">База данных, которая используется для хранения метаданных, связанных с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="5d6dd-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d6dd-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="5d6dd-136">Группа ресурсов, к которой принадлежит база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="5d6dd-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="5d6dd-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="5d6dd-138">Сервер, на котором размещается база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="5d6dd-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5d6dd-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="5d6dd-140">Используйте подключение к частной ссылке при подключении к концентратору этой группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="5d6dd-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d6dd-141">-Confirm</span></span>
<span data-ttu-id="5d6dd-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d6dd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d6dd-143">-WhatIf</span></span>
<span data-ttu-id="5d6dd-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d6dd-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d6dd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6dd-146">CommonParameters</span></span>
<span data-ttu-id="5d6dd-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d6dd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6dd-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d6dd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6dd-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d6dd-149">INPUTS</span></span>

### <span data-ttu-id="5d6dd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5d6dd-150">System.String</span></span>

## <span data-ttu-id="5d6dd-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d6dd-151">OUTPUTS</span></span>

### <span data-ttu-id="5d6dd-152">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="5d6dd-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="5d6dd-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d6dd-153">NOTES</span></span>

## <span data-ttu-id="5d6dd-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d6dd-154">RELATED LINKS</span></span>

[<span data-ttu-id="5d6dd-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5d6dd-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="5d6dd-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5d6dd-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="5d6dd-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5d6dd-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

