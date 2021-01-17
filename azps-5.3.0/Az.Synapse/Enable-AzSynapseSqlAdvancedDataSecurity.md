---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424567"
---
# <span data-ttu-id="bd192-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="bd192-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="bd192-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd192-102">SYNOPSIS</span></span>
<span data-ttu-id="bd192-103">Включает расширенные возможности безопасности данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bd192-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="bd192-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd192-104">SYNTAX</span></span>

### <span data-ttu-id="bd192-105">EnableByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd192-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd192-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd192-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd192-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd192-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd192-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd192-108">DESCRIPTION</span></span>
<span data-ttu-id="bd192-109">С помощью cmdlet **Enable-AzSynapseSqlAdvancedDataSecurity** можно включить в рабочей области расширенные возможности безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="bd192-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="bd192-110">Advanced Data Security — это единый пакет обеспечения безопасности, который включает в себя классификацию данных, оценку уязвимости и Advanced Threat Protection для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bd192-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="bd192-111">(Для сохранения оценок уязвимости будет автоматически создана новая учетная запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bd192-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="bd192-112">Если для этой цели ранее была создана учетная запись хранения, она будет использоваться вместо нее)</span><span class="sxs-lookup"><span data-stu-id="bd192-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="bd192-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd192-113">EXAMPLES</span></span>

### <span data-ttu-id="bd192-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd192-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="bd192-115">Эта команда обеспечивает в рабочей области расширенные возможности безопасности данных.</span><span class="sxs-lookup"><span data-stu-id="bd192-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="bd192-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd192-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="bd192-117">Эта команда обеспечивает в рабочей области расширенные возможности защиты данных в конвейере.</span><span class="sxs-lookup"><span data-stu-id="bd192-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="bd192-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bd192-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="bd192-119">Эта команда включает в рабочей области расширенные возможности защиты данных (pipeline) и не включает автоматически оценку уязвимости.</span><span class="sxs-lookup"><span data-stu-id="bd192-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="bd192-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd192-120">PARAMETERS</span></span>

### <span data-ttu-id="bd192-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd192-121">-AsJob</span></span>
<span data-ttu-id="bd192-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bd192-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd192-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd192-123">-DefaultProfile</span></span>
<span data-ttu-id="bd192-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd192-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd192-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bd192-125">-DeploymentName</span></span>
<span data-ttu-id="bd192-126">Задай пользовательское имя для развертывания Advanced Data Security.</span><span class="sxs-lookup"><span data-stu-id="bd192-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="bd192-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="bd192-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="bd192-128">Не ввайте автоматически встраивайте оценку уязвимости (при этом учетная запись хранения не создается).</span><span class="sxs-lookup"><span data-stu-id="bd192-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="bd192-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd192-129">-InputObject</span></span>
<span data-ttu-id="bd192-130">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="bd192-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd192-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd192-131">-ResourceGroupName</span></span>
<span data-ttu-id="bd192-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd192-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd192-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd192-133">-ResourceId</span></span>
<span data-ttu-id="bd192-134">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="bd192-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd192-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd192-135">-WorkspaceName</span></span>
<span data-ttu-id="bd192-136">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="bd192-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd192-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd192-137">-Confirm</span></span>
<span data-ttu-id="bd192-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bd192-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd192-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd192-139">-WhatIf</span></span>
<span data-ttu-id="bd192-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd192-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd192-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd192-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd192-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd192-142">CommonParameters</span></span>
<span data-ttu-id="bd192-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd192-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd192-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd192-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd192-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd192-145">INPUTS</span></span>

### <span data-ttu-id="bd192-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd192-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bd192-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd192-147">OUTPUTS</span></span>

### <span data-ttu-id="bd192-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="bd192-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="bd192-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd192-149">NOTES</span></span>

## <span data-ttu-id="bd192-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd192-150">RELATED LINKS</span></span>
