---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 9afa329aae934fd713d80702dc32b402015afc8a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506476"
---
# <span data-ttu-id="7145f-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7145f-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="7145f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7145f-102">SYNOPSIS</span></span>
<span data-ttu-id="7145f-103">Изменяет параметры аудита для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7145f-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="7145f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7145f-104">SYNTAX</span></span>

### <span data-ttu-id="7145f-105">DatabaseParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7145f-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7145f-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7145f-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7145f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7145f-107">DESCRIPTION</span></span>
<span data-ttu-id="7145f-108">Для базы данных Azure SQL параметры аудита с SQL **Set-AzSqlDataBaseAudit.**</span><span class="sxs-lookup"><span data-stu-id="7145f-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="7145f-109">Чтобы использовать этот cmdlet, используйте параметры *ResourceGroupName,* *ServerName* и *DatabaseName* для определения базы данных.</span><span class="sxs-lookup"><span data-stu-id="7145f-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="7145f-110">Если хранилище BLOB-устройств является местом назначения для журналов аудита, укажите параметр *StorageAccountResourceId,* чтобы определить учетную запись хранения для журналов аудита, и *параметр StorageKeyType* для определения ключей хранения.</span><span class="sxs-lookup"><span data-stu-id="7145f-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="7145f-111">Вы также можете определить хранение для журналов аудита, установив значение параметра *RetentionInDays,* чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="7145f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7145f-112">EXAMPLES</span></span>

### <span data-ttu-id="7145f-113">Пример 1. Политика аудита хранилища BLOB-SQL Azure</span><span class="sxs-lookup"><span data-stu-id="7145f-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="7145f-114">Пример 2. Отключение политики аудита хранилища BLOB-SQL Azure</span><span class="sxs-lookup"><span data-stu-id="7145f-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="7145f-115">Пример 3. Применение политики аудита хранилища BLOB-SQL для базы данных Azure с использованием SQL предиката T-SQL.</span><span class="sxs-lookup"><span data-stu-id="7145f-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="7145f-116">Пример 4. Удаление фильтрации из политики аудита базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7145f-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="7145f-117">Пример 5. Политика аудита концентратора событий для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7145f-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="7145f-118">Пример 6. Отключение политики аудита концентратора событий для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7145f-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="7145f-119">Пример 7. Политика аудита аналитики журнала для базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7145f-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7145f-120">Пример 8. Отключение политики аудита аналитики журналов в базе данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7145f-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="7145f-121">Пример 9. Отключение (через конвейер) политики аудита аналитики журналов для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7145f-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="7145f-122">Пример 10. Отключать отправку записей аудита базы данных Azure SQL в хранилище BLOB-приложений и включить отправку их в аналитику журнала.</span><span class="sxs-lookup"><span data-stu-id="7145f-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="7145f-123">Пример 11. Отправка записей аудита базы данных Azure SQL в хранилище BLOB-приложений, центр событий и аналитику журналов.</span><span class="sxs-lookup"><span data-stu-id="7145f-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="7145f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7145f-124">PARAMETERS</span></span>

### <span data-ttu-id="7145f-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="7145f-125">-AuditAction</span></span>
<span data-ttu-id="7145f-126">Набор действий аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-126">The set of audit actions.</span></span>  
<span data-ttu-id="7145f-127">Поддерживаются такие действия:</span><span class="sxs-lookup"><span data-stu-id="7145f-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="7145f-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="7145f-128">SELECT</span></span>  
<span data-ttu-id="7145f-129">UPDATE</span><span class="sxs-lookup"><span data-stu-id="7145f-129">UPDATE</span></span>  
<span data-ttu-id="7145f-130">INSERT</span><span class="sxs-lookup"><span data-stu-id="7145f-130">INSERT</span></span>  
<span data-ttu-id="7145f-131">DELETE</span><span class="sxs-lookup"><span data-stu-id="7145f-131">DELETE</span></span>  
<span data-ttu-id="7145f-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="7145f-132">EXECUTE</span></span>  
<span data-ttu-id="7145f-133">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="7145f-133">RECEIVE</span></span>  
<span data-ttu-id="7145f-134">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="7145f-134">REFERENCES</span></span>  
<span data-ttu-id="7145f-135">Общая форма определения действия для аудита: [действие] ON [object] BY [principal] Note that [object] в формате выше может ссылаться на объект, например таблицу, представление или хранимую процедуру, либо всю базу данных или схему.</span><span class="sxs-lookup"><span data-stu-id="7145f-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="7145f-136">В последних случаях используются формы DATABASE:[dbname] и SCHEMA::[schemaname] соответственно.</span><span class="sxs-lookup"><span data-stu-id="7145f-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="7145f-137">Например:</span><span class="sxs-lookup"><span data-stu-id="7145f-137">For example:</span></span>  
<span data-ttu-id="7145f-138">Select on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="7145f-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="7145f-139">SELECT в database::myDatabase по общедоступным</span><span class="sxs-lookup"><span data-stu-id="7145f-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="7145f-140">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="7145f-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="7145f-141">Дополнительные сведения https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions см. в .</span><span class="sxs-lookup"><span data-stu-id="7145f-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="7145f-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="7145f-142">-AuditActionGroup</span></span>
<span data-ttu-id="7145f-143">Рекомендуемый набор групп действий состоит из следующего сочетания: это позволит выполнять аудит всех запросов и хранимых процедур, выполненных в базе данных, а также успешного и неудачного входа:</span><span class="sxs-lookup"><span data-stu-id="7145f-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="7145f-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7145f-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="7145f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7145f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="7145f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="7145f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="7145f-147">Это сочетание также настроено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7145f-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="7145f-148">Эти группы охватывают все SQL и хранимые процедуры, выполненные в базе данных, и не должны использоваться вместе с другими группами, так как это приведет к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="7145f-149">Дополнительные сведения https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups см. в .</span><span class="sxs-lookup"><span data-stu-id="7145f-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="7145f-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="7145f-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="7145f-151">Указывает, является ли хранилище BLOB-хранилищ местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="7145f-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7145f-152">-DatabaseName</span></span>
<span data-ttu-id="7145f-153">SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="7145f-153">SQL Database name.</span></span>

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

