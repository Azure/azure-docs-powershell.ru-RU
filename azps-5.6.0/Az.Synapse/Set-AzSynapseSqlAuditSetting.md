---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 15d553800aa51bdf4752902dadd8d5b15fcdf2f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992127"
---
# <span data-ttu-id="fe7e1-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="fe7e1-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="fe7e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7e1-103">Изменение параметров аудита рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="fe7e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe7e1-104">SYNTAX</span></span>

### <span data-ttu-id="fe7e1-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe7e1-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe7e1-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe7e1-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe7e1-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe7e1-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe7e1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe7e1-108">DESCRIPTION</span></span>
<span data-ttu-id="fe7e1-109">Для **параметра Set-AzSynapseSqlAuditSetting** изменяется параметры аудита рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="fe7e1-110">Если хранилище BLOB-устройств является местом назначения для журналов аудита, укажите параметр *StorageAccountResourceId,* чтобы определить учетную запись хранения для журналов аудита, и *параметр StorageKeyType* для определения ключей хранения.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="fe7e1-111">Вы также можете определить хранение для журналов аудита, установив значение параметра *RetentionInDays,* чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="fe7e1-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe7e1-112">EXAMPLES</span></span>

### <span data-ttu-id="fe7e1-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe7e1-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="fe7e1-114">В течение этого времени в рабочей области Azure Synapse Analytics Workspace ContosoWorkspace можно включить политику аудита хранилища BLOB-приложений.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fe7e1-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fe7e1-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="fe7e1-116">Отключать политику аудита хранилища BLOB-сайтов рабочей области Azure Synapse Analytics с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fe7e1-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fe7e1-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="fe7e1-118">В течение этого времени в рабочей области Azure Synapse Analytics с именем ContosoWorkspace можно включить политику аудита хранилища BLOB-SQL с использованием предиката T-SQL.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="fe7e1-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="fe7e1-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="fe7e1-120">Удалите параметры расширенных фильтров из политики аудита рабочей области Azure Synapse Analytics с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fe7e1-121">Пример 5</span><span class="sxs-lookup"><span data-stu-id="fe7e1-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="fe7e1-122">Отключать политику аудита хранилища BLOB-сайтов рабочей области Azure Synapse Analytics с именем ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="fe7e1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe7e1-123">PARAMETERS</span></span>

### <span data-ttu-id="fe7e1-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe7e1-124">-AsJob</span></span>
<span data-ttu-id="fe7e1-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fe7e1-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe7e1-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="fe7e1-126">-AuditActionGroup</span></span>
<span data-ttu-id="fe7e1-127">Рекомендуемый набор групп действий состоит из следующего сочетания: это позволит выполнять аудит всех запросов и хранимых процедур, выполненных в базе данных, а также успешного и неудачного входа:</span><span class="sxs-lookup"><span data-stu-id="fe7e1-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="fe7e1-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="fe7e1-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="fe7e1-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="fe7e1-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="fe7e1-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="fe7e1-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="fe7e1-131">Это сочетание также настроено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="fe7e1-132">Эти группы охватывают все SQL и хранимые процедуры, выполненные в базе данных, и не должны использоваться вместе с другими группами, так как это приведет к дублированию журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="fe7e1-133">Дополнительные сведения https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups см. в .</span><span class="sxs-lookup"><span data-stu-id="fe7e1-133">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="fe7e1-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="fe7e1-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="fe7e1-135">Указывает, является ли хранилище BLOB-хранилищ местом назначения для записей аудита.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="fe7e1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7e1-136">-DefaultProfile</span></span>
<span data-ttu-id="fe7e1-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe7e1-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe7e1-138">-InputObject</span></span>
<span data-ttu-id="fe7e1-139">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7e1-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe7e1-140">-PassThru</span></span>
<span data-ttu-id="fe7e1-141">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fe7e1-142">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fe7e1-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="fe7e1-143">-PredicateExpression</span></span>
<span data-ttu-id="fe7e1-144">Предика T-SQL (предложение WHERE), используемая для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="fe7e1-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe7e1-145">-ResourceGroupName</span></span>
<span data-ttu-id="fe7e1-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-146">Resource group name.</span></span>

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

### <span data-ttu-id="fe7e1-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe7e1-147">-ResourceId</span></span>
<span data-ttu-id="fe7e1-148">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="fe7e1-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="fe7e1-149">-RetentionInDays</span></span>
<span data-ttu-id="fe7e1-150">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="fe7e1-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="fe7e1-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="fe7e1-152">ИД ресурса учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="fe7e1-152">The storage account resource id</span></span>

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

### <span data-ttu-id="fe7e1-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="fe7e1-153">-StorageKeyType</span></span>
<span data-ttu-id="fe7e1-154">Определяет, какой ключ доступа к хранилищу нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="fe7e1-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fe7e1-155">-WorkspaceName</span></span>
<span data-ttu-id="fe7e1-156">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fe7e1-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe7e1-157">-Confirm</span></span>
<span data-ttu-id="fe7e1-158">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe7e1-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe7e1-159">-WhatIf</span></span>
<span data-ttu-id="fe7e1-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe7e1-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe7e1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7e1-162">CommonParameters</span></span>
<span data-ttu-id="fe7e1-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe7e1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7e1-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe7e1-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7e1-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe7e1-165">INPUTS</span></span>

### <span data-ttu-id="fe7e1-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fe7e1-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fe7e1-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe7e1-167">OUTPUTS</span></span>

### <span data-ttu-id="fe7e1-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="fe7e1-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="fe7e1-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe7e1-169">NOTES</span></span>

## <span data-ttu-id="fe7e1-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe7e1-170">RELATED LINKS</span></span>
