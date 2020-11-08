---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077457"
---
# <span data-ttu-id="9e19c-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9e19c-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="9e19c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e19c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e19c-103">Обновляет пул Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9e19c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e19c-104">SYNTAX</span></span>

### <span data-ttu-id="9e19c-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e19c-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e19c-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e19c-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e19c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e19c-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e19c-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e19c-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e19c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e19c-109">DESCRIPTION</span></span>
<span data-ttu-id="9e19c-110">Командлет **Update-AzSynapseSparkPool** обновляет пул Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9e19c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e19c-111">EXAMPLES</span></span>

### <span data-ttu-id="9e19c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e19c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="9e19c-113">Эта команда обновляет пул Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="9e19c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9e19c-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="9e19c-115">Эта команда обновляет пул Azure Synapse Analytics Spark с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="9e19c-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="9e19c-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9e19c-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="9e19c-117">Эта команда обновляет пул Azure Synapse Analytics Spark с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="9e19c-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="9e19c-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="9e19c-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="9e19c-119">Эта команда обновляет пул Azure Synapse Analytics Spark с ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e19c-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="9e19c-120">Пример 5</span><span class="sxs-lookup"><span data-stu-id="9e19c-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="9e19c-121">Эта команда включает автоматическое масштабирование для пула Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="9e19c-122">Пример 6</span><span class="sxs-lookup"><span data-stu-id="9e19c-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="9e19c-123">Эта команда отключает автоматическое масштабирование для пула Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="9e19c-124">Пример 7</span><span class="sxs-lookup"><span data-stu-id="9e19c-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="9e19c-125">Эта команда включает функцию автоматического приостановки для пула Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="9e19c-126">Пример 8</span><span class="sxs-lookup"><span data-stu-id="9e19c-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="9e19c-127">Эта команда отключает функцию автоматического приостановки для пула Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="9e19c-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e19c-128">PARAMETERS</span></span>

### <span data-ttu-id="9e19c-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e19c-129">-AsJob</span></span>
<span data-ttu-id="9e19c-130">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9e19c-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e19c-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="9e19c-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="9e19c-132">Количество минут бездействия.</span><span class="sxs-lookup"><span data-stu-id="9e19c-132">Number of minutes idle.</span></span> <span data-ttu-id="9e19c-133">Этот параметр должен быть указан, если включена функция приостановки.</span><span class="sxs-lookup"><span data-stu-id="9e19c-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="9e19c-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="9e19c-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="9e19c-135">Максимальное количество узлов, которые должны быть выделены в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="9e19c-136">Этот параметр должен быть указан, если включено автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="9e19c-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="9e19c-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="9e19c-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="9e19c-138">Минимальное количество узлов, которые должны быть выделены в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="9e19c-139">Этот параметр должен быть указан, если включено автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="9e19c-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="9e19c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e19c-140">-DefaultProfile</span></span>
<span data-ttu-id="9e19c-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e19c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e19c-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="9e19c-142">-EnableAutoPause</span></span>
<span data-ttu-id="9e19c-143">Указывает, следует ли включить функцию автоматического приостановки.</span><span class="sxs-lookup"><span data-stu-id="9e19c-143">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="9e19c-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="9e19c-144">-EnableAutoScale</span></span>
<span data-ttu-id="9e19c-145">Указывает, следует ли включить автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="9e19c-145">Indicates whether Auto-scale should be enabled</span></span>

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

### <span data-ttu-id="9e19c-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e19c-146">-InputObject</span></span>
<span data-ttu-id="9e19c-147">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="9e19c-147">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e19c-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="9e19c-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="9e19c-149">Файл конфигурации среды (выводится сообщение "закрепить от PIP").</span><span class="sxs-lookup"><span data-stu-id="9e19c-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="9e19c-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e19c-150">-Name</span></span>
<span data-ttu-id="9e19c-151">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e19c-151">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9e19c-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9e19c-152">-NodeCount</span></span>
<span data-ttu-id="9e19c-153">Количество узлов, которые должны быть выделены в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="9e19c-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="9e19c-154">-NodeSize</span></span>
<span data-ttu-id="9e19c-155">Количество ядер и памяти, которые будут использоваться для узлов, выделенных в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="9e19c-156">Этот параметр должен быть указан, если отключено автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="9e19c-156">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="9e19c-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e19c-157">-ResourceGroupName</span></span>
<span data-ttu-id="9e19c-158">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e19c-158">Resource group name.</span></span>

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

### <span data-ttu-id="9e19c-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e19c-159">-ResourceId</span></span>
<span data-ttu-id="9e19c-160">Идентификатор ресурса для пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e19c-160">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9e19c-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="9e19c-161">-SparkVersion</span></span>
<span data-ttu-id="9e19c-162">Версия Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="9e19c-162">Apache Spark version.</span></span>
<span data-ttu-id="9e19c-163">Разрешенные значения: 2,4</span><span class="sxs-lookup"><span data-stu-id="9e19c-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="9e19c-164">-Тег</span><span class="sxs-lookup"><span data-stu-id="9e19c-164">-Tag</span></span>
<span data-ttu-id="9e19c-165">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="9e19c-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="9e19c-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e19c-166">-WorkspaceName</span></span>
<span data-ttu-id="9e19c-167">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9e19c-167">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e19c-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9e19c-168">-WorkspaceObject</span></span>
<span data-ttu-id="9e19c-169">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="9e19c-169">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e19c-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e19c-170">-Confirm</span></span>
<span data-ttu-id="9e19c-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e19c-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e19c-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e19c-172">-WhatIf</span></span>
<span data-ttu-id="9e19c-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e19c-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e19c-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e19c-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e19c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e19c-175">CommonParameters</span></span>
<span data-ttu-id="9e19c-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e19c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e19c-177">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e19c-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e19c-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e19c-178">INPUTS</span></span>

### <span data-ttu-id="9e19c-179">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e19c-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9e19c-180">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9e19c-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="9e19c-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e19c-181">OUTPUTS</span></span>

### <span data-ttu-id="9e19c-182">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9e19c-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="9e19c-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e19c-183">NOTES</span></span>

## <span data-ttu-id="9e19c-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e19c-184">RELATED LINKS</span></span>
