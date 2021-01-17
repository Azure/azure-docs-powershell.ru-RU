---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 1afa4776aa82dcfddab1709cf08dcfe8cd0ff71b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424159"
---
# <span data-ttu-id="667fa-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="667fa-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="667fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667fa-102">SYNOPSIS</span></span>
<span data-ttu-id="667fa-103">Удаляет пул спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="667fa-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="667fa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="667fa-104">SYNTAX</span></span>

### <span data-ttu-id="667fa-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="667fa-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667fa-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="667fa-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667fa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="667fa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667fa-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="667fa-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="667fa-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="667fa-109">DESCRIPTION</span></span>
<span data-ttu-id="667fa-110">**Спарклет Remove-AzSynapseSparkPool** окончательно удаляет пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="667fa-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="667fa-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="667fa-111">EXAMPLES</span></span>

### <span data-ttu-id="667fa-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="667fa-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="667fa-113">Эта команда удаляет пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="667fa-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="667fa-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="667fa-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="667fa-115">Эта команда удаляет пул спаркпарков Azure Synapse Analytics через канал.</span><span class="sxs-lookup"><span data-stu-id="667fa-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="667fa-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="667fa-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="667fa-117">Эта команда удаляет пул спаркпарков Azure Synapse Analytics через канал.</span><span class="sxs-lookup"><span data-stu-id="667fa-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="667fa-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="667fa-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="667fa-119">Эта команда удаляет пул спаркпарков Azure Synapse Analytics с ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="667fa-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="667fa-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="667fa-120">PARAMETERS</span></span>

### <span data-ttu-id="667fa-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="667fa-121">-AsJob</span></span>
<span data-ttu-id="667fa-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="667fa-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="667fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667fa-123">-DefaultProfile</span></span>
<span data-ttu-id="667fa-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="667fa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="667fa-125">-Force</span><span class="sxs-lookup"><span data-stu-id="667fa-125">-Force</span></span>
<span data-ttu-id="667fa-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="667fa-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="667fa-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="667fa-127">-InputObject</span></span>
<span data-ttu-id="667fa-128">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="667fa-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="667fa-129">-Name</span><span class="sxs-lookup"><span data-stu-id="667fa-129">-Name</span></span>
<span data-ttu-id="667fa-130">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="667fa-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667fa-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="667fa-131">-PassThru</span></span>
<span data-ttu-id="667fa-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="667fa-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="667fa-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="667fa-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="667fa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667fa-134">-ResourceGroupName</span></span>
<span data-ttu-id="667fa-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="667fa-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667fa-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="667fa-136">-ResourceId</span></span>
<span data-ttu-id="667fa-137">Идентификатор ресурса пула synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="667fa-137">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667fa-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="667fa-138">-WorkspaceName</span></span>
<span data-ttu-id="667fa-139">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="667fa-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667fa-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="667fa-140">-WorkspaceObject</span></span>
<span data-ttu-id="667fa-141">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="667fa-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="667fa-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="667fa-142">-Confirm</span></span>
<span data-ttu-id="667fa-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="667fa-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667fa-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667fa-144">-WhatIf</span></span>
<span data-ttu-id="667fa-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="667fa-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667fa-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="667fa-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667fa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667fa-147">CommonParameters</span></span>
<span data-ttu-id="667fa-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667fa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667fa-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="667fa-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667fa-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="667fa-150">INPUTS</span></span>

### <span data-ttu-id="667fa-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="667fa-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="667fa-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="667fa-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="667fa-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="667fa-153">OUTPUTS</span></span>

### <span data-ttu-id="667fa-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="667fa-154">System.Boolean</span></span>

## <span data-ttu-id="667fa-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="667fa-155">NOTES</span></span>

## <span data-ttu-id="667fa-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="667fa-156">RELATED LINKS</span></span>
