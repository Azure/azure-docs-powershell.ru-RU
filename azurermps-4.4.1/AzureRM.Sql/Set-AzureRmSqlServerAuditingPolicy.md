---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: daec1290dfa70166e532265da98bdb507b1318e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566262"
---
# <span data-ttu-id="664a4-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="664a4-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="664a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="664a4-102">SYNOPSIS</span></span>
<span data-ttu-id="664a4-103">Изменение политики аудита на сервере базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="664a4-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="664a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="664a4-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="664a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="664a4-105">DESCRIPTION</span></span>
<span data-ttu-id="664a4-106">Командлет **Set-AzureRmSqlServerAuditingPolicy** изменяет политику аудита на сервере базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="664a4-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="664a4-107">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита, а также параметр *StorageKeyType* , чтобы определить ключи хранения для использования.</span><span class="sxs-lookup"><span data-stu-id="664a4-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="664a4-108">Вы также можете задать хранение для таблицы Audit Logs, задав значения параметров *RetentionInDays* и *TableIdentifier* , чтобы определить период и начальное значение для имен таблиц журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="664a4-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="664a4-109">Укажите параметр *EventType* , чтобы определить типы событий для аудита.</span><span class="sxs-lookup"><span data-stu-id="664a4-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="664a4-110">После запуска этого командлета выполняется аудит баз данных, использующих политику этого сервера.</span><span class="sxs-lookup"><span data-stu-id="664a4-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="664a4-111">Если командлет завершился успешно и вы указываете параметр *PassThru* , командлет возвращает объект, который описывает текущую политику аудита и идентификаторы сервера.</span><span class="sxs-lookup"><span data-stu-id="664a4-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="664a4-112">Идентификаторы сервера включают **ResourceGroupName** и **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="664a4-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="664a4-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="664a4-113">EXAMPLES</span></span>

### <span data-ttu-id="664a4-114">Пример 1: Настройка политики аудита для Azure SQL Server использование аудита таблиц</span><span class="sxs-lookup"><span data-stu-id="664a4-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="664a4-115">Эта команда задает для политики аудита сервера с именем Server01 использование учетной записи хранения с именем Storage22.</span><span class="sxs-lookup"><span data-stu-id="664a4-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="664a4-116">Пример 2: Настройка ключа учетной записи хранения для существующей политики аудита на сервере Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="664a4-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="664a4-117">Эта команда задает для политики аудита сервера с именем Server01 использование вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="664a4-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="664a4-118">Команда не изменяет имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="664a4-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="664a4-119">Пример 3: Настройка политики аудита сервера Azure SQL Server для использования определенного типа события</span><span class="sxs-lookup"><span data-stu-id="664a4-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="664a4-120">Пример 4: Настройка политики аудита для базы данных для использования аудита больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="664a4-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="664a4-121">Эта команда задает политику аудита сервера с именем Server01, чтобы использовать тип события Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="664a4-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="664a4-122">Эта команда не изменяет другие настройки.</span><span class="sxs-lookup"><span data-stu-id="664a4-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="664a4-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="664a4-123">PARAMETERS</span></span>

### <span data-ttu-id="664a4-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="664a4-124">-AuditActionGroup</span></span>
<span data-ttu-id="664a4-125">Укажите одну или несколько групп действий аудита.</span><span class="sxs-lookup"><span data-stu-id="664a4-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="664a4-126">Этот параметр применим только к аудиту больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="664a4-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="664a4-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="664a4-127">-AuditType</span></span>
<span data-ttu-id="664a4-128">Укажите тип аудита.</span><span class="sxs-lookup"><span data-stu-id="664a4-128">Specify the audit type.</span></span> <span data-ttu-id="664a4-129">Журналы аудита можно записывать в хранилище таблиц или хранилище BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="664a4-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="664a4-130">Аудит больших двоичных объектов обеспечивает более высокий уровень производительности и поддерживает аудит на уровне объектов.</span><span class="sxs-lookup"><span data-stu-id="664a4-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

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

