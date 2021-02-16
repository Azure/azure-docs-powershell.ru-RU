---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229628"
---
# <span data-ttu-id="9c8ea-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="9c8ea-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="9c8ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8ea-103">Изменение параметров аудита для пула azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9c8ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c8ea-104">SYNTAX</span></span>

### <span data-ttu-id="9c8ea-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c8ea-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8ea-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c8ea-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8ea-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c8ea-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8ea-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c8ea-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c8ea-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c8ea-109">DESCRIPTION</span></span>
<span data-ttu-id="9c8ea-110">Для пула Azure **Synapse** Analytics SQL параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="9c8ea-111">Если хранилище BLOB-устройств является местом назначения для журналов аудита, укажите параметр *StorageAccountResourceId,* чтобы определить учетную запись хранения для журналов аудита, и *параметр StorageKeyType* для определения ключей хранения.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="9c8ea-112">Вы также можете определить хранение для журналов аудита, установив значение параметра *RetentionInDays,* чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="9c8ea-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c8ea-113">EXAMPLES</span></span>

### <span data-ttu-id="9c8ea-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c8ea-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="9c8ea-115">В течение этого времени в службе Azure Synapse Analytics можно включить политику аудита хранилища BLOB SQL с именем ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="9c8ea-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9c8ea-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="9c8ea-117">Отключать политику аудита хранилища BLOB-сайтов для пула Azure Synapse Analytics SQL ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="9c8ea-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9c8ea-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="9c8ea-119">В течение этого времени вы можете включить политику аудита хранилища BLOB-SQL пула Azure Synapse Analytics с именем ContosoSqlPool с расширенными средствами фильтрации с использованием предиктора T-SQL.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="9c8ea-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="9c8ea-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="9c8ea-121">Удалите параметры расширенных фильтров из политики аудита пула Azure Synapse Analytics SQL ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="9c8ea-122">Пример 5</span><span class="sxs-lookup"><span data-stu-id="9c8ea-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="9c8ea-123">Отключать политику аудита хранилища BLOB-сайтов для пула Azure Synapse Analytics SQL ContosoSqlPool через канал.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="9c8ea-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c8ea-124">PARAMETERS</span></span>

### <span data-ttu-id="9c8ea-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c8ea-125">-AsJob</span></span>
<span data-ttu-id="9c8ea-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9c8ea-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c8ea-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="9c8ea-127">-AuditAction</span></span>
<span data-ttu-id="9c8ea-128">Набор действий аудита.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-128">The set of audit actions.</span></span>

<span data-ttu-id="9c8ea-129">Поддерживаются такие действия:</span><span class="sxs-lookup"><span data-stu-id="9c8ea-129">The supported actions to audit are:</span></span>

<span data-ttu-id="9c8ea-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="9c8ea-130">SELECT</span></span>

<span data-ttu-id="9c8ea-131">UPDATE</span><span class="sxs-lookup"><span data-stu-id="9c8ea-131">UPDATE</span></span>

<span data-ttu-id="9c8ea-132">INSERT</span><span class="sxs-lookup"><span data-stu-id="9c8ea-132">INSERT</span></span>

<span data-ttu-id="9c8ea-133">DELETE</span><span class="sxs-lookup"><span data-stu-id="9c8ea-133">DELETE</span></span>

<span data-ttu-id="9c8ea-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="9c8ea-134">EXECUTE</span></span>

<span data-ttu-id="9c8ea-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="9c8ea-135">RECEIVE</span></span>

<span data-ttu-id="9c8ea-136">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="9c8ea-136">REFERENCES</span></span>

<span data-ttu-id="9c8ea-137">Для определения действия, который нужно проверять, существует общая форма:</span><span class="sxs-lookup"><span data-stu-id="9c8ea-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="9c8ea-138">\[action \] ON object BY \[ \] \[ principal\]</span><span class="sxs-lookup"><span data-stu-id="9c8ea-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="9c8ea-139">Обратите внимание, что объект в формате выше может ссылаться на объект, например таблицу, представление или хранимую процедуру, либо на всю базу данных \[ \] или схему.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="9c8ea-140">В последних случаях используются формы DATABASE:: \[ dbname \] и SCHEMA:: \[ schemaname \] соответственно.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="9c8ea-141">Например:</span><span class="sxs-lookup"><span data-stu-id="9c8ea-141">For example:</span></span>

