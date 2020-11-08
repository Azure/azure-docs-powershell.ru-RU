---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247139"
---
# <span data-ttu-id="6aaf0-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6aaf0-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="6aaf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6aaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="6aaf0-103">Удаление пула Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="6aaf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6aaf0-104">SYNTAX</span></span>

### <span data-ttu-id="6aaf0-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6aaf0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aaf0-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aaf0-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aaf0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aaf0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aaf0-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aaf0-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aaf0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aaf0-109">DESCRIPTION</span></span>
<span data-ttu-id="6aaf0-110">Командлет **Remove-AzSynapseSparkPool** окончательно удаляет пул Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="6aaf0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6aaf0-111">EXAMPLES</span></span>

### <span data-ttu-id="6aaf0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6aaf0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="6aaf0-113">Эта команда удаляет пул Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="6aaf0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6aaf0-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="6aaf0-115">Эта команда удаляет пул Azure Synapse Analytics Spark через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="6aaf0-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6aaf0-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="6aaf0-117">Эта команда удаляет пул Azure Synapse Analytics Spark через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="6aaf0-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6aaf0-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="6aaf0-119">Эта команда удаляет пул Azure Synapse Analytics Spark с ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="6aaf0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6aaf0-120">PARAMETERS</span></span>

### <span data-ttu-id="6aaf0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aaf0-121">-AsJob</span></span>
<span data-ttu-id="6aaf0-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6aaf0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6aaf0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aaf0-123">-DefaultProfile</span></span>
<span data-ttu-id="6aaf0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aaf0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6aaf0-125">-InputObject</span></span>
<span data-ttu-id="6aaf0-126">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-126">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6aaf0-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6aaf0-127">-Name</span></span>
<span data-ttu-id="6aaf0-128">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-128">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="6aaf0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aaf0-129">-PassThru</span></span>
<span data-ttu-id="6aaf0-130">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6aaf0-131">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6aaf0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aaf0-132">-ResourceGroupName</span></span>
<span data-ttu-id="6aaf0-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-133">Resource group name.</span></span>

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

### <span data-ttu-id="6aaf0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aaf0-134">-ResourceId</span></span>
<span data-ttu-id="6aaf0-135">Идентификатор ресурса для пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-135">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="6aaf0-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6aaf0-136">-WorkspaceName</span></span>
<span data-ttu-id="6aaf0-137">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6aaf0-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6aaf0-138">-WorkspaceObject</span></span>
<span data-ttu-id="6aaf0-139">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6aaf0-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aaf0-140">-Confirm</span></span>
<span data-ttu-id="6aaf0-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aaf0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aaf0-142">-WhatIf</span></span>
<span data-ttu-id="6aaf0-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aaf0-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aaf0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aaf0-145">CommonParameters</span></span>
<span data-ttu-id="6aaf0-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6aaf0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aaf0-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aaf0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aaf0-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6aaf0-148">INPUTS</span></span>

### <span data-ttu-id="6aaf0-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6aaf0-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6aaf0-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6aaf0-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="6aaf0-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aaf0-151">OUTPUTS</span></span>

### <span data-ttu-id="6aaf0-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6aaf0-152">System.Boolean</span></span>

## <span data-ttu-id="6aaf0-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="6aaf0-153">NOTES</span></span>

## <span data-ttu-id="6aaf0-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6aaf0-154">RELATED LINKS</span></span>
