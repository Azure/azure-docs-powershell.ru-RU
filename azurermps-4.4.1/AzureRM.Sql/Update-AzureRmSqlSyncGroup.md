---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: a530a9e99c698ca6b827df94b1966e4df065790d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566671"
---
# <span data-ttu-id="af054-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="af054-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="af054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af054-102">SYNOPSIS</span></span>
<span data-ttu-id="af054-103">Обновляет группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="af054-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af054-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af054-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af054-105">DESCRIPTION</span></span>
<span data-ttu-id="af054-106">Командлет **Update-AzureRmSqlSyncGroup** изменяет свойства группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="af054-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="af054-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af054-107">EXAMPLES</span></span>

### <span data-ttu-id="af054-108">Пример 1: Обновление группы синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="af054-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
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

<span data-ttu-id="af054-109">Эта команда обновляет группу синхронизации для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="af054-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="af054-110">"schema.json" — файл на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="af054-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="af054-111">Он имеет полезные данные shema в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="af054-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="af054-112">Пример JSON схемы: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"столбцы": [{"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-AD07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "", "MasterSyncMemberName".</span><span class="sxs-lookup"><span data-stu-id="af054-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="af054-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af054-113">PARAMETERS</span></span>

### <span data-ttu-id="af054-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af054-114">-Confirm</span></span>
<span data-ttu-id="af054-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af054-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af054-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="af054-116">-DatabaseCredential</span></span>
<span data-ttu-id="af054-117">Учетные данные проверки подлинности SQL для базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="af054-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="af054-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af054-118">-DatabaseName</span></span>
<span data-ttu-id="af054-119">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="af054-119">SQL Database name.</span></span>

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

### <span data-ttu-id="af054-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="af054-120">-IntervalInSeconds</span></span>
<span data-ttu-id="af054-121">Частота выполнения синхронизации данных (в секундах).</span><span class="sxs-lookup"><span data-stu-id="af054-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="af054-122">По умолчанию используется значение-1, что означает, что автоматическая синхронизация не включена.</span><span class="sxs-lookup"><span data-stu-id="af054-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="af054-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af054-123">-Name</span></span>
<span data-ttu-id="af054-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="af054-124">The sync group name.</span></span>

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

### <span data-ttu-id="af054-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af054-125">-ResourceGroupName</span></span>
<span data-ttu-id="af054-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af054-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="af054-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="af054-127">-SchemaFile</span></span>
<span data-ttu-id="af054-128">Путь к файлу схемы.</span><span class="sxs-lookup"><span data-stu-id="af054-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="af054-129">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="af054-129">-ServerName</span></span>
<span data-ttu-id="af054-130">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af054-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="af054-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af054-131">-WhatIf</span></span>
<span data-ttu-id="af054-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af054-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af054-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af054-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af054-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af054-134">-DefaultProfile</span></span>
<span data-ttu-id="af054-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af054-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af054-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af054-136">CommonParameters</span></span>
<span data-ttu-id="af054-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af054-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af054-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af054-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af054-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af054-139">INPUTS</span></span>

## <span data-ttu-id="af054-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af054-140">OUTPUTS</span></span>

### <span data-ttu-id="af054-141">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="af054-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="af054-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="af054-142">NOTES</span></span>

## <span data-ttu-id="af054-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af054-143">RELATED LINKS</span></span>

[<span data-ttu-id="af054-144">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="af054-144">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="af054-145">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="af054-145">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="af054-146">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="af054-146">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