### <span data-ttu-id="7145f-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7145f-154">-DatabaseObject</span></span>
<span data-ttu-id="7145f-155">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="7145f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7145f-156">-DefaultProfile</span></span>
<span data-ttu-id="7145f-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7145f-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7145f-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="7145f-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="7145f-159">ИД ресурса для правила авторизации концентратора событий</span><span class="sxs-lookup"><span data-stu-id="7145f-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="7145f-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7145f-160">-EventHubName</span></span>
<span data-ttu-id="7145f-161">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="7145f-161">The name of the event hub.</span></span> <span data-ttu-id="7145f-162">Если при предоставлении EventHubAuthorizationRuleResourceId отсутствует, будет выбран центр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7145f-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="7145f-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="7145f-163">-EventHubTargetState</span></span>
<span data-ttu-id="7145f-164">Указывает, является ли центр событий местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="7145f-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="7145f-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="7145f-166">Указывает, является ли аналитика журнала местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="7145f-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7145f-167">-PassThru</span></span>
<span data-ttu-id="7145f-168">Указывает, нужно ли выводить политику аудита в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7145f-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7145f-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="7145f-169">-PredicateExpression</span></span>
<span data-ttu-id="7145f-170">Предикат T-SQL (предложение WHERE), используемый для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="7145f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7145f-171">-ResourceGroupName</span></span>
<span data-ttu-id="7145f-172">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7145f-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="7145f-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7145f-173">-RetentionInDays</span></span>
<span data-ttu-id="7145f-174">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="7145f-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7145f-175">-ServerName</span></span>
<span data-ttu-id="7145f-176">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7145f-176">SQL server name.</span></span>

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

### <span data-ttu-id="7145f-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7145f-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="7145f-178">ИД ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7145f-178">The storage account resource id</span></span>

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

### <span data-ttu-id="7145f-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7145f-179">-StorageKeyType</span></span>
<span data-ttu-id="7145f-180">Определяет, какой из ключей доступа к хранилищу нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="7145f-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="7145f-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7145f-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="7145f-182">ИД рабочей области (ИД ресурса рабочей области журнала аналитики журнала) для рабочей области "Аналитика журналов", в которую вы хотите отправлять журналы аудита.</span><span class="sxs-lookup"><span data-stu-id="7145f-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="7145f-183">Пример: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="7145f-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="7145f-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7145f-184">-Confirm</span></span>
<span data-ttu-id="7145f-185">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7145f-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7145f-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7145f-186">-WhatIf</span></span>
<span data-ttu-id="7145f-187">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7145f-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7145f-188">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7145f-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7145f-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7145f-189">CommonParameters</span></span>
<span data-ttu-id="7145f-190">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7145f-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7145f-191">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7145f-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7145f-192">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7145f-192">INPUTS</span></span>

### <span data-ttu-id="7145f-193">System.String</span><span class="sxs-lookup"><span data-stu-id="7145f-193">System.String</span></span>

### <span data-ttu-id="7145f-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7145f-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="7145f-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="7145f-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="7145f-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7145f-196">System.String[]</span></span>

### <span data-ttu-id="7145f-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7145f-197">System.Guid</span></span>

### <span data-ttu-id="7145f-198">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7145f-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7145f-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="7145f-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="7145f-200">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7145f-200">OUTPUTS</span></span>

### <span data-ttu-id="7145f-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7145f-201">System.Boolean</span></span>

## <span data-ttu-id="7145f-202">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7145f-202">NOTES</span></span>

## <span data-ttu-id="7145f-203">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7145f-203">RELATED LINKS</span></span>
