---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: ec88d8ff9f5a514a3b1b5dcd9ecb917ee348b900
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323137"
---
# <span data-ttu-id="df118-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="df118-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="df118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df118-102">SYNOPSIS</span></span>
<span data-ttu-id="df118-103">Изменяет параметры аудита на сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="df118-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="df118-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df118-104">SYNTAX</span></span>

### <span data-ttu-id="df118-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df118-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df118-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df118-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df118-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df118-107">DESCRIPTION</span></span>
<span data-ttu-id="df118-108">Чтобы изменить параметры аудита для azure SQL Server, можно настроить параметры аудита для сервера **Set-AzSqlServerAudit.**</span><span class="sxs-lookup"><span data-stu-id="df118-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="df118-109">Чтобы использовать этот cmdlet, используйте *параметры ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="df118-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="df118-110">Если хранилище BLOB-устройств является местом назначения для журналов аудита, укажите параметр *StorageAccountResourceId,* чтобы определить учетную запись хранения для журналов аудита, и *параметр StorageKeyType* для определения ключей хранения.</span><span class="sxs-lookup"><span data-stu-id="df118-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="df118-111">Вы также можете определить хранение для журналов аудита, установив значение параметра *RetentionInDays,* чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="df118-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df118-112">EXAMPLES</span></span>

### <span data-ttu-id="df118-113">Пример 1. Политика аудита хранилища BLOB-SQL Azure</span><span class="sxs-lookup"><span data-stu-id="df118-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="df118-114">Пример 2. Отключение политики аудита хранилища BLOB-SQL Azure</span><span class="sxs-lookup"><span data-stu-id="df118-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="df118-115">Пример 3. Политика аудита хранилища BLOB-SQL Azure с расширенными фильтрами с использованием предиката T-SQL.</span><span class="sxs-lookup"><span data-stu-id="df118-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="df118-116">Пример 4. Удаление параметра advanced filtering из политики аудита сервера Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="df118-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="df118-117">Пример 5. Политика аудита концентратора событий для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="df118-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="df118-118">Пример 6. Отключение политики аудита концентратора событий для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="df118-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="df118-119">Пример 7. Политика аудита аналитики журнала для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="df118-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="df118-120">Пример 8. Отключение политики аудита аналитики журнала для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="df118-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="df118-121">Пример 9. Отключение (через конвейер) политики аудита аналитики журналов для сервера Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="df118-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="df118-122">Пример 10. Отключать отправку записей аудита сервера Azure SQL в хранилище BLOB-приложений и включить отправку их для аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="df118-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="df118-123">Пример 11. Отправка записей аудита на сервере Azure SQL для хранения BLOB-сайтов, центра событий и аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="df118-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="df118-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df118-124">PARAMETERS</span></span>

### <span data-ttu-id="df118-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df118-125">-AsJob</span></span>
<span data-ttu-id="df118-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="df118-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df118-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="df118-127">-AuditActionGroup</span></span>
<span data-ttu-id="df118-128">Рекомендуемый набор групп действий состоит из следующего сочетания: это позволит выполнять аудит всех запросов и хранимых процедур, выполненных в базе данных, а также успешного и неудачного входа:</span><span class="sxs-lookup"><span data-stu-id="df118-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="df118-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="df118-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="df118-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="df118-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="df118-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="df118-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="df118-132">Это сочетание также настроено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df118-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="df118-133">Эти группы охватывают все SQL и хранимые процедуры, выполненные в базе данных, и не должны использоваться вместе с другими группами, так как это приведет к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="df118-134">Дополнительные сведения https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups см. в .</span><span class="sxs-lookup"><span data-stu-id="df118-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="df118-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="df118-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="df118-136">Указывает, является ли хранилище BLOB-хранилищ местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="df118-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df118-137">-DefaultProfile</span></span>
<span data-ttu-id="df118-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df118-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df118-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="df118-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="df118-140">ИД ресурса для правила авторизации концентратора событий</span><span class="sxs-lookup"><span data-stu-id="df118-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="df118-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="df118-141">-EventHubName</span></span>
<span data-ttu-id="df118-142">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="df118-142">The name of the event hub.</span></span> <span data-ttu-id="df118-143">Если при предоставлении EventHubAuthorizationRuleResourceId отсутствует, будет выбран центр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df118-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="df118-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="df118-144">-EventHubTargetState</span></span>
<span data-ttu-id="df118-145">Указывает, является ли центр событий местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="df118-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="df118-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="df118-147">Указывает, является ли аналитика журнала назначением для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="df118-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df118-148">-PassThru</span></span>
<span data-ttu-id="df118-149">Указывает, нужно ли выводить политику аудита в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df118-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="df118-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="df118-150">-PredicateExpression</span></span>
<span data-ttu-id="df118-151">Предикат T-SQL (предложение WHERE), используемый для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="df118-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df118-152">-ResourceGroupName</span></span>
<span data-ttu-id="df118-153">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df118-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df118-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="df118-154">-RetentionInDays</span></span>
<span data-ttu-id="df118-155">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="df118-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df118-156">-ServerName</span></span>
<span data-ttu-id="df118-157">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="df118-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df118-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="df118-158">-ServerObject</span></span>
<span data-ttu-id="df118-159">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df118-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="df118-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="df118-161">ИД ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="df118-161">The storage account resource id</span></span>

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

### <span data-ttu-id="df118-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="df118-162">-StorageKeyType</span></span>
<span data-ttu-id="df118-163">Определяет, какой из ключей доступа к хранилищу нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="df118-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="df118-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="df118-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="df118-165">ИД рабочей области (ИД ресурса рабочей области журнала аналитики журнала) для рабочей области "Аналитика журналов", в которую вы хотите отправлять журналы аудита.</span><span class="sxs-lookup"><span data-stu-id="df118-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="df118-166">Пример: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="df118-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="df118-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df118-167">-Confirm</span></span>
<span data-ttu-id="df118-168">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df118-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df118-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df118-169">-WhatIf</span></span>
<span data-ttu-id="df118-170">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df118-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df118-171">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="df118-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df118-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df118-172">CommonParameters</span></span>
<span data-ttu-id="df118-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df118-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df118-174">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df118-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df118-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df118-175">INPUTS</span></span>

### <span data-ttu-id="df118-176">System.String</span><span class="sxs-lookup"><span data-stu-id="df118-176">System.String</span></span>

### <span data-ttu-id="df118-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="df118-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="df118-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="df118-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="df118-179">System.Guid</span><span class="sxs-lookup"><span data-stu-id="df118-179">System.Guid</span></span>

### <span data-ttu-id="df118-180">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="df118-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="df118-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="df118-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="df118-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df118-182">OUTPUTS</span></span>

### <span data-ttu-id="df118-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df118-183">System.Boolean</span></span>

## <span data-ttu-id="df118-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df118-184">NOTES</span></span>

## <span data-ttu-id="df118-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df118-185">RELATED LINKS</span></span>
