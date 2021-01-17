---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424260"
---
# <span data-ttu-id="a12e7-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a12e7-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="a12e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a12e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a12e7-103">Создает пул спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a12e7-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a12e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a12e7-104">SYNTAX</span></span>

### <span data-ttu-id="a12e7-105">CreateByNameAndEnableAutoScaleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a12e7-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12e7-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a12e7-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12e7-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a12e7-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12e7-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a12e7-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a12e7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a12e7-109">DESCRIPTION</span></span>
<span data-ttu-id="a12e7-110">Для создания пула спаркпарков Azure Synapse Analytics будет создаваться **cmdlet New-AzSynapseSparkPool.**</span><span class="sxs-lookup"><span data-stu-id="a12e7-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a12e7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a12e7-111">EXAMPLES</span></span>

### <span data-ttu-id="a12e7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a12e7-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a12e7-113">Эта команда создает пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a12e7-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="a12e7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a12e7-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a12e7-115">Эта команда создает пул спаркпарков Azure Synapse Analytics с включенной автоматическим масштабом.</span><span class="sxs-lookup"><span data-stu-id="a12e7-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="a12e7-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a12e7-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a12e7-117">Эта команда создает пул спаркпарков Azure Synapse Analytics через канал.</span><span class="sxs-lookup"><span data-stu-id="a12e7-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="a12e7-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a12e7-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="a12e7-119">Эта команда создает пул спаркпарков Azure Synapse Analytics с автоматическим масштабом в конвейере.</span><span class="sxs-lookup"><span data-stu-id="a12e7-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="a12e7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a12e7-120">PARAMETERS</span></span>

### <span data-ttu-id="a12e7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a12e7-121">-AsJob</span></span>
<span data-ttu-id="a12e7-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a12e7-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a12e7-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="a12e7-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="a12e7-124">Количество неадля в минутах.</span><span class="sxs-lookup"><span data-stu-id="a12e7-124">Number of minutes idle.</span></span> <span data-ttu-id="a12e7-125">Этот параметр должен быть указан, если включена автоматическая пауза.</span><span class="sxs-lookup"><span data-stu-id="a12e7-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="a12e7-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="a12e7-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="a12e7-127">Максимальное количество узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="a12e7-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="a12e7-128">Этот параметр должен быть указан, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="a12e7-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="a12e7-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="a12e7-130">Минимальное количество узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="a12e7-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="a12e7-131">Этот параметр должен быть указан, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="a12e7-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12e7-132">-DefaultProfile</span></span>
<span data-ttu-id="a12e7-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a12e7-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a12e7-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="a12e7-134">-EnableAutoPause</span></span>
<span data-ttu-id="a12e7-135">Указывает на то, должна ли быть включена автоматическая пауза.</span><span class="sxs-lookup"><span data-stu-id="a12e7-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="a12e7-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="a12e7-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="a12e7-137">Файл конфигурации среды ("PIP freeze" выход).</span><span class="sxs-lookup"><span data-stu-id="a12e7-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="a12e7-138">-Name</span><span class="sxs-lookup"><span data-stu-id="a12e7-138">-Name</span></span>
<span data-ttu-id="a12e7-139">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="a12e7-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="a12e7-140">-NodeCount</span></span>
<span data-ttu-id="a12e7-141">Количество узлов, которые должны быть выделены в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="a12e7-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="a12e7-142">-NodeSize</span></span>
<span data-ttu-id="a12e7-143">Количество ядра и памяти, используемых для узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="a12e7-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="a12e7-144">Этот параметр должен быть задан, если автоматическая шкала отключена.</span><span class="sxs-lookup"><span data-stu-id="a12e7-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12e7-145">-ResourceGroupName</span></span>
<span data-ttu-id="a12e7-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a12e7-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="a12e7-147">-SparkVersion</span></span>
<span data-ttu-id="a12e7-148">Версия спарк-версии Apache.</span><span class="sxs-lookup"><span data-stu-id="a12e7-148">Apache Spark version.</span></span>
<span data-ttu-id="a12e7-149">Разрешенные значения: 2,4</span><span class="sxs-lookup"><span data-stu-id="a12e7-149">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="a12e7-150">-Tag</span></span>
<span data-ttu-id="a12e7-151">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="a12e7-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="a12e7-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a12e7-152">-WorkspaceName</span></span>
<span data-ttu-id="a12e7-153">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="a12e7-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a12e7-154">-WorkspaceObject</span></span>
<span data-ttu-id="a12e7-155">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="a12e7-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a12e7-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a12e7-156">-Confirm</span></span>
<span data-ttu-id="a12e7-157">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a12e7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a12e7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a12e7-158">-WhatIf</span></span>
<span data-ttu-id="a12e7-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a12e7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a12e7-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a12e7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a12e7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12e7-161">CommonParameters</span></span>
<span data-ttu-id="a12e7-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a12e7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12e7-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a12e7-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12e7-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a12e7-164">INPUTS</span></span>

### <span data-ttu-id="a12e7-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a12e7-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a12e7-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a12e7-166">OUTPUTS</span></span>

### <span data-ttu-id="a12e7-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a12e7-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="a12e7-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a12e7-168">NOTES</span></span>

## <span data-ttu-id="a12e7-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a12e7-169">RELATED LINKS</span></span>
