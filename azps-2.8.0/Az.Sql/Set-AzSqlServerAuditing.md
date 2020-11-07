---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906406"
---
# <span data-ttu-id="8aaee-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="8aaee-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="8aaee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8aaee-102">SYNOPSIS</span></span>
<span data-ttu-id="8aaee-103">**Внимание! этот командлет устарел, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) заменяет его.**</span><span class="sxs-lookup"><span data-stu-id="8aaee-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="8aaee-104">Изменяет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8aaee-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="8aaee-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8aaee-105">SYNTAX</span></span>

### <span data-ttu-id="8aaee-106">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8aaee-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aaee-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="8aaee-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8aaee-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="8aaee-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aaee-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="8aaee-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aaee-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8aaee-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aaee-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8aaee-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8aaee-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8aaee-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aaee-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8aaee-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aaee-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aaee-114">DESCRIPTION</span></span>
<span data-ttu-id="8aaee-115">Командлет **Set-AzSqlServerAuditing** изменяет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8aaee-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="8aaee-116">Чтобы использовать командлет, используйте параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="8aaee-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="8aaee-117">Назначение журналов аудита определяется указанием одного из следующих параметров переключателя: BlobStorage, LogAnalytics или EventHub (если ничего не указано, по умолчанию используется значение BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="8aaee-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="8aaee-118">Используйте параметр *State* для включения или отключения политики.</span><span class="sxs-lookup"><span data-stu-id="8aaee-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="8aaee-119">Если в качестве назначения журналов аудита задано хранилище BLOB-объектов, укажите параметр *StorageAccountName* , чтобы определить учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранения.</span><span class="sxs-lookup"><span data-stu-id="8aaee-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="8aaee-120">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="8aaee-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="8aaee-121">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущие параметры аудита в дополнение к идентификаторам сервера.</span><span class="sxs-lookup"><span data-stu-id="8aaee-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="8aaee-122">Идентификаторы сервера включают, но не ограничиваются **ResourceGroupName** и **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="8aaee-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="8aaee-123">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8aaee-123">EXAMPLES</span></span>

### <span data-ttu-id="8aaee-124">Пример 1: Включение политики аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="8aaee-125">Пример 2: отключение политики аудита хранилища BLOB-объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="8aaee-126">Пример 3: Включение политики аудита хранилища BLOB-объектов для Azure SQL Server с помощью учетной записи хранения из другой подписки</span><span class="sxs-lookup"><span data-stu-id="8aaee-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="8aaee-127">Пример 4: Включение политики аудита хранилища BLOB-объектов для Azure SQL Server с расширенной фильтрацией с помощью предиката T-SQL</span><span class="sxs-lookup"><span data-stu-id="8aaee-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="8aaee-128">Пример 5. Удаление параметра расширенной фильтрации из политики хранилища аудита больших двоичных объектов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="8aaee-129">Пример 6: Включение политики аудита центра событий для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="8aaee-130">Пример 7: отключение политики аудита центра событий для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="8aaee-131">Пример 8: Включение политики аудита анализа журналов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="8aaee-132">Пример 9: отключение политики аудита для службы анализа журналов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="8aaee-133">Пример 10: отключение через конвейер, политика аудита анализа журналов для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="8aaee-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="8aaee-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8aaee-134">PARAMETERS</span></span>

