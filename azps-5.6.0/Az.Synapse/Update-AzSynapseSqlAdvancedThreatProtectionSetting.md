---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 5766c93ba1fa7434b6ebd41f0c414f5e8a9a5073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991917"
---
# <span data-ttu-id="05b87-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="05b87-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="05b87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b87-102">SYNOPSIS</span></span>
<span data-ttu-id="05b87-103">Обновляет дополнительные параметры защиты от угроз в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="05b87-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="05b87-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05b87-104">SYNTAX</span></span>

### <span data-ttu-id="05b87-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05b87-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b87-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05b87-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b87-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05b87-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05b87-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05b87-108">DESCRIPTION</span></span>
<span data-ttu-id="05b87-109">При этом в рабочей области Azure Synapse Analytics расширенные параметры защиты от угроз обновляются с использованием параметров **Update-AzSynapseSqlAdvancedThreatProtectionSetting.**</span><span class="sxs-lookup"><span data-stu-id="05b87-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="05b87-110">Чтобы включить в рабочей области расширенные возможности защиты от угроз, в этой рабочей области должны быть включены параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="05b87-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="05b87-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05b87-111">EXAMPLES</span></span>

### <span data-ttu-id="05b87-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05b87-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="05b87-113">Эта команда обновляет дополнительные параметры защиты от угроз для рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="05b87-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="05b87-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05b87-114">PARAMETERS</span></span>

### <span data-ttu-id="05b87-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05b87-115">-AsJob</span></span>
<span data-ttu-id="05b87-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="05b87-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05b87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b87-117">-DefaultProfile</span></span>
<span data-ttu-id="05b87-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05b87-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05b87-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="05b87-119">-EmailAdmin</span></span>
<span data-ttu-id="05b87-120">Определяет, следует ли отправлять сообщения администраторам электронной почты.</span><span class="sxs-lookup"><span data-stu-id="05b87-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="05b87-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="05b87-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="05b87-122">Типы обнаружения, которые нужно исключить.</span><span class="sxs-lookup"><span data-stu-id="05b87-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="05b87-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05b87-123">-InputObject</span></span>
<span data-ttu-id="05b87-124">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="05b87-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="05b87-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="05b87-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="05b87-126">Список адресов электронной почты с разделительным заст.</span><span class="sxs-lookup"><span data-stu-id="05b87-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="05b87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b87-127">-ResourceGroupName</span></span>
<span data-ttu-id="05b87-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05b87-128">Resource group name.</span></span>

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

### <span data-ttu-id="05b87-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05b87-129">-ResourceId</span></span>
<span data-ttu-id="05b87-130">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="05b87-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="05b87-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="05b87-131">-RetentionInDays</span></span>
<span data-ttu-id="05b87-132">Количество дней хранения для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="05b87-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="05b87-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05b87-133">-StorageAccountName</span></span>
<span data-ttu-id="05b87-134">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="05b87-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="05b87-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05b87-135">-WorkspaceName</span></span>
<span data-ttu-id="05b87-136">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="05b87-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="05b87-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05b87-137">-Confirm</span></span>
<span data-ttu-id="05b87-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="05b87-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b87-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b87-139">-WhatIf</span></span>
<span data-ttu-id="05b87-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05b87-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b87-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="05b87-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b87-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b87-142">CommonParameters</span></span>
<span data-ttu-id="05b87-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05b87-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b87-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05b87-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b87-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05b87-145">INPUTS</span></span>

### <span data-ttu-id="05b87-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="05b87-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="05b87-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05b87-147">OUTPUTS</span></span>

### <span data-ttu-id="05b87-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="05b87-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="05b87-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05b87-149">NOTES</span></span>

## <span data-ttu-id="05b87-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05b87-150">RELATED LINKS</span></span>
