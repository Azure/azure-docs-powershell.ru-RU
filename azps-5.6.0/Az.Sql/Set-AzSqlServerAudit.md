---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8b0312ddcdce5c538b80f0245470496c534bf07f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993222"
---
# <span data-ttu-id="d6e21-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d6e21-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="d6e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6e21-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e21-103">Изменяет параметры аудита на сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d6e21-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="d6e21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6e21-104">SYNTAX</span></span>

### <span data-ttu-id="d6e21-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6e21-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e21-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6e21-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6e21-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6e21-107">DESCRIPTION</span></span>
<span data-ttu-id="d6e21-108">Чтобы изменить параметры аудита для azure SQL Server, можно настроить параметры аудита для сервера **Set-AzSqlServerAudit.**</span><span class="sxs-lookup"><span data-stu-id="d6e21-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="d6e21-109">Чтобы использовать этот cmdlet, используйте *параметры ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="d6e21-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="d6e21-110">Если хранилище BLOB-устройств является местом назначения для журналов аудита, укажите параметр *StorageAccountResourceId,* чтобы определить учетную запись хранения для журналов аудита, и *параметр StorageKeyType* для определения ключей хранения.</span><span class="sxs-lookup"><span data-stu-id="d6e21-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="d6e21-111">Вы также можете определить хранение для журналов аудита, установив значение параметра *RetentionInDays,* чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="d6e21-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6e21-112">EXAMPLES</span></span>

### <span data-ttu-id="d6e21-113">Пример 1. Политика аудита хранилища BLOB-SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d6e21-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="d6e21-114">Пример 2. Отключение политики аудита хранилища BLOB-SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d6e21-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="d6e21-115">Пример 3. Политика аудита хранилища BLOB-SQL Azure с расширенными фильтрами с использованием предика T-SQL.</span><span class="sxs-lookup"><span data-stu-id="d6e21-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="d6e21-116">Пример 4. Удаление параметра advanced filtering из политики аудита сервера Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="d6e21-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="d6e21-117">Пример 5. Политика аудита концентратора событий для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d6e21-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="d6e21-118">Пример 6. Отключение политики аудита концентратора событий для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d6e21-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="d6e21-119">Пример 7. Политика аудита аналитики журнала для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d6e21-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="d6e21-120">Пример 8. Отключение политики аудита аналитики журнала для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d6e21-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="d6e21-121">Пример 9. Отключение (через конвейер) политики аудита аналитики журналов для сервера Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d6e21-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="d6e21-122">Пример 10. Отключать отправку записей аудита сервера Azure SQL для хранения BLOB-приложений и включить отправку их для аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="d6e21-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="d6e21-123">Пример 11. Отправка записей аудита на сервере Azure SQL для хранения BLOB-сайтов, центра событий и аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="d6e21-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="d6e21-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6e21-124">PARAMETERS</span></span>

### <span data-ttu-id="d6e21-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6e21-125">-AsJob</span></span>
<span data-ttu-id="d6e21-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d6e21-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6e21-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d6e21-127">-AuditActionGroup</span></span>
<span data-ttu-id="d6e21-128">Рекомендуемый набор групп действий состоит из следующего сочетания: это позволит выполнять аудит всех запросов и хранимых процедур, выполненных в базе данных, а также успешного и неудачного входа:</span><span class="sxs-lookup"><span data-stu-id="d6e21-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="d6e21-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d6e21-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="d6e21-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d6e21-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="d6e21-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="d6e21-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="d6e21-132">Это сочетание также настроено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6e21-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="d6e21-133">Эти группы охватывают все SQL и хранимые процедуры, выполненные в базе данных, и не должны использоваться вместе с другими группами, так как это приведет к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="d6e21-134">Дополнительные сведения https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups см. в .</span><span class="sxs-lookup"><span data-stu-id="d6e21-134">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="d6e21-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="d6e21-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="d6e21-136">Указывает, является ли хранилище BLOB-хранилищ местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="d6e21-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e21-137">-DefaultProfile</span></span>
<span data-ttu-id="d6e21-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6e21-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e21-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e21-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="d6e21-140">ИД ресурса для правила авторизации концентратора событий</span><span class="sxs-lookup"><span data-stu-id="d6e21-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="d6e21-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="d6e21-141">-EventHubName</span></span>
<span data-ttu-id="d6e21-142">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="d6e21-142">The name of the event hub.</span></span> <span data-ttu-id="d6e21-143">Если при предоставлении EventHubAuthorizationRuleResourceId ничего не указано, будет выбран центр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6e21-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="d6e21-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="d6e21-144">-EventHubTargetState</span></span>
<span data-ttu-id="d6e21-145">Указывает, является ли центр событий местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="d6e21-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="d6e21-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="d6e21-147">Указывает, является ли аналитика журнала местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="d6e21-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6e21-148">-PassThru</span></span>
<span data-ttu-id="d6e21-149">Указывает, нужно ли выводить политику аудита в конце выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6e21-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="d6e21-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="d6e21-150">-PredicateExpression</span></span>
<span data-ttu-id="d6e21-151">Предика T-SQL (предложение WHERE), используемая для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="d6e21-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e21-152">-ResourceGroupName</span></span>
<span data-ttu-id="d6e21-153">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6e21-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6e21-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d6e21-154">-RetentionInDays</span></span>
<span data-ttu-id="d6e21-155">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="d6e21-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6e21-156">-ServerName</span></span>
<span data-ttu-id="d6e21-157">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d6e21-157">SQL server name.</span></span>

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

### <span data-ttu-id="d6e21-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="d6e21-158">-ServerObject</span></span>
<span data-ttu-id="d6e21-159">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-159">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="d6e21-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e21-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="d6e21-161">ИД ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d6e21-161">The storage account resource id</span></span>

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

### <span data-ttu-id="d6e21-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d6e21-162">-StorageKeyType</span></span>
<span data-ttu-id="d6e21-163">Определяет, какой из ключей доступа к хранилищу нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="d6e21-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="d6e21-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e21-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="d6e21-165">ИД рабочей области (ИД ресурса рабочей области журнала аналитики журнала) для рабочей области "Аналитика журналов", в которую вы хотите отправлять журналы аудита.</span><span class="sxs-lookup"><span data-stu-id="d6e21-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="d6e21-166">Пример: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="d6e21-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="d6e21-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6e21-167">-Confirm</span></span>
<span data-ttu-id="d6e21-168">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d6e21-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6e21-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6e21-169">-WhatIf</span></span>
<span data-ttu-id="d6e21-170">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6e21-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6e21-171">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d6e21-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6e21-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e21-172">CommonParameters</span></span>
<span data-ttu-id="d6e21-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e21-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e21-174">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6e21-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e21-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6e21-175">INPUTS</span></span>

### <span data-ttu-id="d6e21-176">System.String</span><span class="sxs-lookup"><span data-stu-id="d6e21-176">System.String</span></span>

### <span data-ttu-id="d6e21-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d6e21-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="d6e21-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="d6e21-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="d6e21-179">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d6e21-179">System.Guid</span></span>

### <span data-ttu-id="d6e21-180">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6e21-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d6e21-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="d6e21-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="d6e21-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6e21-182">OUTPUTS</span></span>

### <span data-ttu-id="d6e21-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6e21-183">System.Boolean</span></span>

## <span data-ttu-id="d6e21-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6e21-184">NOTES</span></span>

## <span data-ttu-id="d6e21-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6e21-185">RELATED LINKS</span></span>
