---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 2a81030cdf985ae338692e59d86da30cee50694f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563255"
---
# <span data-ttu-id="74c31-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="74c31-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="74c31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74c31-102">SYNOPSIS</span></span>
<span data-ttu-id="74c31-103">Изменяет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="74c31-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74c31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74c31-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74c31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74c31-105">DESCRIPTION</span></span>
<span data-ttu-id="74c31-106">Командлет **Set-AzureRmSqlServerAuditing** изменяет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="74c31-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="74c31-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="74c31-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="74c31-108">Укажите параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранилища.</span><span class="sxs-lookup"><span data-stu-id="74c31-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="74c31-109">Используйте параметр *State* для включения или отключения политики.</span><span class="sxs-lookup"><span data-stu-id="74c31-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="74c31-110">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="74c31-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="74c31-111">После успешного выполнения командлета выполняется аудит баз данных Azure SQL Server, определенных в указанном сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="74c31-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="74c31-112">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущую политику аудита BLOB-объектов, в дополнение к идентификаторам сервера.</span><span class="sxs-lookup"><span data-stu-id="74c31-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="74c31-113">Идентификаторы сервера включают, но не ограничиваются **ResourceGroupName** и **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="74c31-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="74c31-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74c31-114">EXAMPLES</span></span>

### <span data-ttu-id="74c31-115">Пример 1: Включение политики аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="74c31-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="74c31-116">Пример 2: отключение политики аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="74c31-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="74c31-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74c31-117">PARAMETERS</span></span>

### <span data-ttu-id="74c31-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="74c31-118">-AuditActionGroup</span></span>
<span data-ttu-id="74c31-119">Рекомендуемый набор групп действий: в этом случае будут проверены все запросы и хранимые процедуры, выполненные для базы данных, а также успешные и неудачные входные данные.</span><span class="sxs-lookup"><span data-stu-id="74c31-119">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="74c31-120">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="74c31-120">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="74c31-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="74c31-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="74c31-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="74c31-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="74c31-123">Это сочетание также является набором, настроенным по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="74c31-123">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="74c31-124">Эти группы охватывают все инструкции SQL и хранимые процедуры, выполненные для базы данных, и их нельзя использовать в сочетании с другими группами, так как это приводит к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="74c31-124">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="74c31-125">Дополнительные сведения можно найти в разделе https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="74c31-125">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="74c31-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c31-126">-DefaultProfile</span></span>
<span data-ttu-id="74c31-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74c31-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74c31-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74c31-128">-PassThru</span></span>
<span data-ttu-id="74c31-129">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="74c31-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="74c31-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c31-130">-ResourceGroupName</span></span>
<span data-ttu-id="74c31-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74c31-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="74c31-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="74c31-132">-RetentionInDays</span></span>
<span data-ttu-id="74c31-133">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="74c31-133">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="74c31-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="74c31-134">-ServerName</span></span>
<span data-ttu-id="74c31-135">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="74c31-135">SQL server name.</span></span>

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

### <span data-ttu-id="74c31-136">-State</span><span class="sxs-lookup"><span data-stu-id="74c31-136">-State</span></span>
<span data-ttu-id="74c31-137">Состояние политики.</span><span class="sxs-lookup"><span data-stu-id="74c31-137">The state of the policy.</span></span>

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

### <span data-ttu-id="74c31-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="74c31-138">-StorageAccountName</span></span>
<span data-ttu-id="74c31-139">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="74c31-139">The name of the storage account.</span></span> <span data-ttu-id="74c31-140">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="74c31-140">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="74c31-141">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="74c31-141">This parameter is not required.</span></span>  
<span data-ttu-id="74c31-142">Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита.</span><span class="sxs-lookup"><span data-stu-id="74c31-142">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="74c31-143">Если политика аудита не задана в первый раз и вы не указали этот параметр, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="74c31-143">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="74c31-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="74c31-144">-StorageKeyType</span></span>
<span data-ttu-id="74c31-145">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="74c31-145">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="74c31-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74c31-146">-Confirm</span></span>
<span data-ttu-id="74c31-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74c31-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c31-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c31-148">-WhatIf</span></span>
<span data-ttu-id="74c31-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74c31-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74c31-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74c31-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c31-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c31-151">CommonParameters</span></span>
<span data-ttu-id="74c31-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74c31-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c31-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c31-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c31-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74c31-154">INPUTS</span></span>

### <span data-ttu-id="74c31-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="74c31-155">None</span></span>
<span data-ttu-id="74c31-156">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="74c31-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74c31-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74c31-157">OUTPUTS</span></span>

### <span data-ttu-id="74c31-158">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="74c31-158">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="74c31-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="74c31-159">NOTES</span></span>

## <span data-ttu-id="74c31-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74c31-160">RELATED LINKS</span></span>
