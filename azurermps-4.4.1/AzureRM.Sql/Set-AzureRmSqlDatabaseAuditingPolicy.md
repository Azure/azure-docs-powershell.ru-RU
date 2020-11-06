---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559428"
---
# <span data-ttu-id="5398a-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="5398a-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="5398a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5398a-102">SYNOPSIS</span></span>
<span data-ttu-id="5398a-103">Задает политику аудита для базы данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5398a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5398a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5398a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5398a-105">DESCRIPTION</span></span>
<span data-ttu-id="5398a-106">Командлет **Set-AzureRmSqlDatabaseAuditingPolicy** изменяет политику аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5398a-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="5398a-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="5398a-108">Укажите параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранилища.</span><span class="sxs-lookup"><span data-stu-id="5398a-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="5398a-109">Вы также можете задать хранение для таблицы Audit Logs, задав значения параметров *RetentionInDays* и *TableIdentifier* , чтобы определить период и начальное значение для имен таблиц журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="5398a-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="5398a-110">Укажите параметр *EventType* , чтобы определить типы событий для аудита.</span><span class="sxs-lookup"><span data-stu-id="5398a-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="5398a-111">После успешного выполнения командлета аудит базы данных включен.</span><span class="sxs-lookup"><span data-stu-id="5398a-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="5398a-112">Если база данных использовала политику сервера для аудита перед выполнением этого командлета, аудит перестает использовать эту политику.</span><span class="sxs-lookup"><span data-stu-id="5398a-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="5398a-113">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, который описывает текущую политику аудита в дополнение к идентификаторам базы данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="5398a-114">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="5398a-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="5398a-115">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="5398a-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5398a-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5398a-116">EXAMPLES</span></span>

### <span data-ttu-id="5398a-117">Пример 1: Настройка политики аудита базы данных для использования аудита таблиц</span><span class="sxs-lookup"><span data-stu-id="5398a-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="5398a-118">Эта команда задает политику аудита для базы данных с именем Database01, расположенную в Server01, чтобы использовать учетную запись хранения с именем Storage31.</span><span class="sxs-lookup"><span data-stu-id="5398a-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="5398a-119">Пример 2: Настройка ключа учетной записи хранения для существующей политики аудита базы данных</span><span class="sxs-lookup"><span data-stu-id="5398a-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="5398a-120">Эта команда задает политику аудита для базы данных с именем Database01, расположенную на Server01, чтобы использовать ту же учетную запись хранения, но теперь для использования вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="5398a-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="5398a-121">Пример 3: Настройка политики аудита для базы данных для использования определенного типа события</span><span class="sxs-lookup"><span data-stu-id="5398a-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="5398a-122">Пример 4: Настройка политики аудита для базы данных для использования аудита больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="5398a-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="5398a-123">Эта команда задает политику аудита для базы данных с именем Database01, расположенную на Server01.</span><span class="sxs-lookup"><span data-stu-id="5398a-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="5398a-124">Политика заносит в журнал Login_Failure тип события.</span><span class="sxs-lookup"><span data-stu-id="5398a-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="5398a-125">Команда не изменяет параметры хранилища.</span><span class="sxs-lookup"><span data-stu-id="5398a-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="5398a-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5398a-126">PARAMETERS</span></span>