### <span data-ttu-id="8aaee-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8aaee-135">-AsJob</span></span>
<span data-ttu-id="8aaee-136">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8aaee-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8aaee-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8aaee-137">-AuditActionGroup</span></span>
<span data-ttu-id="8aaee-138">Рекомендуемый набор групп действий: в этом случае будут проверены все запросы и хранимые процедуры, выполненные для базы данных, а также успешные и неудачные входные данные.</span><span class="sxs-lookup"><span data-stu-id="8aaee-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="8aaee-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8aaee-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="8aaee-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8aaee-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="8aaee-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="8aaee-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="8aaee-142">Это сочетание также является набором, настроенным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8aaee-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="8aaee-143">Эти группы охватывают все инструкции SQL и хранимые процедуры, выполненные для базы данных, и их нельзя использовать в сочетании с другими группами, так как это приводит к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="8aaee-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="8aaee-144">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="8aaee-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="8aaee-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="8aaee-145">-BlobStorage</span></span>
<span data-ttu-id="8aaee-146">Указывает, что назначение журналов аудита — хранилище BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="8aaee-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="8aaee-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aaee-147">-DefaultProfile</span></span>
<span data-ttu-id="8aaee-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8aaee-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aaee-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8aaee-149">-EventHub</span></span>
<span data-ttu-id="8aaee-150">Указывает на то, что назначение журналов аудита является центром событий</span><span class="sxs-lookup"><span data-stu-id="8aaee-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="8aaee-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="8aaee-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="8aaee-152">Идентификатор ресурса для правила авторизации центра событий</span><span class="sxs-lookup"><span data-stu-id="8aaee-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="8aaee-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="8aaee-153">-EventHubName</span></span>
<span data-ttu-id="8aaee-154">Имя концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="8aaee-154">The name of the event hub.</span></span> <span data-ttu-id="8aaee-155">Если при предоставлении EventHubAuthorizationRuleResourceId не задано значение None, будет выбран центр событий по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8aaee-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="8aaee-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8aaee-156">-InputObject</span></span>
<span data-ttu-id="8aaee-157">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="8aaee-157">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aaee-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="8aaee-158">-LogAnalytics</span></span>
<span data-ttu-id="8aaee-159">Указывает, что назначение журналов аудита — это анализ журнала</span><span class="sxs-lookup"><span data-stu-id="8aaee-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="8aaee-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8aaee-160">-PassThru</span></span>
<span data-ttu-id="8aaee-161">Указывает, следует ли выводить политику аудита при завершении выполнения командлета</span><span class="sxs-lookup"><span data-stu-id="8aaee-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8aaee-162">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="8aaee-162">-PredicateExpression</span></span>
<span data-ttu-id="8aaee-163">Предикат T-SQL (предложение WHERE), используемый для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="8aaee-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="8aaee-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aaee-164">-ResourceGroupName</span></span>
<span data-ttu-id="8aaee-165">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8aaee-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="8aaee-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8aaee-166">-RetentionInDays</span></span>
<span data-ttu-id="8aaee-167">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="8aaee-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="8aaee-168">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="8aaee-168">-ServerName</span></span>
<span data-ttu-id="8aaee-169">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8aaee-169">SQL server name.</span></span>

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

### <span data-ttu-id="8aaee-170">-State</span><span class="sxs-lookup"><span data-stu-id="8aaee-170">-State</span></span>
<span data-ttu-id="8aaee-171">Состояние политики.</span><span class="sxs-lookup"><span data-stu-id="8aaee-171">The state of the policy.</span></span>

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

### <span data-ttu-id="8aaee-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8aaee-172">-StorageAccountName</span></span>
<span data-ttu-id="8aaee-173">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8aaee-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="8aaee-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8aaee-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="8aaee-175">Идентификатор подписки для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8aaee-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="8aaee-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8aaee-176">-StorageKeyType</span></span>
<span data-ttu-id="8aaee-177">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="8aaee-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="8aaee-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="8aaee-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="8aaee-179">ИДЕНТИФИКАТОР рабочей области (ИД ресурса) рабочей области для анализа журналов, в которую вы хотите отправлять журналы аудита.</span><span class="sxs-lookup"><span data-stu-id="8aaee-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="8aaee-180">Пример:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="8aaee-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="8aaee-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8aaee-181">-Confirm</span></span>
<span data-ttu-id="8aaee-182">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8aaee-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aaee-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aaee-183">-WhatIf</span></span>
<span data-ttu-id="8aaee-184">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8aaee-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8aaee-185">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8aaee-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aaee-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aaee-186">CommonParameters</span></span>
<span data-ttu-id="8aaee-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8aaee-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aaee-188">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aaee-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aaee-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8aaee-189">INPUTS</span></span>

### <span data-ttu-id="8aaee-190">System. String</span><span class="sxs-lookup"><span data-stu-id="8aaee-190">System.String</span></span>

### <span data-ttu-id="8aaee-191">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8aaee-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="8aaee-192">Microsoft. Azure. Commands. SQL. Audit. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="8aaee-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="8aaee-193">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8aaee-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8aaee-194">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8aaee-194">System.Guid</span></span>

### <span data-ttu-id="8aaee-195">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8aaee-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8aaee-196">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8aaee-196">OUTPUTS</span></span>

### <span data-ttu-id="8aaee-197">Microsoft. Azure. Commands. SQL. Audit. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="8aaee-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="8aaee-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="8aaee-198">NOTES</span></span>

## <span data-ttu-id="8aaee-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8aaee-199">RELATED LINKS</span></span>
