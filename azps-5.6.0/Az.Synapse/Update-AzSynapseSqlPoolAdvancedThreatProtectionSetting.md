---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 2267f9420e545fd693b734aaf8f90e89cce000a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994731"
---
# <span data-ttu-id="98ffa-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="98ffa-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="98ffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="98ffa-103">Задает дополнительные параметры защиты от угроз в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="98ffa-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="98ffa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98ffa-104">SYNTAX</span></span>

### <span data-ttu-id="98ffa-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98ffa-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ffa-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98ffa-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ffa-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98ffa-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ffa-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98ffa-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ffa-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98ffa-109">DESCRIPTION</span></span>
<span data-ttu-id="98ffa-110">Для пула Azure Synapse Analytics задаются дополнительные параметры защиты от угроз с SQL **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.**</span><span class="sxs-lookup"><span data-stu-id="98ffa-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="98ffa-111">Чтобы включить дополнительные параметры защиты от SQL, в этом SQL должны быть SQL параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="98ffa-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="98ffa-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98ffa-112">EXAMPLES</span></span>

### <span data-ttu-id="98ffa-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98ffa-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="98ffa-114">Эта команда задает дополнительные параметры защиты от угроз для SQL ContosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="98ffa-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="98ffa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98ffa-115">PARAMETERS</span></span>

### <span data-ttu-id="98ffa-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98ffa-116">-AsJob</span></span>
<span data-ttu-id="98ffa-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="98ffa-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98ffa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ffa-118">-DefaultProfile</span></span>
<span data-ttu-id="98ffa-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98ffa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98ffa-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="98ffa-120">-EmailAdmin</span></span>
<span data-ttu-id="98ffa-121">Определяет, следует ли отправлять сообщения администраторам электронной почты.</span><span class="sxs-lookup"><span data-stu-id="98ffa-121">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="98ffa-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="98ffa-123">Типы обнаружения, которые нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="98ffa-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="98ffa-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98ffa-124">-InputObject</span></span>
<span data-ttu-id="98ffa-125">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="98ffa-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-126">-Name</span><span class="sxs-lookup"><span data-stu-id="98ffa-126">-Name</span></span>
<span data-ttu-id="98ffa-127">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="98ffa-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="98ffa-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="98ffa-129">Список адресов электронной почты с разделительным заст.</span><span class="sxs-lookup"><span data-stu-id="98ffa-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ffa-130">-ResourceGroupName</span></span>
<span data-ttu-id="98ffa-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98ffa-131">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ffa-132">-ResourceId</span></span>
<span data-ttu-id="98ffa-133">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="98ffa-133">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="98ffa-134">-RetentionInDays</span></span>
<span data-ttu-id="98ffa-135">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="98ffa-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="98ffa-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="98ffa-136">-StorageAccountName</span></span>
<span data-ttu-id="98ffa-137">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="98ffa-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="98ffa-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98ffa-138">-WorkspaceName</span></span>
<span data-ttu-id="98ffa-139">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="98ffa-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="98ffa-140">-WorkspaceObject</span></span>
<span data-ttu-id="98ffa-141">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="98ffa-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98ffa-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98ffa-142">-Confirm</span></span>
<span data-ttu-id="98ffa-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="98ffa-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ffa-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ffa-144">-WhatIf</span></span>
<span data-ttu-id="98ffa-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98ffa-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98ffa-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="98ffa-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ffa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ffa-147">CommonParameters</span></span>
<span data-ttu-id="98ffa-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ffa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ffa-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98ffa-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ffa-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98ffa-150">INPUTS</span></span>

### <span data-ttu-id="98ffa-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="98ffa-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="98ffa-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="98ffa-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="98ffa-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98ffa-153">OUTPUTS</span></span>

### <span data-ttu-id="98ffa-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="98ffa-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="98ffa-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98ffa-155">NOTES</span></span>

## <span data-ttu-id="98ffa-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98ffa-156">RELATED LINKS</span></span>