### <span data-ttu-id="5398a-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="5398a-127">-AuditAction</span></span>
<span data-ttu-id="5398a-128">Укажите один или несколько действий аудита.</span><span class="sxs-lookup"><span data-stu-id="5398a-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="5398a-129">Этот параметр применим только к аудиту больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="5398a-129">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="5398a-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="5398a-130">-AuditActionGroup</span></span>
<span data-ttu-id="5398a-131">Укажите одну или несколько групп действий аудита.</span><span class="sxs-lookup"><span data-stu-id="5398a-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="5398a-132">Этот параметр применим только к аудиту больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="5398a-132">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="5398a-133">-AuditType</span><span class="sxs-lookup"><span data-stu-id="5398a-133">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5398a-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5398a-134">-DatabaseName</span></span>
<span data-ttu-id="5398a-135">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-135">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5398a-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="5398a-136">-EventType</span></span>
<span data-ttu-id="5398a-137">Указывает типы событий для аудита.</span><span class="sxs-lookup"><span data-stu-id="5398a-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="5398a-138">Этот параметр применим только к аудиту таблиц.</span><span class="sxs-lookup"><span data-stu-id="5398a-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="5398a-139">Вы можете указать несколько типов событий.</span><span class="sxs-lookup"><span data-stu-id="5398a-139">You can specify several event types.</span></span>
<span data-ttu-id="5398a-140">Вы можете задать аудит для всех типов событий или нет, чтобы указать, что никакие события не будут проверяться.</span><span class="sxs-lookup"><span data-stu-id="5398a-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="5398a-141">Если вы укажете "все" или "нет" одновременно, командлет не запустится.</span><span class="sxs-lookup"><span data-stu-id="5398a-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5398a-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5398a-142">-PassThru</span></span>
<span data-ttu-id="5398a-143">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5398a-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5398a-144">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5398a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5398a-145">-ResourceGroupName</span></span>
<span data-ttu-id="5398a-146">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5398a-147">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5398a-147">-RetentionInDays</span></span>
<span data-ttu-id="5398a-148">Указывает количество дней хранения для таблицы журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="5398a-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="5398a-149">Нулевое значение (0) означает, что таблица не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="5398a-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="5398a-150">Значением по умолчанию является нуль.</span><span class="sxs-lookup"><span data-stu-id="5398a-150">The default value is zero.</span></span>
<span data-ttu-id="5398a-151">Если вы задаете значение больше нуля, необходимо указать значение для параметра *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="5398a-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="5398a-152">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5398a-152">-ServerName</span></span>
<span data-ttu-id="5398a-153">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5398a-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5398a-154">-StorageAccountName</span></span>
<span data-ttu-id="5398a-155">Указывает имя учетной записи хранения для аудита базы данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="5398a-156">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="5398a-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="5398a-157">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5398a-157">This parameter is not required.</span></span>
<span data-ttu-id="5398a-158">Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита базы данных.</span><span class="sxs-lookup"><span data-stu-id="5398a-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="5398a-159">Если политика аудита базы данных впервые определена и вы не указали этот параметр, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="5398a-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="5398a-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="5398a-160">-StorageKeyType</span></span>
<span data-ttu-id="5398a-161">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="5398a-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="5398a-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5398a-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5398a-163">Главная</span><span class="sxs-lookup"><span data-stu-id="5398a-163">Primary</span></span>
- <span data-ttu-id="5398a-164">Запас</span><span class="sxs-lookup"><span data-stu-id="5398a-164">Secondary</span></span>

<span data-ttu-id="5398a-165">Значением по умолчанию является PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="5398a-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="5398a-166">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="5398a-166">-TableIdentifier</span></span>
<span data-ttu-id="5398a-167">Указывает имя таблицы журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="5398a-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="5398a-168">Укажите это значение, если для параметра *RetentionInDays* задано значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="5398a-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="5398a-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5398a-169">-Confirm</span></span>
<span data-ttu-id="5398a-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5398a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5398a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5398a-171">-WhatIf</span></span>
<span data-ttu-id="5398a-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5398a-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5398a-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5398a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5398a-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5398a-174">-DefaultProfile</span></span>
<span data-ttu-id="5398a-175">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5398a-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5398a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5398a-176">CommonParameters</span></span>
<span data-ttu-id="5398a-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5398a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5398a-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5398a-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5398a-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5398a-179">INPUTS</span></span>

## <span data-ttu-id="5398a-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5398a-180">OUTPUTS</span></span>

### <span data-ttu-id="5398a-181">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5398a-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="5398a-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="5398a-182">NOTES</span></span>

## <span data-ttu-id="5398a-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5398a-183">RELATED LINKS</span></span>

[<span data-ttu-id="5398a-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="5398a-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="5398a-185">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="5398a-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="5398a-186">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5398a-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


