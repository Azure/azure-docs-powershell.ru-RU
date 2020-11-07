---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906277"
---
# <span data-ttu-id="3ba19-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="3ba19-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="3ba19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ba19-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba19-103">**Внимание! этот командлет устарел, его можно заменить [на Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) .**</span><span class="sxs-lookup"><span data-stu-id="3ba19-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="3ba19-104">Получает параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba19-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="3ba19-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ba19-105">SYNTAX</span></span>

### <span data-ttu-id="3ba19-106">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ba19-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba19-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="3ba19-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba19-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="3ba19-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba19-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="3ba19-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba19-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="3ba19-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba19-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="3ba19-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ba19-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba19-112">DESCRIPTION</span></span>
<span data-ttu-id="3ba19-113">Командлет **Get-AzSqlDatabaseAuditing** получает параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba19-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="3ba19-114">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="3ba19-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="3ba19-115">Назначение журналов аудита определяется указанием одного из следующих параметров переключателя: BlobStorage, LogAnalytics или EventHub (если ничего не указано, по умолчанию используется значение BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="3ba19-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="3ba19-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ba19-116">EXAMPLES</span></span>

### <span data-ttu-id="3ba19-117">Пример 1: получение параметров аудита хранилища BLOB-объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3ba19-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="3ba19-118">Пример 2: получение параметров аудита хранилища BLOB-объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3ba19-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="3ba19-119">Пример 3: Get, с помощью конвейера параметры аудита хранилища BLOB-объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3ba19-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="3ba19-120">Пример 4: получение параметров аудита центра событий для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3ba19-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="3ba19-121">Пример 5: получение через конвейер, параметры аудита центра событий для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3ba19-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="3ba19-122">Пример 6: получение параметров аудита для анализа журналов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3ba19-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="3ba19-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ba19-123">PARAMETERS</span></span>

### <span data-ttu-id="3ba19-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="3ba19-124">-BlobStorage</span></span>
<span data-ttu-id="3ba19-125">Указывает, что назначение журналов аудита — хранилище BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="3ba19-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba19-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ba19-126">-DatabaseName</span></span>
<span data-ttu-id="3ba19-127">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3ba19-127">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba19-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba19-128">-DefaultProfile</span></span>
<span data-ttu-id="3ba19-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba19-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ba19-130">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3ba19-130">-EventHub</span></span>
<span data-ttu-id="3ba19-131">Указывает на то, что назначение журналов аудита является центром событий</span><span class="sxs-lookup"><span data-stu-id="3ba19-131">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba19-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ba19-132">-InputObject</span></span>
<span data-ttu-id="3ba19-133">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="3ba19-133">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba19-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="3ba19-134">-LogAnalytics</span></span>
<span data-ttu-id="3ba19-135">Указывает, что назначение журналов аудита — это анализ журнала</span><span class="sxs-lookup"><span data-stu-id="3ba19-135">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba19-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ba19-136">-ResourceGroupName</span></span>
<span data-ttu-id="3ba19-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ba19-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba19-138">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3ba19-138">-ServerName</span></span>
<span data-ttu-id="3ba19-139">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3ba19-139">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba19-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ba19-140">-Confirm</span></span>
<span data-ttu-id="3ba19-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba19-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ba19-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ba19-142">-WhatIf</span></span>
<span data-ttu-id="3ba19-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba19-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ba19-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ba19-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ba19-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba19-145">CommonParameters</span></span>
<span data-ttu-id="3ba19-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ba19-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba19-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ba19-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba19-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ba19-148">INPUTS</span></span>

### <span data-ttu-id="3ba19-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba19-149">System.String</span></span>

### <span data-ttu-id="3ba19-150">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3ba19-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="3ba19-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3ba19-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3ba19-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba19-152">OUTPUTS</span></span>

### <span data-ttu-id="3ba19-153">Microsoft. Azure. Commands. SQL. Audit. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="3ba19-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="3ba19-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ba19-154">NOTES</span></span>

## <span data-ttu-id="3ba19-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ba19-155">RELATED LINKS</span></span>
