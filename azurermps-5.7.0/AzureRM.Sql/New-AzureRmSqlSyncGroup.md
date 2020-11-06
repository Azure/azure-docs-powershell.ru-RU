---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 65ac7bb4a63fa8519bd8f0b0c006209d5f171833
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566061"
---
# <span data-ttu-id="77319-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="77319-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="77319-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77319-102">SYNOPSIS</span></span>
<span data-ttu-id="77319-103">Создает группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77319-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77319-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77319-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77319-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77319-105">DESCRIPTION</span></span>
<span data-ttu-id="77319-106">Командлет **New-AzureRmSqlSyncGroup** создает группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77319-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="77319-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77319-107">EXAMPLES</span></span>

### <span data-ttu-id="77319-108">Пример 1: создание группы синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77319-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="77319-109">Эта команда создает группу синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77319-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="77319-110">"schema.json" — файл на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="77319-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="77319-111">Он имеет полезные данные shema в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="77319-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="77319-112">Пример JSON схемы: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"столбцы": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "", "MasterSyncMemberName".</span><span class="sxs-lookup"><span data-stu-id="77319-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="77319-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77319-113">PARAMETERS</span></span>

### <span data-ttu-id="77319-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="77319-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="77319-115">Политика разрешения конфликтов между центром и базой данных участников в группе "Синхронизация".</span><span class="sxs-lookup"><span data-stu-id="77319-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77319-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="77319-116">-DatabaseCredential</span></span>
<span data-ttu-id="77319-117">Учетные данные проверки подлинности SQL для базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="77319-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77319-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77319-118">-DatabaseName</span></span>
<span data-ttu-id="77319-119">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="77319-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="77319-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77319-120">-DefaultProfile</span></span>
<span data-ttu-id="77319-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77319-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77319-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="77319-122">-IntervalInSeconds</span></span>
<span data-ttu-id="77319-123">Частота выполнения синхронизации данных (в секундах).</span><span class="sxs-lookup"><span data-stu-id="77319-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="77319-124">По умолчанию используется значение-1, что означает, что автоматическая синхронизация не включена.</span><span class="sxs-lookup"><span data-stu-id="77319-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77319-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77319-125">-Name</span></span>
<span data-ttu-id="77319-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="77319-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77319-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77319-127">-ResourceGroupName</span></span>
<span data-ttu-id="77319-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77319-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="77319-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="77319-129">-SchemaFile</span></span>
<span data-ttu-id="77319-130">Путь к файлу схемы.</span><span class="sxs-lookup"><span data-stu-id="77319-130">The path of the schema file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77319-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="77319-131">-ServerName</span></span>
<span data-ttu-id="77319-132">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77319-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="77319-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="77319-133">-SyncDatabaseName</span></span>
<span data-ttu-id="77319-134">База данных, которая используется для хранения метаданных, связанных с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="77319-134">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77319-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77319-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="77319-136">Группа ресурсов, к которой принадлежит база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="77319-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77319-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="77319-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="77319-138">Сервер, на котором размещается база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="77319-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77319-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77319-139">-Confirm</span></span>
<span data-ttu-id="77319-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77319-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77319-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77319-141">-WhatIf</span></span>
<span data-ttu-id="77319-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77319-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77319-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77319-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77319-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77319-144">CommonParameters</span></span>
<span data-ttu-id="77319-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77319-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77319-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77319-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77319-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77319-147">INPUTS</span></span>

### <span data-ttu-id="77319-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="77319-148">None</span></span>
<span data-ttu-id="77319-149">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="77319-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77319-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77319-150">OUTPUTS</span></span>

### <span data-ttu-id="77319-151">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="77319-151">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="77319-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="77319-152">NOTES</span></span>

## <span data-ttu-id="77319-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77319-153">RELATED LINKS</span></span>

[<span data-ttu-id="77319-154">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="77319-154">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="77319-155">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="77319-155">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="77319-156">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="77319-156">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

