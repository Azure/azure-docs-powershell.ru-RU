---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561375"
---
# <span data-ttu-id="fa505-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="fa505-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="fa505-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa505-102">SYNOPSIS</span></span>
<span data-ttu-id="fa505-103">Изменение параметров аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fa505-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa505-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa505-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa505-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa505-105">DESCRIPTION</span></span>
<span data-ttu-id="fa505-106">Командлет **Set-AzureRmSqlDatabaseAuditing** изменяет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fa505-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="fa505-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="fa505-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="fa505-108">Укажите параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранилища.</span><span class="sxs-lookup"><span data-stu-id="fa505-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="fa505-109">Используйте параметр *State* для включения или отключения политики.</span><span class="sxs-lookup"><span data-stu-id="fa505-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="fa505-110">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="fa505-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="fa505-111">После успешного выполнения командлета аудит базы данных включен.</span><span class="sxs-lookup"><span data-stu-id="fa505-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="fa505-112">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущую политику аудита BLOB-объектов, в дополнение к идентификаторам базы данных.</span><span class="sxs-lookup"><span data-stu-id="fa505-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="fa505-113">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="fa505-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="fa505-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa505-114">EXAMPLES</span></span>

### <span data-ttu-id="fa505-115">Пример 1: Включение политики аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fa505-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="fa505-116">Пример 2: отключение политики аудита больших двоичных объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fa505-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="fa505-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa505-117">PARAMETERS</span></span>

### <span data-ttu-id="fa505-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="fa505-118">-AuditAction</span></span>
<span data-ttu-id="fa505-119">Набор действий аудита.</span><span class="sxs-lookup"><span data-stu-id="fa505-119">The set of audit actions.</span></span>  
<span data-ttu-id="fa505-120">Ниже перечислены поддерживаемые действия для аудита.</span><span class="sxs-lookup"><span data-stu-id="fa505-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="fa505-121">ВЫБРАННЫЕ</span><span class="sxs-lookup"><span data-stu-id="fa505-121">SELECT</span></span>  
<span data-ttu-id="fa505-122">Обновление</span><span class="sxs-lookup"><span data-stu-id="fa505-122">UPDATE</span></span>  
<span data-ttu-id="fa505-123">ВСТАВКОЙ</span><span class="sxs-lookup"><span data-stu-id="fa505-123">INSERT</span></span>  
<span data-ttu-id="fa505-124">Удаление</span><span class="sxs-lookup"><span data-stu-id="fa505-124">DELETE</span></span>  
<span data-ttu-id="fa505-125">ВЫПОЛНЯЕТ</span><span class="sxs-lookup"><span data-stu-id="fa505-125">EXECUTE</span></span>  
<span data-ttu-id="fa505-126">ОШИБК</span><span class="sxs-lookup"><span data-stu-id="fa505-126">RECEIVE</span></span>  
<span data-ttu-id="fa505-127">Указывает</span><span class="sxs-lookup"><span data-stu-id="fa505-127">REFERENCES</span></span>  

<span data-ttu-id="fa505-128">Для определения действия, подлежащие аудиту, можно использовать общую форму:</span><span class="sxs-lookup"><span data-stu-id="fa505-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="fa505-129">транзактное ON [Object] [участник]</span><span class="sxs-lookup"><span data-stu-id="fa505-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="fa505-130">Обратите внимание, что в приведенном выше формате объект [Object] может ссылаться на объект, например на таблицу, представление или сохраненную процедуру, а также на всю базу данных или схему.</span><span class="sxs-lookup"><span data-stu-id="fa505-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="fa505-131">В последних случаях используются базы данных форм: [dbname] и SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="fa505-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="fa505-132">Например:</span><span class="sxs-lookup"><span data-stu-id="fa505-132">For example:</span></span>  
<span data-ttu-id="fa505-133">ВЫБОР на dbo. myTable по открытым</span><span class="sxs-lookup"><span data-stu-id="fa505-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="fa505-134">Выберите базу данных:: myDatabase по общедоступным</span><span class="sxs-lookup"><span data-stu-id="fa505-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="fa505-135">Выбор схемы:: mySchema по общедоступным</span><span class="sxs-lookup"><span data-stu-id="fa505-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="fa505-136">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="fa505-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="fa505-137">-AuditActionGroup</span></span>
<span data-ttu-id="fa505-138">Рекомендуемый набор групп действий: в этом случае будут проверены все запросы и хранимые процедуры, выполненные для базы данных, а также успешные и неудачные входные данные.</span><span class="sxs-lookup"><span data-stu-id="fa505-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="fa505-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="fa505-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="fa505-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="fa505-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="fa505-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="fa505-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="fa505-142">Это сочетание также является набором, настроенным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa505-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="fa505-143">Эти группы охватывают все инструкции SQL и хранимые процедуры, выполненные для базы данных, и их нельзя использовать в сочетании с другими группами, так как это приводит к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="fa505-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="fa505-144">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="fa505-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fa505-145">-DatabaseName</span></span>
<span data-ttu-id="fa505-146">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="fa505-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa505-147">-DefaultProfile</span></span>
<span data-ttu-id="fa505-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa505-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa505-149">-PassThru</span></span>
<span data-ttu-id="fa505-150">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="fa505-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa505-151">-ResourceGroupName</span></span>
<span data-ttu-id="fa505-152">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa505-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fa505-153">-RetentionInDays</span></span>
<span data-ttu-id="fa505-154">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="fa505-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-155">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fa505-155">-ServerName</span></span>
<span data-ttu-id="fa505-156">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="fa505-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-157">-State</span><span class="sxs-lookup"><span data-stu-id="fa505-157">-State</span></span>
<span data-ttu-id="fa505-158">Состояние политики.</span><span class="sxs-lookup"><span data-stu-id="fa505-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fa505-159">-StorageAccountName</span></span>
<span data-ttu-id="fa505-160">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fa505-160">The name of the storage account.</span></span> <span data-ttu-id="fa505-161">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="fa505-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="fa505-162">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fa505-162">This parameter is not required.</span></span>  
<span data-ttu-id="fa505-163">Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита.</span><span class="sxs-lookup"><span data-stu-id="fa505-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="fa505-164">Если политика аудита не задана в первый раз и вы не указали этот параметр, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="fa505-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="fa505-165">-StorageKeyType</span></span>
<span data-ttu-id="fa505-166">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="fa505-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa505-167">-Confirm</span></span>
<span data-ttu-id="fa505-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa505-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa505-169">-WhatIf</span></span>
<span data-ttu-id="fa505-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa505-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa505-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa505-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa505-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa505-172">CommonParameters</span></span>
<span data-ttu-id="fa505-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa505-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa505-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa505-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa505-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa505-175">INPUTS</span></span>

### <span data-ttu-id="fa505-176">Ничего</span><span class="sxs-lookup"><span data-stu-id="fa505-176">None</span></span>
<span data-ttu-id="fa505-177">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fa505-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa505-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa505-178">OUTPUTS</span></span>

### <span data-ttu-id="fa505-179">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="fa505-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="fa505-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa505-180">NOTES</span></span>

## <span data-ttu-id="fa505-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa505-181">RELATED LINKS</span></span>
