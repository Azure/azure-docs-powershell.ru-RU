---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: bcae25cba6eae5f883bffb7248cbca6f5516bcfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565109"
---
# <span data-ttu-id="a7e7b-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a7e7b-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="a7e7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e7b-103">Создает группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7e7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7e7b-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e7b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e7b-106">Командлет **New-AzureRmSqlSyncGroup** создает группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="a7e7b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="a7e7b-108">Пример 1: создание группы синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="a7e7b-109">Эта команда создает группу синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="a7e7b-110">"schema.json" — файл на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="a7e7b-111">Он имеет полезные данные shema в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="a7e7b-112">Пример JSON схемы: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"столбцы": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "", "MasterSyncMemberName".</span><span class="sxs-lookup"><span data-stu-id="a7e7b-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="a7e7b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7e7b-113">PARAMETERS</span></span>

### <span data-ttu-id="a7e7b-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7e7b-114">-Confirm</span></span>
<span data-ttu-id="a7e7b-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7e7b-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7e7b-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="a7e7b-117">Политика разрешения конфликтов между центром и базой данных участников в группе "Синхронизация".</span><span class="sxs-lookup"><span data-stu-id="a7e7b-117">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="a7e7b-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7e7b-118">-DatabaseName</span></span>
<span data-ttu-id="a7e7b-119">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a7e7b-120">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a7e7b-120">-DatabaseCredential</span></span>
<span data-ttu-id="a7e7b-121">Учетные данные проверки подлинности SQL для базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-121">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="a7e7b-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a7e7b-122">-IntervalInSeconds</span></span>
<span data-ttu-id="a7e7b-123">Частота выполнения синхронизации данных (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a7e7b-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="a7e7b-124">По умолчанию используется значение-1, что означает, что автоматическая синхронизация не включена.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="a7e7b-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7e7b-125">-Name</span></span>
<span data-ttu-id="a7e7b-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-126">The sync group name.</span></span>

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

### <span data-ttu-id="a7e7b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e7b-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7e7b-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7e7b-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="a7e7b-129">-SchemaFile</span></span>
<span data-ttu-id="a7e7b-130">Путь к файлу схемы.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="a7e7b-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a7e7b-131">-ServerName</span></span>
<span data-ttu-id="a7e7b-132">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a7e7b-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7e7b-133">-SyncDatabaseName</span></span>
<span data-ttu-id="a7e7b-134">База данных, которая используется для хранения метаданных, связанных с синхронизацией.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="a7e7b-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e7b-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="a7e7b-136">Группа ресурсов, к которой принадлежит база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="a7e7b-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="a7e7b-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="a7e7b-138">Сервер, на котором размещается база данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="a7e7b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e7b-139">-WhatIf</span></span>
<span data-ttu-id="a7e7b-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7e7b-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7e7b-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e7b-142">-DefaultProfile</span></span>
<span data-ttu-id="a7e7b-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e7b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e7b-144">CommonParameters</span></span>
<span data-ttu-id="a7e7b-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7e7b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e7b-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e7b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e7b-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7e7b-147">INPUTS</span></span>

## <span data-ttu-id="a7e7b-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7e7b-148">OUTPUTS</span></span>

### <span data-ttu-id="a7e7b-149">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a7e7b-149">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a7e7b-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7e7b-150">NOTES</span></span>

## <span data-ttu-id="a7e7b-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7e7b-151">RELATED LINKS</span></span>

[<span data-ttu-id="a7e7b-152">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a7e7b-152">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a7e7b-153">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a7e7b-153">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a7e7b-154">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a7e7b-154">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

