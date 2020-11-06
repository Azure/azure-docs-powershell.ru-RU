---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560015"
---
# <span data-ttu-id="aa8bc-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="aa8bc-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="aa8bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8bc-103">Изменение параметров аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa8bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa8bc-104">SYNTAX</span></span>

### <span data-ttu-id="aa8bc-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa8bc-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa8bc-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="aa8bc-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa8bc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa8bc-107">DESCRIPTION</span></span>
<span data-ttu-id="aa8bc-108">Командлет **Set-AzureRmSqlDatabaseAuditing** изменяет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="aa8bc-109">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="aa8bc-110">Укажите параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранилища.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="aa8bc-111">Используйте параметр *State* для включения или отключения политики.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="aa8bc-112">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="aa8bc-113">После успешного выполнения командлета аудит базы данных включен.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="aa8bc-114">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущую политику аудита BLOB-объектов, в дополнение к идентификаторам базы данных.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="aa8bc-115">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="aa8bc-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa8bc-116">EXAMPLES</span></span>

### <span data-ttu-id="aa8bc-117">Пример 1: Включение политики аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="aa8bc-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="aa8bc-118">Пример 2: отключение политики аудита больших двоичных объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="aa8bc-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="aa8bc-119">Пример 3: Включение политики аудита для базы данных Azure SQL с помощью учетной записи хранения из другой подписки</span><span class="sxs-lookup"><span data-stu-id="aa8bc-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="aa8bc-120">Пример 4: Включение расширенной политики аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="aa8bc-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="aa8bc-121">Пример 5: Удаление политики расширенной проверки для базы данных Azure SQL и установка политики аудита вместо нее.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="aa8bc-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa8bc-122">PARAMETERS</span></span>

### <span data-ttu-id="aa8bc-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="aa8bc-123">-AuditAction</span></span>
<span data-ttu-id="aa8bc-124">Набор действий аудита.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-124">The set of audit actions.</span></span>
<span data-ttu-id="aa8bc-125">Ниже перечислены действия, которые необходимо выполнить для аудита. выберите команду "Обновить" вставить команду "получить ссылки" для определения действия, подлежащие аудиту: [Action] ON [Object] BY [Principal] Обратите внимание, что [Object] в приведенном выше формате может ссылаться на объект, например на таблицу, представление или сохраненную процедуру либо на всю базу данных или схему.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="aa8bc-126">В последних случаях используются базы данных форм: [dbname] и SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="aa8bc-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="aa8bc-127">Пример: SELECT на dbo. myTable по общедоступной SELECT on база данных:: myDatabase по общедоступному SELECT On On (схема:: mySchema, Public) Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="aa8bc-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="aa8bc-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="aa8bc-128">-AuditActionGroup</span></span>
<span data-ttu-id="aa8bc-129">Рекомендуемый набор групп действий: в этом случае будут проверены все запросы и хранимые процедуры, выполненные для базы данных, а также успешные и неудачные входные данные: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" это также набор, который настроен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="aa8bc-130">Эти группы охватывают все инструкции SQL и хранимые процедуры, выполненные для базы данных, и их нельзя использовать в сочетании с другими группами, так как это приводит к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="aa8bc-131">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="aa8bc-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa8bc-132">-DatabaseName</span></span>
<span data-ttu-id="aa8bc-133">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-133">SQL Database name.</span></span>

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

### <span data-ttu-id="aa8bc-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa8bc-134">-DefaultProfile</span></span>
<span data-ttu-id="aa8bc-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa8bc-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa8bc-136">-PassThru</span></span>
<span data-ttu-id="aa8bc-137">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="aa8bc-137">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="aa8bc-138">-PredicateExpression</span></span>
<span data-ttu-id="aa8bc-139">Инструкция предложения WHERE, используемая для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="aa8bc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa8bc-140">-ResourceGroupName</span></span>
<span data-ttu-id="aa8bc-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="aa8bc-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="aa8bc-142">-RetentionInDays</span></span>
<span data-ttu-id="aa8bc-143">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-143">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-144">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="aa8bc-144">-ServerName</span></span>
<span data-ttu-id="aa8bc-145">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-145">SQL Database server name.</span></span>

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

### <span data-ttu-id="aa8bc-146">-State</span><span class="sxs-lookup"><span data-stu-id="aa8bc-146">-State</span></span>
<span data-ttu-id="aa8bc-147">Состояние политики.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-147">The state of the policy.</span></span>

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

### <span data-ttu-id="aa8bc-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa8bc-148">-StorageAccountName</span></span>
<span data-ttu-id="aa8bc-149">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-149">The name of the storage account.</span></span> <span data-ttu-id="aa8bc-150">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="aa8bc-151">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-151">This parameter is not required.</span></span>
<span data-ttu-id="aa8bc-152">Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="aa8bc-153">Если политика аудита не задана в первый раз и вы не указали этот параметр, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa8bc-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="aa8bc-155">Указывает идентификатор подписки для учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="aa8bc-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="aa8bc-156">-StorageKeyType</span></span>
<span data-ttu-id="aa8bc-157">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa8bc-158">-Confirm</span></span>
<span data-ttu-id="aa8bc-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa8bc-160">-WhatIf</span></span>
<span data-ttu-id="aa8bc-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa8bc-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa8bc-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8bc-163">CommonParameters</span></span>
<span data-ttu-id="aa8bc-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa8bc-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8bc-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa8bc-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8bc-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa8bc-166">INPUTS</span></span>

## <span data-ttu-id="aa8bc-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa8bc-167">OUTPUTS</span></span>

## <span data-ttu-id="aa8bc-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa8bc-168">NOTES</span></span>

## <span data-ttu-id="aa8bc-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa8bc-169">RELATED LINKS</span></span>
