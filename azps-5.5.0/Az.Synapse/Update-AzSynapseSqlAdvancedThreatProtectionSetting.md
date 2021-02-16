---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243013"
---
# <span data-ttu-id="56667-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="56667-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="56667-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56667-102">SYNOPSIS</span></span>
<span data-ttu-id="56667-103">Обновляет дополнительные параметры защиты от угроз в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="56667-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="56667-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56667-104">SYNTAX</span></span>

### <span data-ttu-id="56667-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56667-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56667-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56667-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56667-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56667-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56667-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56667-108">DESCRIPTION</span></span>
<span data-ttu-id="56667-109">При этом в рабочей области Azure Synapse Analytics расширенные параметры защиты от угроз обновляются с использованием параметров **Update-AzSynapseSqlAdvancedThreatProtectionSetting.**</span><span class="sxs-lookup"><span data-stu-id="56667-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="56667-110">Чтобы включить в рабочей области расширенные параметры защиты от угроз, в этой рабочей области должны быть включены параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="56667-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="56667-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56667-111">EXAMPLES</span></span>

### <span data-ttu-id="56667-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56667-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="56667-113">Эта команда обновляет дополнительные параметры защиты от угроз для рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="56667-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="56667-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56667-114">PARAMETERS</span></span>

### <span data-ttu-id="56667-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56667-115">-AsJob</span></span>
<span data-ttu-id="56667-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="56667-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56667-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56667-117">-DefaultProfile</span></span>
<span data-ttu-id="56667-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56667-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56667-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="56667-119">-EmailAdmin</span></span>
<span data-ttu-id="56667-120">Определяет, следует ли отправлять сообщения администраторам электронной почты.</span><span class="sxs-lookup"><span data-stu-id="56667-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="56667-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="56667-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="56667-122">Типы обнаружения, которые нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="56667-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="56667-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56667-123">-InputObject</span></span>
<span data-ttu-id="56667-124">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="56667-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56667-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="56667-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="56667-126">Список адресов электронной почты с разделительным заст.</span><span class="sxs-lookup"><span data-stu-id="56667-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="56667-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56667-127">-ResourceGroupName</span></span>
<span data-ttu-id="56667-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56667-128">Resource group name.</span></span>

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

### <span data-ttu-id="56667-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56667-129">-ResourceId</span></span>
<span data-ttu-id="56667-130">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="56667-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="56667-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="56667-131">-RetentionInDays</span></span>
<span data-ttu-id="56667-132">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="56667-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="56667-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="56667-133">-StorageAccountName</span></span>
<span data-ttu-id="56667-134">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="56667-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="56667-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="56667-135">-WorkspaceName</span></span>
<span data-ttu-id="56667-136">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="56667-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="56667-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56667-137">-Confirm</span></span>
<span data-ttu-id="56667-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="56667-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56667-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56667-139">-WhatIf</span></span>
<span data-ttu-id="56667-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56667-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56667-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56667-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56667-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56667-142">CommonParameters</span></span>
<span data-ttu-id="56667-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56667-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56667-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56667-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56667-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56667-145">INPUTS</span></span>

### <span data-ttu-id="56667-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="56667-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="56667-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56667-147">OUTPUTS</span></span>

### <span data-ttu-id="56667-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="56667-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="56667-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56667-149">NOTES</span></span>

## <span data-ttu-id="56667-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56667-150">RELATED LINKS</span></span>