<span data-ttu-id="9c8ea-142">Select on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="9c8ea-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="9c8ea-143">SELECT в database::myDatabase по общедоступным</span><span class="sxs-lookup"><span data-stu-id="9c8ea-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="9c8ea-144">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="9c8ea-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="9c8ea-145">Дополнительные сведения https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions см. в .</span><span class="sxs-lookup"><span data-stu-id="9c8ea-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="9c8ea-146">-AuditActionGroup</span></span>
<span data-ttu-id="9c8ea-147">Рекомендуемый набор групп действий состоит из следующего сочетания: это позволит выполнять аудит всех запросов и хранимых процедур, выполненных в базе данных, а также успешного и неудачного входа:</span><span class="sxs-lookup"><span data-stu-id="9c8ea-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="9c8ea-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="9c8ea-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="9c8ea-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="9c8ea-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="9c8ea-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="9c8ea-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="9c8ea-151">Это сочетание также настроено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="9c8ea-152">Эти группы охватывают все SQL и хранимые процедуры, выполненные в базе данных, и не должны использоваться вместе с другими группами, так как это приведет к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="9c8ea-153">Дополнительные сведения https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups см. в .</span><span class="sxs-lookup"><span data-stu-id="9c8ea-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="9c8ea-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="9c8ea-155">Указывает, является ли хранилище BLOB-хранилищ местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="9c8ea-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8ea-156">-DefaultProfile</span></span>
<span data-ttu-id="9c8ea-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c8ea-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c8ea-158">-InputObject</span></span>
<span data-ttu-id="9c8ea-159">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-160">-Name</span><span class="sxs-lookup"><span data-stu-id="9c8ea-160">-Name</span></span>
<span data-ttu-id="9c8ea-161">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c8ea-162">-PassThru</span></span>
<span data-ttu-id="9c8ea-163">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9c8ea-164">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9c8ea-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="9c8ea-165">-PredicateExpression</span></span>
<span data-ttu-id="9c8ea-166">Предикат T-SQL (предложение WHERE), используемый для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="9c8ea-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c8ea-167">-ResourceGroupName</span></span>
<span data-ttu-id="9c8ea-168">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-168">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c8ea-169">-ResourceId</span></span>
<span data-ttu-id="9c8ea-170">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-170">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9c8ea-171">-RetentionInDays</span></span>
<span data-ttu-id="9c8ea-172">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="9c8ea-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9c8ea-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="9c8ea-174">ИД ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9c8ea-174">The storage account resource id</span></span>

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

### <span data-ttu-id="9c8ea-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="9c8ea-175">-StorageKeyType</span></span>
<span data-ttu-id="9c8ea-176">Определяет, какой из ключей доступа к хранилищу нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="9c8ea-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9c8ea-177">-WorkspaceName</span></span>
<span data-ttu-id="9c8ea-178">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-178">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9c8ea-179">-WorkspaceObject</span></span>
<span data-ttu-id="9c8ea-180">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c8ea-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c8ea-181">-Confirm</span></span>
<span data-ttu-id="9c8ea-182">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c8ea-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c8ea-183">-WhatIf</span></span>
<span data-ttu-id="9c8ea-184">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c8ea-185">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c8ea-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8ea-186">CommonParameters</span></span>
<span data-ttu-id="9c8ea-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c8ea-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8ea-188">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c8ea-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8ea-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c8ea-189">INPUTS</span></span>

### <span data-ttu-id="9c8ea-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9c8ea-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9c8ea-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9c8ea-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9c8ea-192">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c8ea-192">OUTPUTS</span></span>

### <span data-ttu-id="9c8ea-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="9c8ea-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="9c8ea-194">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c8ea-194">NOTES</span></span>

## <span data-ttu-id="9c8ea-195">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c8ea-195">RELATED LINKS</span></span>
