---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415639"
---
# <span data-ttu-id="5d0b9-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5d0b9-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="5d0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0b9-103">Создает пул спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="5d0b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d0b9-104">SYNTAX</span></span>

### <span data-ttu-id="5d0b9-105">CreateByNameAndEnableAutoScaleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d0b9-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d0b9-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d0b9-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d0b9-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d0b9-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d0b9-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d0b9-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d0b9-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d0b9-109">DESCRIPTION</span></span>
<span data-ttu-id="5d0b9-110">Для создания пула спаркпарков Azure Synapse Analytics будет создаваться **cmdlet New-AzSynapseSparkPool.**</span><span class="sxs-lookup"><span data-stu-id="5d0b9-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="5d0b9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d0b9-111">EXAMPLES</span></span>

### <span data-ttu-id="5d0b9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d0b9-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="5d0b9-113">Эта команда создает пул спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="5d0b9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5d0b9-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="5d0b9-115">Эта команда создает пул спаркпарков Azure Synapse Analytics с включенной автоматическим масштабом.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="5d0b9-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5d0b9-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="5d0b9-117">Эта команда создает пул спаркпарков Azure Synapse Analytics через канал.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="5d0b9-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5d0b9-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="5d0b9-119">Эта команда создает пул спаркпарков Azure Synapse Analytics с автоматическим масштабом в конвейере.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="5d0b9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d0b9-120">PARAMETERS</span></span>

### <span data-ttu-id="5d0b9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d0b9-121">-AsJob</span></span>
<span data-ttu-id="5d0b9-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5d0b9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d0b9-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="5d0b9-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="5d0b9-124">Количество неавиваиваемого времени (в минутах).</span><span class="sxs-lookup"><span data-stu-id="5d0b9-124">Number of minutes idle.</span></span> <span data-ttu-id="5d0b9-125">Этот параметр должен быть задан, если включена автоматическая пауза.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="5d0b9-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="5d0b9-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="5d0b9-127">Максимальное количество узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="5d0b9-128">Этот параметр должен быть указан, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="5d0b9-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="5d0b9-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="5d0b9-130">Минимальное количество узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="5d0b9-131">Этот параметр должен быть указан, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="5d0b9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d0b9-132">-DefaultProfile</span></span>
<span data-ttu-id="5d0b9-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d0b9-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="5d0b9-134">-EnableAutoPause</span></span>
<span data-ttu-id="5d0b9-135">Указывает на то, должна ли быть включена автоматическая пауза.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="5d0b9-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="5d0b9-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="5d0b9-137">Файл конфигурации среды ("PIP freeze" выход).</span><span class="sxs-lookup"><span data-stu-id="5d0b9-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="5d0b9-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5d0b9-138">-Name</span></span>
<span data-ttu-id="5d0b9-139">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="5d0b9-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="5d0b9-140">-NodeCount</span></span>
<span data-ttu-id="5d0b9-141">Количество узлов, которые должны быть выделены в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="5d0b9-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="5d0b9-142">-NodeSize</span></span>
<span data-ttu-id="5d0b9-143">Количество ядра и памяти, используемых для узлов, выделенных в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="5d0b9-144">Этот параметр должен быть задан, если автоматическая шкала отключена.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="5d0b9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d0b9-145">-ResourceGroupName</span></span>
<span data-ttu-id="5d0b9-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-146">Resource group name.</span></span>

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

### <span data-ttu-id="5d0b9-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="5d0b9-147">-SparkVersion</span></span>
<span data-ttu-id="5d0b9-148">Версия спарк-версии Apache.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-148">Apache Spark version.</span></span>
<span data-ttu-id="5d0b9-149">Разрешенные значения: 2,4</span><span class="sxs-lookup"><span data-stu-id="5d0b9-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="5d0b9-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d0b9-150">-Tag</span></span>
<span data-ttu-id="5d0b9-151">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5d0b9-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5d0b9-152">-WorkspaceName</span></span>
<span data-ttu-id="5d0b9-153">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d0b9-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5d0b9-154">-WorkspaceObject</span></span>
<span data-ttu-id="5d0b9-155">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5d0b9-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d0b9-156">-Confirm</span></span>
<span data-ttu-id="5d0b9-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d0b9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d0b9-158">-WhatIf</span></span>
<span data-ttu-id="5d0b9-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d0b9-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d0b9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0b9-161">CommonParameters</span></span>
<span data-ttu-id="5d0b9-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d0b9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0b9-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d0b9-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0b9-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d0b9-164">INPUTS</span></span>

### <span data-ttu-id="5d0b9-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d0b9-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5d0b9-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d0b9-166">OUTPUTS</span></span>

### <span data-ttu-id="5d0b9-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5d0b9-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="5d0b9-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d0b9-168">NOTES</span></span>

## <span data-ttu-id="5d0b9-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d0b9-169">RELATED LINKS</span></span>
