---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241632"
---
# <span data-ttu-id="cfe3d-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cfe3d-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cfe3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe3d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe3d-103">Задает дополнительные параметры защиты от угроз в SQL пуле.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="cfe3d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cfe3d-104">SYNTAX</span></span>

### <span data-ttu-id="cfe3d-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cfe3d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe3d-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfe3d-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe3d-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfe3d-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe3d-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfe3d-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe3d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfe3d-109">DESCRIPTION</span></span>
<span data-ttu-id="cfe3d-110">Для пула Azure Synapse Analytics задаются дополнительные параметры защиты от угроз с SQL **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.**</span><span class="sxs-lookup"><span data-stu-id="cfe3d-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="cfe3d-111">Чтобы включить дополнительные параметры защиты от SQL, в этом SQL должны быть SQL параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="cfe3d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cfe3d-112">EXAMPLES</span></span>

### <span data-ttu-id="cfe3d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfe3d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="cfe3d-114">Эта команда задает дополнительные параметры защиты от угроз для SQL ContosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="cfe3d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfe3d-115">PARAMETERS</span></span>

### <span data-ttu-id="cfe3d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfe3d-116">-AsJob</span></span>
<span data-ttu-id="cfe3d-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cfe3d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfe3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe3d-118">-DefaultProfile</span></span>
<span data-ttu-id="cfe3d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfe3d-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="cfe3d-120">-EmailAdmin</span></span>
<span data-ttu-id="cfe3d-121">Определяет, следует ли отправлять сообщения администраторам электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="cfe3d-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="cfe3d-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="cfe3d-123">Типы обнаружения, которые нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="cfe3d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfe3d-124">-InputObject</span></span>
<span data-ttu-id="cfe3d-125">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-125">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cfe3d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cfe3d-126">-Name</span></span>
<span data-ttu-id="cfe3d-127">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-127">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="cfe3d-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="cfe3d-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="cfe3d-129">Список адресов электронной почты с разделительным заст.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="cfe3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="cfe3d-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-131">Resource group name.</span></span>

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

### <span data-ttu-id="cfe3d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfe3d-132">-ResourceId</span></span>
<span data-ttu-id="cfe3d-133">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="cfe3d-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cfe3d-134">-RetentionInDays</span></span>
<span data-ttu-id="cfe3d-135">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="cfe3d-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cfe3d-136">-StorageAccountName</span></span>
<span data-ttu-id="cfe3d-137">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="cfe3d-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cfe3d-138">-WorkspaceName</span></span>
<span data-ttu-id="cfe3d-139">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cfe3d-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cfe3d-140">-WorkspaceObject</span></span>
<span data-ttu-id="cfe3d-141">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cfe3d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfe3d-142">-Confirm</span></span>
<span data-ttu-id="cfe3d-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe3d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe3d-144">-WhatIf</span></span>
<span data-ttu-id="cfe3d-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe3d-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe3d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe3d-147">CommonParameters</span></span>
<span data-ttu-id="cfe3d-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe3d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe3d-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfe3d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe3d-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfe3d-150">INPUTS</span></span>

### <span data-ttu-id="cfe3d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cfe3d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cfe3d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cfe3d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="cfe3d-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cfe3d-153">OUTPUTS</span></span>

### <span data-ttu-id="cfe3d-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="cfe3d-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="cfe3d-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cfe3d-155">NOTES</span></span>

## <span data-ttu-id="cfe3d-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfe3d-156">RELATED LINKS</span></span>
