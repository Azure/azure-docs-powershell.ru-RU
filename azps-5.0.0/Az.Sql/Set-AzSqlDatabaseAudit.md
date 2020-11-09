---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: e13e97bd9f636de68344f83b600e440252431a22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248801"
---
# <span data-ttu-id="b32ce-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="b32ce-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="b32ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b32ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b32ce-103">Изменение параметров аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b32ce-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="b32ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b32ce-104">SYNTAX</span></span>

### <span data-ttu-id="b32ce-105">DatabaseParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b32ce-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b32ce-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b32ce-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b32ce-107">DESCRIPTION</span></span>
<span data-ttu-id="b32ce-108">Командлет **Set-AzSqlDatabaseAudit** изменяет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b32ce-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="b32ce-109">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="b32ce-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b32ce-110">Когда хранилище BLOB-объектов является конечным для журналов аудита, укажите параметр *StorageAccountResourceId* , чтобы определить учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранения.</span><span class="sxs-lookup"><span data-stu-id="b32ce-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="b32ce-111">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="b32ce-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b32ce-112">EXAMPLES</span></span>

### <span data-ttu-id="b32ce-113">Пример 1: Включение политики аудита хранилища BLOB-объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b32ce-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="b32ce-114">Пример 2: отключение политики аудита хранилища BLOB-объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b32ce-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="b32ce-115">Пример 3: Включение политики аудита хранилища BLOB-объектов для базы данных SQL Azure с расширенной фильтрацией с помощью предиката T-SQL</span><span class="sxs-lookup"><span data-stu-id="b32ce-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="b32ce-116">Пример 4: Удаление параметра расширенной фильтрации из политики аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b32ce-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="b32ce-117">Пример 5: Включение политики аудита центра событий для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b32ce-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="b32ce-118">Пример 6: отключение политики аудита центра событий для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b32ce-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="b32ce-119">Пример 7: Включение политики аудита анализа журналов для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b32ce-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="b32ce-120">Пример 8: отключение политики аудита анализа журналов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="b32ce-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="b32ce-121">Пример 9: отключение, с помощью конвейера, политика аудита анализа журналов для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b32ce-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="b32ce-122">Пример 10: отключение отправки записей аудита для базы данных SQL Azure в хранилище BLOB-объектов и разрешение их отправки в службу анализа журнала.</span><span class="sxs-lookup"><span data-stu-id="b32ce-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="b32ce-123">Пример 11. разрешите отправку записей аудита для базы данных SQL Azure в хранилище BLOB-объектов, на концентратор событий и в анализ журнала.</span><span class="sxs-lookup"><span data-stu-id="b32ce-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="b32ce-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b32ce-124">PARAMETERS</span></span>