### <span data-ttu-id="664a4-131">-EventType</span><span class="sxs-lookup"><span data-stu-id="664a4-131">-EventType</span></span>
<span data-ttu-id="664a4-132">Указывает типы событий для аудита.</span><span class="sxs-lookup"><span data-stu-id="664a4-132">Specifies the event types to audit.</span></span>
<span data-ttu-id="664a4-133">Этот параметр применим только к аудиту таблиц.</span><span class="sxs-lookup"><span data-stu-id="664a4-133">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="664a4-134">Вы можете указать несколько типов событий.</span><span class="sxs-lookup"><span data-stu-id="664a4-134">You can specify several event types.</span></span>
<span data-ttu-id="664a4-135">Вы можете задать аудит для всех типов событий или нет, чтобы указать, что никакие события не будут проверяться.</span><span class="sxs-lookup"><span data-stu-id="664a4-135">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="664a4-136">Если вы задаете значение "все" или "нет" одновременно, команда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="664a4-136">If you specify All or None at the same time, the command fails.</span></span>

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

### <span data-ttu-id="664a4-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="664a4-137">-PassThru</span></span>
<span data-ttu-id="664a4-138">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="664a4-138">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="664a4-139">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="664a4-139">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="664a4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="664a4-140">-ResourceGroupName</span></span>
<span data-ttu-id="664a4-141">Указывает имя группы ресурсов, содержащей базу данных.</span><span class="sxs-lookup"><span data-stu-id="664a4-141">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="664a4-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="664a4-142">-RetentionInDays</span></span>
<span data-ttu-id="664a4-143">Указывает количество дней хранения для таблицы журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="664a4-143">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="664a4-144">Нулевое значение (0) означает, что таблица не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="664a4-144">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="664a4-145">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="664a4-145">this is the default.</span></span>
<span data-ttu-id="664a4-146">Если вы задаете значение больше нуля, необходимо также указать значение параметра *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="664a4-146">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="664a4-147">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="664a4-147">-ServerName</span></span>
<span data-ttu-id="664a4-148">Указывает имя сервера, который содержит базу данных.</span><span class="sxs-lookup"><span data-stu-id="664a4-148">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664a4-149">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="664a4-149">-StorageAccountName</span></span>
<span data-ttu-id="664a4-150">Указывает имя учетной записи хранения для аудита базы данных.</span><span class="sxs-lookup"><span data-stu-id="664a4-150">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="664a4-151">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="664a4-151">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="664a4-152">Если этот параметр не указан, командлет использует учетную запись хранения, которая была ранее определена как часть политики аудита базы данных.</span><span class="sxs-lookup"><span data-stu-id="664a4-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="664a4-153">Если политика аудита базы данных в первый раз определена, а этот параметр не указан, команда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="664a4-153">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="664a4-154">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="664a4-154">-StorageKeyType</span></span>
<span data-ttu-id="664a4-155">Указывает, какие клавиши доступа к хранилищу следует использовать.</span><span class="sxs-lookup"><span data-stu-id="664a4-155">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="664a4-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="664a4-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="664a4-157">Главная</span><span class="sxs-lookup"><span data-stu-id="664a4-157">Primary</span></span>
- <span data-ttu-id="664a4-158">Запас</span><span class="sxs-lookup"><span data-stu-id="664a4-158">Secondary</span></span>

<span data-ttu-id="664a4-159">Значением по умолчанию является PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="664a4-159">The default value is Primary.</span></span>

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

### <span data-ttu-id="664a4-160">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="664a4-160">-TableIdentifier</span></span>
<span data-ttu-id="664a4-161">Указывает имя таблицы журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="664a4-161">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="664a4-162">Укажите это значение, если для параметра *RetentionInDays* задано значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="664a4-162">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="664a4-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="664a4-163">-Confirm</span></span>
<span data-ttu-id="664a4-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="664a4-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="664a4-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="664a4-165">-WhatIf</span></span>
<span data-ttu-id="664a4-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="664a4-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="664a4-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="664a4-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="664a4-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664a4-168">-DefaultProfile</span></span>
<span data-ttu-id="664a4-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="664a4-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="664a4-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664a4-170">CommonParameters</span></span>
<span data-ttu-id="664a4-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="664a4-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664a4-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664a4-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664a4-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="664a4-173">INPUTS</span></span>

## <span data-ttu-id="664a4-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="664a4-174">OUTPUTS</span></span>

### <span data-ttu-id="664a4-175">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="664a4-175">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="664a4-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="664a4-176">NOTES</span></span>

## <span data-ttu-id="664a4-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="664a4-177">RELATED LINKS</span></span>

[<span data-ttu-id="664a4-178">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="664a4-178">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="664a4-179">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="664a4-179">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="664a4-180">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="664a4-180">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


