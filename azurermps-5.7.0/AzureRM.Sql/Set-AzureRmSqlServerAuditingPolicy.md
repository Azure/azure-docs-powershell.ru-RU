---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: ee54928b1f32c726bc2847eace77e6ccbe48c4d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563252"
---
# <span data-ttu-id="869d3-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="869d3-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="869d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="869d3-102">SYNOPSIS</span></span>
<span data-ttu-id="869d3-103">Изменение политики аудита на сервере базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="869d3-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="869d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="869d3-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="869d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="869d3-105">DESCRIPTION</span></span>
<span data-ttu-id="869d3-106">Командлет **Set-AzureRmSqlServerAuditingPolicy** изменяет политику аудита на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="869d3-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="869d3-107">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита, а также параметр *StorageKeyType* , чтобы определить ключи хранения для использования.</span><span class="sxs-lookup"><span data-stu-id="869d3-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="869d3-108">Вы также можете задать хранение для таблицы Audit Logs, задав значения параметров *RetentionInDays* и *TableIdentifier* , чтобы определить период и начальное значение для имен таблиц журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="869d3-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="869d3-109">Укажите параметр *EventType* , чтобы определить типы событий для аудита.</span><span class="sxs-lookup"><span data-stu-id="869d3-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="869d3-110">После запуска этого командлета выполняется аудит баз данных, использующих политику этого сервера.</span><span class="sxs-lookup"><span data-stu-id="869d3-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="869d3-111">Если командлет завершился успешно и вы указываете параметр *PassThru* , командлет возвращает объект, который описывает текущую политику аудита и идентификаторы сервера.</span><span class="sxs-lookup"><span data-stu-id="869d3-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="869d3-112">Идентификаторы сервера включают **ResourceGroupName** и **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="869d3-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="869d3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="869d3-113">EXAMPLES</span></span>

### <span data-ttu-id="869d3-114">Пример 1: Настройка политики аудита для Azure SQL Server использование аудита таблиц</span><span class="sxs-lookup"><span data-stu-id="869d3-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="869d3-115">Эта команда задает для политики аудита сервера с именем Server01 использование учетной записи хранения с именем Storage22.</span><span class="sxs-lookup"><span data-stu-id="869d3-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="869d3-116">Пример 2: Настройка ключа учетной записи хранения для существующей политики аудита на сервере Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="869d3-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="869d3-117">Эта команда задает для политики аудита сервера с именем Server01 использование вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="869d3-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="869d3-118">Команда не изменяет имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="869d3-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="869d3-119">Пример 3: Настройка политики аудита сервера Azure SQL Server для использования определенного типа события</span><span class="sxs-lookup"><span data-stu-id="869d3-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="869d3-120">Пример 4: Настройка политики аудита для базы данных для использования аудита больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="869d3-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="869d3-121">Эта команда задает политику аудита сервера с именем Server01, чтобы использовать тип события Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="869d3-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="869d3-122">Эта команда не изменяет другие настройки.</span><span class="sxs-lookup"><span data-stu-id="869d3-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="869d3-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="869d3-123">PARAMETERS</span></span>