### <span data-ttu-id="b32ce-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="b32ce-125">-AuditAction</span></span>
<span data-ttu-id="b32ce-126">Набор действий аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-126">The set of audit actions.</span></span>  
<span data-ttu-id="b32ce-127">Ниже перечислены поддерживаемые действия для аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="b32ce-128">ВЫБРАННЫЕ</span><span class="sxs-lookup"><span data-stu-id="b32ce-128">SELECT</span></span>  
<span data-ttu-id="b32ce-129">Обновление</span><span class="sxs-lookup"><span data-stu-id="b32ce-129">UPDATE</span></span>  
<span data-ttu-id="b32ce-130">ВСТАВКОЙ</span><span class="sxs-lookup"><span data-stu-id="b32ce-130">INSERT</span></span>  
<span data-ttu-id="b32ce-131">Удаление</span><span class="sxs-lookup"><span data-stu-id="b32ce-131">DELETE</span></span>  
<span data-ttu-id="b32ce-132">ВЫПОЛНЯЕТ</span><span class="sxs-lookup"><span data-stu-id="b32ce-132">EXECUTE</span></span>  
<span data-ttu-id="b32ce-133">ОШИБК</span><span class="sxs-lookup"><span data-stu-id="b32ce-133">RECEIVE</span></span>  
<span data-ttu-id="b32ce-134">Указывает</span><span class="sxs-lookup"><span data-stu-id="b32ce-134">REFERENCES</span></span>  
<span data-ttu-id="b32ce-135">Общая форма для определения действия, подлежащие аудиту: [Action] ON [Object] BY [Principal] Обратите внимание на то, что [Object] в приведенном выше формате может ссылаться на объект, например на таблицу, представление или сохраненную процедуру, а также на всю базу данных или схему.</span><span class="sxs-lookup"><span data-stu-id="b32ce-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="b32ce-136">В последних случаях используются базы данных форм: [dbname] и SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="b32ce-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="b32ce-137">Например:</span><span class="sxs-lookup"><span data-stu-id="b32ce-137">For example:</span></span>  
<span data-ttu-id="b32ce-138">ВЫБОР на dbo. myTable по открытым</span><span class="sxs-lookup"><span data-stu-id="b32ce-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="b32ce-139">Выберите базу данных:: myDatabase по общедоступным</span><span class="sxs-lookup"><span data-stu-id="b32ce-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="b32ce-140">Выбор схемы:: mySchema по общедоступным</span><span class="sxs-lookup"><span data-stu-id="b32ce-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="b32ce-141">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="b32ce-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="b32ce-142">-AuditActionGroup</span></span>
<span data-ttu-id="b32ce-143">Рекомендуемый набор групп действий: в этом случае будут проверены все запросы и хранимые процедуры, выполненные для базы данных, а также успешные и неудачные входные данные.</span><span class="sxs-lookup"><span data-stu-id="b32ce-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="b32ce-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="b32ce-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="b32ce-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="b32ce-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="b32ce-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="b32ce-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="b32ce-147">Это сочетание также является набором, настроенным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b32ce-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="b32ce-148">Эти группы охватывают все инструкции SQL и хранимые процедуры, выполненные для базы данных, и их нельзя использовать в сочетании с другими группами, так как это приводит к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="b32ce-149">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="b32ce-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="b32ce-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="b32ce-151">Указывает, является ли хранилище BLOB-объектов конечным для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b32ce-152">-DatabaseName</span></span>
<span data-ttu-id="b32ce-153">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b32ce-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b32ce-154">-DatabaseObject</span></span>
<span data-ttu-id="b32ce-155">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32ce-156">-DefaultProfile</span></span>
<span data-ttu-id="b32ce-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b32ce-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b32ce-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="b32ce-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="b32ce-159">Идентификатор ресурса для правила авторизации центра событий</span><span class="sxs-lookup"><span data-stu-id="b32ce-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="b32ce-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="b32ce-160">-EventHubName</span></span>
<span data-ttu-id="b32ce-161">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="b32ce-161">The name of the event hub.</span></span> <span data-ttu-id="b32ce-162">Если при предоставлении EventHubAuthorizationRuleResourceId не задано значение None, будет выбран центр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b32ce-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="b32ce-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="b32ce-163">-EventHubTargetState</span></span>
<span data-ttu-id="b32ce-164">Указывает, является ли концентратор событий конечным для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="b32ce-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="b32ce-166">Указывает, является ли аналитика журналом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b32ce-167">-PassThru</span></span>
<span data-ttu-id="b32ce-168">Указывает, следует ли выводить политику аудита при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="b32ce-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="b32ce-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="b32ce-169">-PredicateExpression</span></span>
<span data-ttu-id="b32ce-170">Предикат T-SQL (предложение WHERE), используемый для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="b32ce-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32ce-171">-ResourceGroupName</span></span>
<span data-ttu-id="b32ce-172">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b32ce-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b32ce-173">-RetentionInDays</span></span>
<span data-ttu-id="b32ce-174">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-175">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b32ce-175">-ServerName</span></span>
<span data-ttu-id="b32ce-176">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b32ce-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="b32ce-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="b32ce-178">Идентификатор ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b32ce-178">The storage account resource id</span></span>

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

### <span data-ttu-id="b32ce-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b32ce-179">-StorageKeyType</span></span>
<span data-ttu-id="b32ce-180">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="b32ce-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b32ce-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b32ce-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="b32ce-182">ИДЕНТИФИКАТОР рабочей области (ИД ресурса) рабочей области для анализа журналов, в которую вы хотите отправлять журналы аудита.</span><span class="sxs-lookup"><span data-stu-id="b32ce-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="b32ce-183">Пример:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="b32ce-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="b32ce-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b32ce-184">-Confirm</span></span>
<span data-ttu-id="b32ce-185">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b32ce-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32ce-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32ce-186">-WhatIf</span></span>
<span data-ttu-id="b32ce-187">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b32ce-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b32ce-188">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b32ce-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32ce-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32ce-189">CommonParameters</span></span>
<span data-ttu-id="b32ce-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b32ce-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32ce-191">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b32ce-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32ce-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b32ce-192">INPUTS</span></span>

### <span data-ttu-id="b32ce-193">System. String</span><span class="sxs-lookup"><span data-stu-id="b32ce-193">System.String</span></span>

### <span data-ttu-id="b32ce-194">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b32ce-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="b32ce-195">Microsoft. Azure. Commands. SQL. Audit. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="b32ce-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="b32ce-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="b32ce-196">System.String[]</span></span>

### <span data-ttu-id="b32ce-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b32ce-197">System.Guid</span></span>

### <span data-ttu-id="b32ce-198">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b32ce-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b32ce-199">Microsoft. Azure. Commands. SQL. Audit. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="b32ce-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="b32ce-200">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b32ce-200">OUTPUTS</span></span>

### <span data-ttu-id="b32ce-201">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b32ce-201">System.Boolean</span></span>

## <span data-ttu-id="b32ce-202">Пуск</span><span class="sxs-lookup"><span data-stu-id="b32ce-202">NOTES</span></span>

## <span data-ttu-id="b32ce-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b32ce-203">RELATED LINKS</span></span>