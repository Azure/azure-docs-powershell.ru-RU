---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408684"
---
# <span data-ttu-id="5a99a-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5a99a-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="5a99a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a99a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a99a-103">Обновляет пул спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a99a-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="5a99a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a99a-104">SYNTAX</span></span>

### <span data-ttu-id="5a99a-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a99a-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a99a-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a99a-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a99a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a99a-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a99a-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a99a-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a99a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a99a-109">DESCRIPTION</span></span>
<span data-ttu-id="5a99a-110">**Спарклет Update-AzSynapseSparkPool** обновляет пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a99a-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="5a99a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a99a-111">EXAMPLES</span></span>

### <span data-ttu-id="5a99a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a99a-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="5a99a-113">Эта команда обновляет пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a99a-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="5a99a-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a99a-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="5a99a-115">Эта команда обновляет пул спаркпарков Azure Synapse Analytics через канал.</span><span class="sxs-lookup"><span data-stu-id="5a99a-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="5a99a-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5a99a-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="5a99a-117">Эта команда обновляет пул спаркпарков Azure Synapse Analytics через канал.</span><span class="sxs-lookup"><span data-stu-id="5a99a-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="5a99a-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5a99a-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="5a99a-119">Эта команда обновляет пул спаркпарков Azure Synapse Analytics с помощью ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a99a-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="5a99a-120">Пример 5</span><span class="sxs-lookup"><span data-stu-id="5a99a-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="5a99a-121">Эта команда позволяет автоматически масштабировать пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a99a-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="5a99a-122">Пример 6</span><span class="sxs-lookup"><span data-stu-id="5a99a-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="5a99a-123">Эта команда отключает автоматический масштаб для пула спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a99a-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="5a99a-124">Пример 7</span><span class="sxs-lookup"><span data-stu-id="5a99a-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="5a99a-125">Эта команда позволяет автоматически приостановить пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a99a-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="5a99a-126">Пример 8</span><span class="sxs-lookup"><span data-stu-id="5a99a-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="5a99a-127">Эта команда отключает автоматическую паузу для пула спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a99a-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="5a99a-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a99a-128">PARAMETERS</span></span>

### <span data-ttu-id="5a99a-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a99a-129">-AsJob</span></span>
<span data-ttu-id="5a99a-130">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5a99a-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a99a-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="5a99a-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="5a99a-132">Количество неадля в минутах.</span><span class="sxs-lookup"><span data-stu-id="5a99a-132">Number of minutes idle.</span></span> <span data-ttu-id="5a99a-133">Этот параметр должен быть указан, если включена автоматическая пауза.</span><span class="sxs-lookup"><span data-stu-id="5a99a-133">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="5a99a-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="5a99a-135">Максимальное количество узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5a99a-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="5a99a-136">Этот параметр должен быть указан, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="5a99a-136">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="5a99a-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="5a99a-138">Минимальное количество узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5a99a-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="5a99a-139">Этот параметр должен быть указан, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="5a99a-139">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a99a-140">-DefaultProfile</span></span>
<span data-ttu-id="5a99a-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a99a-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a99a-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="5a99a-142">-EnableAutoPause</span></span>
<span data-ttu-id="5a99a-143">Указывает на то, должна ли быть включена автоматическая пауза.</span><span class="sxs-lookup"><span data-stu-id="5a99a-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="5a99a-144">-EnableAutoScale</span></span>
<span data-ttu-id="5a99a-145">Указывает на то, должна ли быть включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="5a99a-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a99a-146">-InputObject</span></span>
<span data-ttu-id="5a99a-147">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="5a99a-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="5a99a-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="5a99a-149">Файл конфигурации среды ("PIP freeze" выход).</span><span class="sxs-lookup"><span data-stu-id="5a99a-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="5a99a-150">-Name</span><span class="sxs-lookup"><span data-stu-id="5a99a-150">-Name</span></span>
<span data-ttu-id="5a99a-151">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="5a99a-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="5a99a-152">-NodeCount</span></span>
<span data-ttu-id="5a99a-153">Количество узлов, которые должны быть выделены в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5a99a-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="5a99a-154">-NodeSize</span></span>
<span data-ttu-id="5a99a-155">Количество ядра и памяти, используемых для узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5a99a-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="5a99a-156">Этот параметр должен быть задан, если автоматическая шкала отключена.</span><span class="sxs-lookup"><span data-stu-id="5a99a-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a99a-157">-ResourceGroupName</span></span>
<span data-ttu-id="5a99a-158">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a99a-158">Resource group name.</span></span>

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

### <span data-ttu-id="5a99a-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a99a-159">-ResourceId</span></span>
<span data-ttu-id="5a99a-160">Идентификатор ресурса пула synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="5a99a-160">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="5a99a-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="5a99a-161">-SparkVersion</span></span>
<span data-ttu-id="5a99a-162">Версия спарк-версии Apache.</span><span class="sxs-lookup"><span data-stu-id="5a99a-162">Apache Spark version.</span></span>
<span data-ttu-id="5a99a-163">Разрешенные значения: 2,4</span><span class="sxs-lookup"><span data-stu-id="5a99a-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="5a99a-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a99a-164">-Tag</span></span>
<span data-ttu-id="5a99a-165">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="5a99a-165">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a99a-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5a99a-166">-WorkspaceName</span></span>
<span data-ttu-id="5a99a-167">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="5a99a-167">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5a99a-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5a99a-168">-WorkspaceObject</span></span>
<span data-ttu-id="5a99a-169">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="5a99a-169">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5a99a-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a99a-170">-Confirm</span></span>
<span data-ttu-id="5a99a-171">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5a99a-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a99a-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a99a-172">-WhatIf</span></span>
<span data-ttu-id="5a99a-173">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a99a-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a99a-174">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5a99a-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a99a-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a99a-175">CommonParameters</span></span>
<span data-ttu-id="5a99a-176">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a99a-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a99a-177">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a99a-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a99a-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a99a-178">INPUTS</span></span>

### <span data-ttu-id="5a99a-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a99a-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5a99a-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5a99a-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="5a99a-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a99a-181">OUTPUTS</span></span>

### <span data-ttu-id="5a99a-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5a99a-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="5a99a-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a99a-183">NOTES</span></span>

## <span data-ttu-id="5a99a-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a99a-184">RELATED LINKS</span></span>