### <span data-ttu-id="869d3-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="869d3-124">-AuditActionGroup</span></span>
<span data-ttu-id="869d3-125">Укажите одну или несколько групп действий аудита.</span><span class="sxs-lookup"><span data-stu-id="869d3-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="869d3-126">Этот параметр применим только к аудиту больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="869d3-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="869d3-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="869d3-127">-AuditType</span></span>
<span data-ttu-id="869d3-128">Укажите тип аудита.</span><span class="sxs-lookup"><span data-stu-id="869d3-128">Specify the audit type.</span></span> <span data-ttu-id="869d3-129">Журналы аудита можно записывать в хранилище таблиц или хранилище BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="869d3-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="869d3-130">Аудит больших двоичных объектов обеспечивает более высокий уровень производительности и поддерживает аудит на уровне объектов.</span><span class="sxs-lookup"><span data-stu-id="869d3-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869d3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869d3-131">-DefaultProfile</span></span>
<span data-ttu-id="869d3-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="869d3-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="869d3-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="869d3-133">-EventType</span></span>
<span data-ttu-id="869d3-134">Указывает типы событий для аудита.</span><span class="sxs-lookup"><span data-stu-id="869d3-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="869d3-135">Этот параметр применим только к аудиту таблиц.</span><span class="sxs-lookup"><span data-stu-id="869d3-135">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="869d3-136">Вы можете указать несколько типов событий.</span><span class="sxs-lookup"><span data-stu-id="869d3-136">You can specify several event types.</span></span>
<span data-ttu-id="869d3-137">Вы можете задать аудит для всех типов событий или нет, чтобы указать, что никакие события не будут проверяться.</span><span class="sxs-lookup"><span data-stu-id="869d3-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="869d3-138">Если вы задаете значение "все" или "нет" одновременно, команда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="869d3-138">If you specify All or None at the same time, the command fails.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869d3-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="869d3-139">-PassThru</span></span>
<span data-ttu-id="869d3-140">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="869d3-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="869d3-141">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="869d3-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="869d3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="869d3-142">-ResourceGroupName</span></span>
<span data-ttu-id="869d3-143">Указывает имя группы ресурсов, содержащей базу данных.</span><span class="sxs-lookup"><span data-stu-id="869d3-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="869d3-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="869d3-144">-RetentionInDays</span></span>
<span data-ttu-id="869d3-145">Указывает количество дней хранения для таблицы журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="869d3-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="869d3-146">Нулевое значение (0) означает, что таблица не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="869d3-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="869d3-147">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="869d3-147">this is the default.</span></span>
<span data-ttu-id="869d3-148">Если вы задаете значение больше нуля, необходимо также указать значение параметра *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="869d3-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="869d3-149">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="869d3-149">-ServerName</span></span>
<span data-ttu-id="869d3-150">Указывает имя сервера, который содержит базу данных.</span><span class="sxs-lookup"><span data-stu-id="869d3-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="869d3-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="869d3-151">-StorageAccountName</span></span>
<span data-ttu-id="869d3-152">Указывает имя учетной записи хранения для аудита базы данных.</span><span class="sxs-lookup"><span data-stu-id="869d3-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="869d3-153">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="869d3-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="869d3-154">Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита базы данных.</span><span class="sxs-lookup"><span data-stu-id="869d3-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="869d3-155">Если политика аудита базы данных в первый раз определена, а этот параметр не указан, команда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="869d3-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="869d3-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="869d3-156">-StorageKeyType</span></span>
<span data-ttu-id="869d3-157">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="869d3-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="869d3-158">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="869d3-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="869d3-159">Главная</span><span class="sxs-lookup"><span data-stu-id="869d3-159">Primary</span></span>
- <span data-ttu-id="869d3-160">Запас</span><span class="sxs-lookup"><span data-stu-id="869d3-160">Secondary</span></span>

<span data-ttu-id="869d3-161">Значением по умолчанию является PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="869d3-161">The default value is Primary.</span></span>

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

### <span data-ttu-id="869d3-162">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="869d3-162">-TableIdentifier</span></span>
<span data-ttu-id="869d3-163">Указывает имя таблицы журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="869d3-163">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="869d3-164">Укажите это значение, если для параметра *RetentionInDays* задано значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="869d3-164">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="869d3-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="869d3-165">-Confirm</span></span>
<span data-ttu-id="869d3-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="869d3-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="869d3-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="869d3-167">-WhatIf</span></span>
<span data-ttu-id="869d3-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="869d3-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="869d3-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="869d3-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="869d3-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869d3-170">CommonParameters</span></span>
<span data-ttu-id="869d3-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="869d3-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869d3-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869d3-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869d3-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="869d3-173">INPUTS</span></span>

### <span data-ttu-id="869d3-174">Ничего</span><span class="sxs-lookup"><span data-stu-id="869d3-174">None</span></span>
<span data-ttu-id="869d3-175">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="869d3-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="869d3-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="869d3-176">OUTPUTS</span></span>

### <span data-ttu-id="869d3-177">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="869d3-177">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="869d3-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="869d3-178">NOTES</span></span>

## <span data-ttu-id="869d3-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="869d3-179">RELATED LINKS</span></span>

[<span data-ttu-id="869d3-180">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="869d3-180">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="869d3-181">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="869d3-181">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="869d3-182">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="869d3-182">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


