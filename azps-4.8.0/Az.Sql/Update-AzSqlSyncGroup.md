---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 9c4a6572a5a2025bba23758160378519524b8ce7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236568"
---
# <span data-ttu-id="2e252-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2e252-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="2e252-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e252-102">SYNOPSIS</span></span>
<span data-ttu-id="2e252-103">Обновляет группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2e252-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2e252-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e252-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e252-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e252-105">DESCRIPTION</span></span>
<span data-ttu-id="2e252-106">Командлет **Update-AzSqlSyncGroup** изменяет свойства группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2e252-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2e252-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e252-107">EXAMPLES</span></span>

### <span data-ttu-id="2e252-108">Пример 1: Обновление группы синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2e252-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="2e252-109">Эта команда обновляет группу синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2e252-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="2e252-110">"schema.json" — файл на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="2e252-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="2e252-111">Она включает полезные данные схемы в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2e252-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="2e252-112">Пример JSON схемы: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"столбцы": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "", "MasterSyncMemberName".</span><span class="sxs-lookup"><span data-stu-id="2e252-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="2e252-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e252-113">PARAMETERS</span></span>

### <span data-ttu-id="2e252-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="2e252-114">-DatabaseCredential</span></span>
<span data-ttu-id="2e252-115">Учетные данные проверки подлинности SQL для базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="2e252-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="2e252-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2e252-116">-DatabaseName</span></span>
<span data-ttu-id="2e252-117">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2e252-117">SQL Database name.</span></span>

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

### <span data-ttu-id="2e252-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e252-118">-DefaultProfile</span></span>
<span data-ttu-id="2e252-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2e252-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e252-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2e252-120">-IntervalInSeconds</span></span>
<span data-ttu-id="2e252-121">Частота выполнения синхронизации данных (в секундах).</span><span class="sxs-lookup"><span data-stu-id="2e252-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="2e252-122">По умолчанию используется значение-1, что означает, что автоматическая синхронизация не включена.</span><span class="sxs-lookup"><span data-stu-id="2e252-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="2e252-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e252-123">-Name</span></span>
<span data-ttu-id="2e252-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2e252-124">The sync group name.</span></span>

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

### <span data-ttu-id="2e252-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e252-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e252-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e252-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="2e252-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="2e252-127">-SchemaFile</span></span>
<span data-ttu-id="2e252-128">Путь к файлу схемы.</span><span class="sxs-lookup"><span data-stu-id="2e252-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="2e252-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2e252-129">-ServerName</span></span>
<span data-ttu-id="2e252-130">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2e252-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2e252-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2e252-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="2e252-132">Следует ли использовать соединение с частными ссылками при подключении к концентратору этой группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2e252-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e252-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e252-133">-Confirm</span></span>
<span data-ttu-id="2e252-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e252-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e252-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e252-135">-WhatIf</span></span>
<span data-ttu-id="2e252-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e252-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e252-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e252-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e252-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e252-138">CommonParameters</span></span>
<span data-ttu-id="2e252-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e252-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e252-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e252-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e252-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e252-141">INPUTS</span></span>

### <span data-ttu-id="2e252-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2e252-142">System.String</span></span>

## <span data-ttu-id="2e252-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e252-143">OUTPUTS</span></span>

### <span data-ttu-id="2e252-144">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="2e252-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="2e252-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e252-145">NOTES</span></span>

## <span data-ttu-id="2e252-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e252-146">RELATED LINKS</span></span>

[<span data-ttu-id="2e252-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2e252-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="2e252-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2e252-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="2e252-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2e252-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

