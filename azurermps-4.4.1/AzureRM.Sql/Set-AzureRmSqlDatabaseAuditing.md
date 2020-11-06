---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563840"
---
# <span data-ttu-id="c8dc7-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="c8dc7-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="c8dc7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="c8dc7-103">Изменение параметров аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8dc7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8dc7-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8dc7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="c8dc7-106">Командлет **Set-AzureRmSqlDatabaseAuditing** изменяет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="c8dc7-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c8dc7-108">Укажите параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранилища.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="c8dc7-109">Используйте параметр *State* для включения или отключения политики.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="c8dc7-110">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="c8dc7-111">После успешного выполнения командлета аудит базы данных включен.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="c8dc7-112">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущую политику аудита BLOB-объектов, в дополнение к идентификаторам базы данных.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="c8dc7-113">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="c8dc7-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8dc7-114">EXAMPLES</span></span>

### <span data-ttu-id="c8dc7-115">Пример 1: Включение политики аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c8dc7-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="c8dc7-116">Пример 2: отключение политики аудита больших двоичных объектов для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="c8dc7-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="c8dc7-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8dc7-117">PARAMETERS</span></span>

### <span data-ttu-id="c8dc7-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="c8dc7-118">-AuditAction</span></span>
<span data-ttu-id="c8dc7-119">Набор действий аудита</span><span class="sxs-lookup"><span data-stu-id="c8dc7-119">The set of the audit actions</span></span>

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

### <span data-ttu-id="c8dc7-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="c8dc7-120">-AuditActionGroup</span></span>
<span data-ttu-id="c8dc7-121">Набор групп действий аудита</span><span class="sxs-lookup"><span data-stu-id="c8dc7-121">The set of the audit action groups</span></span>

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

### <span data-ttu-id="c8dc7-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8dc7-122">-DatabaseName</span></span>
<span data-ttu-id="c8dc7-123">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-123">SQL Database name.</span></span>

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

### <span data-ttu-id="c8dc7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8dc7-124">-PassThru</span></span>
<span data-ttu-id="c8dc7-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="c8dc7-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c8dc7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8dc7-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8dc7-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8dc7-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c8dc7-128">-RetentionInDays</span></span>
<span data-ttu-id="c8dc7-129">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="c8dc7-129">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="c8dc7-130">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c8dc7-130">-ServerName</span></span>
<span data-ttu-id="c8dc7-131">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-131">SQL Database server name.</span></span>

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

### <span data-ttu-id="c8dc7-132">-State</span><span class="sxs-lookup"><span data-stu-id="c8dc7-132">-State</span></span>
<span data-ttu-id="c8dc7-133">Состояние политики аудита</span><span class="sxs-lookup"><span data-stu-id="c8dc7-133">The state of the auditing policy</span></span>

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

### <span data-ttu-id="c8dc7-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8dc7-134">-StorageAccountName</span></span>
<span data-ttu-id="c8dc7-135">Имя учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c8dc7-135">The name of the storage account</span></span>

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

### <span data-ttu-id="c8dc7-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="c8dc7-136">-StorageKeyType</span></span>
<span data-ttu-id="c8dc7-137">Тип ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="c8dc7-137">The type of the storage key</span></span>

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

### <span data-ttu-id="c8dc7-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8dc7-138">-Confirm</span></span>
<span data-ttu-id="c8dc7-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8dc7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8dc7-140">-WhatIf</span></span>
<span data-ttu-id="c8dc7-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8dc7-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8dc7-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8dc7-143">-DefaultProfile</span></span>
<span data-ttu-id="c8dc7-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8dc7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8dc7-145">CommonParameters</span></span>
<span data-ttu-id="c8dc7-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8dc7-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8dc7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8dc7-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8dc7-148">INPUTS</span></span>

## <span data-ttu-id="c8dc7-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8dc7-149">OUTPUTS</span></span>

### <span data-ttu-id="c8dc7-150">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="c8dc7-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="c8dc7-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8dc7-151">NOTES</span></span>

## <span data-ttu-id="c8dc7-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8dc7-152">RELATED LINKS</span></span>

