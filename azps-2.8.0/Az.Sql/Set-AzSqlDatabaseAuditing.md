---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905929"
---
# <span data-ttu-id="50918-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="50918-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="50918-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50918-102">SYNOPSIS</span></span>
<span data-ttu-id="50918-103">**Внимание! этот командлет устарел, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) заменяет его.**</span><span class="sxs-lookup"><span data-stu-id="50918-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="50918-104">Изменение параметров аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="50918-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="50918-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50918-105">SYNTAX</span></span>

### <span data-ttu-id="50918-106">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50918-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50918-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="50918-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50918-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="50918-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50918-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="50918-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50918-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="50918-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50918-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="50918-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50918-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="50918-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50918-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="50918-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50918-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50918-114">DESCRIPTION</span></span>
<span data-ttu-id="50918-115">Командлет **Set-AzSqlDatabaseAuditing** изменяет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="50918-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="50918-116">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="50918-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="50918-117">Назначение журналов аудита определяется указанием одного из следующих параметров переключателя: BlobStorage, LogAnalytics или EventHub (если ничего не указано, по умолчанию используется значение BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="50918-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="50918-118">Используйте параметр *State* для включения или отключения политики.</span><span class="sxs-lookup"><span data-stu-id="50918-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="50918-119">Если в качестве назначения журналов аудита задано хранилище BLOB-объектов, укажите параметр *StorageAccountName* , чтобы определить учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранения.</span><span class="sxs-lookup"><span data-stu-id="50918-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="50918-120">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="50918-121">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущие параметры аудита в дополнение к идентификаторам базы данных.</span><span class="sxs-lookup"><span data-stu-id="50918-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="50918-122">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="50918-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="50918-123">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50918-123">EXAMPLES</span></span>

### <span data-ttu-id="50918-124">Пример 1: Включение политики аудита хранилища BLOB-объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="50918-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="50918-125">Пример 2: отключение политики аудита хранилища BLOB-объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="50918-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="50918-126">Пример 3: Включение политики аудита хранилища BLOB-объектов для базы данных Azure SQL с помощью учетной записи хранения из другой подписки</span><span class="sxs-lookup"><span data-stu-id="50918-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="50918-127">Пример 4: Включение политики аудита хранилища BLOB-объектов для базы данных SQL Azure с расширенной фильтрацией с помощью предиката T-SQL</span><span class="sxs-lookup"><span data-stu-id="50918-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="50918-128">Пример 5. Удаление параметра расширенной фильтрации из политики аудита хранилища BLOB-объектов в базе данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="50918-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="50918-129">Пример 6: Включение политики аудита центра событий для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="50918-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="50918-130">Пример 7: отключение политики аудита центра событий для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="50918-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="50918-131">Пример 8: Включение политики аудита анализа журналов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="50918-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="50918-132">Пример 9: отключение политики аудита анализа журналов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="50918-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="50918-133">Пример 10: отключение через конвейер, политика аудита анализа журналов для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="50918-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="50918-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50918-134">PARAMETERS</span></span>

### <span data-ttu-id="50918-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50918-135">-AsJob</span></span>
<span data-ttu-id="50918-136">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="50918-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50918-137">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="50918-137">-AuditAction</span></span>
<span data-ttu-id="50918-138">Набор действий аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-138">The set of audit actions.</span></span>  
<span data-ttu-id="50918-139">Ниже перечислены поддерживаемые действия для аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="50918-140">ВЫБРАННЫЕ</span><span class="sxs-lookup"><span data-stu-id="50918-140">SELECT</span></span>  
<span data-ttu-id="50918-141">Обновление</span><span class="sxs-lookup"><span data-stu-id="50918-141">UPDATE</span></span>  
<span data-ttu-id="50918-142">ВСТАВКОЙ</span><span class="sxs-lookup"><span data-stu-id="50918-142">INSERT</span></span>  
<span data-ttu-id="50918-143">Удаление</span><span class="sxs-lookup"><span data-stu-id="50918-143">DELETE</span></span>  
<span data-ttu-id="50918-144">ВЫПОЛНЯЕТ</span><span class="sxs-lookup"><span data-stu-id="50918-144">EXECUTE</span></span>  
<span data-ttu-id="50918-145">ОШИБК</span><span class="sxs-lookup"><span data-stu-id="50918-145">RECEIVE</span></span>  
<span data-ttu-id="50918-146">ССЫЛАЕТСЯ на общую форму для определения действия, подлежащие аудиту: [Action] ON [Object] BY [Principal] Обратите внимание, что [Object] в приведенном выше формате может ссылаться на объект, например на таблицу, представление или сохраненную процедуру, а также на всю базу данных или схему.</span><span class="sxs-lookup"><span data-stu-id="50918-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="50918-147">В последних случаях используются базы данных форм: [dbname] и SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="50918-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="50918-148">Например:</span><span class="sxs-lookup"><span data-stu-id="50918-148">For example:</span></span>  
<span data-ttu-id="50918-149">ВЫБОР на dbo. myTable по открытым</span><span class="sxs-lookup"><span data-stu-id="50918-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="50918-150">Выберите базу данных:: myDatabase по общедоступным</span><span class="sxs-lookup"><span data-stu-id="50918-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="50918-151">Выбор схемы:: mySchema по общедоступным</span><span class="sxs-lookup"><span data-stu-id="50918-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="50918-152">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="50918-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="50918-153">-AuditActionGroup</span></span>
<span data-ttu-id="50918-154">Рекомендуемый набор групп действий: в этом случае будут проверены все запросы и хранимые процедуры, выполненные для базы данных, а также успешные и неудачные входные данные.</span><span class="sxs-lookup"><span data-stu-id="50918-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="50918-155">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="50918-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="50918-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="50918-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="50918-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="50918-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="50918-158">Это сочетание также является набором, настроенным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="50918-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="50918-159">Эти группы охватывают все инструкции SQL и хранимые процедуры, выполненные для базы данных, и их нельзя использовать в сочетании с другими группами, так как это приводит к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="50918-160">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="50918-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="50918-161">-BlobStorage</span></span>
<span data-ttu-id="50918-162">Указывает, что назначение журналов аудита — хранилище BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="50918-162">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="50918-163">-DatabaseName</span></span>
<span data-ttu-id="50918-164">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="50918-164">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50918-165">-DefaultProfile</span></span>
<span data-ttu-id="50918-166">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50918-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50918-167">-EventHub</span><span class="sxs-lookup"><span data-stu-id="50918-167">-EventHub</span></span>
<span data-ttu-id="50918-168">Указывает на то, что назначение журналов аудита является центром событий</span><span class="sxs-lookup"><span data-stu-id="50918-168">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="50918-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="50918-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="50918-170">Идентификатор ресурса для правила авторизации центра событий</span><span class="sxs-lookup"><span data-stu-id="50918-170">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="50918-171">-EventHubName</span></span>
<span data-ttu-id="50918-172">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="50918-172">The name of the event hub.</span></span> <span data-ttu-id="50918-173">Если при предоставлении EventHubAuthorizationRuleResourceId не задано значение None, будет выбран центр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="50918-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-174">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50918-174">-InputObject</span></span>
<span data-ttu-id="50918-175">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-175">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="50918-176">-LogAnalytics</span></span>
<span data-ttu-id="50918-177">Указывает, что назначение журналов аудита — это анализ журнала</span><span class="sxs-lookup"><span data-stu-id="50918-177">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="50918-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50918-178">-PassThru</span></span>
<span data-ttu-id="50918-179">Указывает, следует ли выводить политику аудита при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="50918-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="50918-180">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="50918-180">-PredicateExpression</span></span>
<span data-ttu-id="50918-181">Предикат T-SQL (предложение WHERE), используемый для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50918-182">-ResourceGroupName</span></span>
<span data-ttu-id="50918-183">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50918-183">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-184">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="50918-184">-RetentionInDays</span></span>
<span data-ttu-id="50918-185">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-185">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-186">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="50918-186">-ServerName</span></span>
<span data-ttu-id="50918-187">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="50918-187">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-188">-State</span><span class="sxs-lookup"><span data-stu-id="50918-188">-State</span></span>
<span data-ttu-id="50918-189">Состояние политики.</span><span class="sxs-lookup"><span data-stu-id="50918-189">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="50918-190">-StorageAccountName</span></span>
<span data-ttu-id="50918-191">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="50918-191">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50918-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="50918-193">Идентификатор подписки для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="50918-193">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="50918-194">-StorageKeyType</span></span>
<span data-ttu-id="50918-195">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="50918-195">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="50918-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="50918-197">ИДЕНТИФИКАТОР рабочей области (ИД ресурса) рабочей области для анализа журналов, в которую вы хотите отправлять журналы аудита.</span><span class="sxs-lookup"><span data-stu-id="50918-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="50918-198">Пример:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="50918-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50918-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50918-199">-Confirm</span></span>
<span data-ttu-id="50918-200">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50918-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50918-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50918-201">-WhatIf</span></span>
<span data-ttu-id="50918-202">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50918-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50918-203">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50918-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50918-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50918-204">CommonParameters</span></span>
<span data-ttu-id="50918-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50918-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50918-206">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50918-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50918-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50918-207">INPUTS</span></span>

### <span data-ttu-id="50918-208">System. String</span><span class="sxs-lookup"><span data-stu-id="50918-208">System.String</span></span>

### <span data-ttu-id="50918-209">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="50918-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="50918-210">Microsoft. Azure. Commands. SQL. Audit. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="50918-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="50918-211">System. String []</span><span class="sxs-lookup"><span data-stu-id="50918-211">System.String[]</span></span>

### <span data-ttu-id="50918-212">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="50918-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="50918-213">System. GUID</span><span class="sxs-lookup"><span data-stu-id="50918-213">System.Guid</span></span>

### <span data-ttu-id="50918-214">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="50918-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="50918-215">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50918-215">OUTPUTS</span></span>

### <span data-ttu-id="50918-216">Microsoft. Azure. Commands. SQL. Audit. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="50918-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="50918-217">Пуск</span><span class="sxs-lookup"><span data-stu-id="50918-217">NOTES</span></span>

## <span data-ttu-id="50918-218">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50918-218">RELATED LINKS</span></span>
