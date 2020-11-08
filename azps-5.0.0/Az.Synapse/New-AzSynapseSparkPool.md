---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246316"
---
# <span data-ttu-id="56040-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="56040-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="56040-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56040-102">SYNOPSIS</span></span>
<span data-ttu-id="56040-103">Создание пула Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="56040-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56040-104">SYNTAX</span></span>

### <span data-ttu-id="56040-105">CreateByNameAndEnableAutoScaleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56040-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56040-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="56040-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56040-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="56040-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56040-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="56040-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56040-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56040-109">DESCRIPTION</span></span>
<span data-ttu-id="56040-110">Командлет **New-AzSynapseSparkPool** создает пул Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="56040-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56040-111">EXAMPLES</span></span>

### <span data-ttu-id="56040-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56040-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="56040-113">Эта команда создает пул Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="56040-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="56040-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="56040-115">Эта команда создает пул Azure Synapse Analytics Spark с включенной функцией автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="56040-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="56040-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="56040-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="56040-117">Эта команда создает пул Azure Synapse Analytics Spark через конвейер.</span><span class="sxs-lookup"><span data-stu-id="56040-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="56040-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="56040-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="56040-119">Эта команда создает пул Azure Synapse Analytics Spark с включенным автоматическим масштабированием через конвейер.</span><span class="sxs-lookup"><span data-stu-id="56040-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="56040-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56040-120">PARAMETERS</span></span>

### <span data-ttu-id="56040-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56040-121">-AsJob</span></span>
<span data-ttu-id="56040-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="56040-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56040-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="56040-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="56040-124">Количество минут бездействия.</span><span class="sxs-lookup"><span data-stu-id="56040-124">Number of minutes idle.</span></span> <span data-ttu-id="56040-125">Этот параметр должен быть указан, если включена функция приостановки.</span><span class="sxs-lookup"><span data-stu-id="56040-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="56040-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="56040-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="56040-127">Максимальное количество узлов, которые должны быть выделены в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="56040-128">Этот параметр должен быть указан, если включено автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="56040-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="56040-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="56040-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="56040-130">Минимальное количество узлов, которые должны быть выделены в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="56040-131">Этот параметр должен быть указан, если включено автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="56040-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="56040-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56040-132">-DefaultProfile</span></span>
<span data-ttu-id="56040-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56040-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56040-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="56040-134">-EnableAutoPause</span></span>
<span data-ttu-id="56040-135">Указывает, следует ли включить функцию автоматического приостановки.</span><span class="sxs-lookup"><span data-stu-id="56040-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="56040-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="56040-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="56040-137">Файл конфигурации среды (выводится сообщение "закрепить от PIP").</span><span class="sxs-lookup"><span data-stu-id="56040-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="56040-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56040-138">-Name</span></span>
<span data-ttu-id="56040-139">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="56040-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="56040-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="56040-140">-NodeCount</span></span>
<span data-ttu-id="56040-141">Количество узлов, которые должны быть выделены в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="56040-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="56040-142">-NodeSize</span></span>
<span data-ttu-id="56040-143">Количество ядер и памяти, которые будут использоваться для узлов, выделенных в указанном пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="56040-144">Этот параметр должен быть указан, если отключено автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="56040-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="56040-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56040-145">-ResourceGroupName</span></span>
<span data-ttu-id="56040-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56040-146">Resource group name.</span></span>

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

### <span data-ttu-id="56040-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="56040-147">-SparkVersion</span></span>
<span data-ttu-id="56040-148">Версия Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="56040-148">Apache Spark version.</span></span>
<span data-ttu-id="56040-149">Разрешенные значения: 2,4</span><span class="sxs-lookup"><span data-stu-id="56040-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="56040-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="56040-150">-Tag</span></span>
<span data-ttu-id="56040-151">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="56040-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="56040-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="56040-152">-WorkspaceName</span></span>
<span data-ttu-id="56040-153">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="56040-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="56040-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="56040-154">-WorkspaceObject</span></span>
<span data-ttu-id="56040-155">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="56040-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="56040-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56040-156">-Confirm</span></span>
<span data-ttu-id="56040-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56040-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56040-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56040-158">-WhatIf</span></span>
<span data-ttu-id="56040-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56040-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56040-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56040-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56040-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56040-161">CommonParameters</span></span>
<span data-ttu-id="56040-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56040-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56040-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56040-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56040-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56040-164">INPUTS</span></span>

### <span data-ttu-id="56040-165">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="56040-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="56040-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56040-166">OUTPUTS</span></span>

### <span data-ttu-id="56040-167">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="56040-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="56040-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="56040-168">NOTES</span></span>

## <span data-ttu-id="56040-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56040-169">RELATED LINKS</span></span>
