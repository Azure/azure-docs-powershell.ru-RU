---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247958"
---
# <span data-ttu-id="9721e-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9721e-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="9721e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9721e-102">SYNOPSIS</span></span>
<span data-ttu-id="9721e-103">Запуск сеанса Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9721e-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9721e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9721e-104">SYNTAX</span></span>

### <span data-ttu-id="9721e-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9721e-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9721e-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9721e-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9721e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9721e-107">DESCRIPTION</span></span>
<span data-ttu-id="9721e-108">Командлет **Start-AzSynapseSparkSession** запускает сеанс Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9721e-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9721e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9721e-109">EXAMPLES</span></span>

### <span data-ttu-id="9721e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9721e-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="9721e-111">Эта команда запускает сеанс Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9721e-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="9721e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9721e-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="9721e-113">Эта команда запускает сеанс Azure Synapse Analytics Spark через конвейер.</span><span class="sxs-lookup"><span data-stu-id="9721e-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="9721e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9721e-114">PARAMETERS</span></span>

### <span data-ttu-id="9721e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9721e-115">-AsJob</span></span>
<span data-ttu-id="9721e-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9721e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9721e-117">-Configuration</span><span class="sxs-lookup"><span data-stu-id="9721e-117">-Configuration</span></span>
<span data-ttu-id="9721e-118">Свойства конфигурации Spark.</span><span class="sxs-lookup"><span data-stu-id="9721e-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="9721e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9721e-119">-DefaultProfile</span></span>
<span data-ttu-id="9721e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9721e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9721e-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="9721e-121">-ExecutorCount</span></span>
<span data-ttu-id="9721e-122">Количество исполнителей, которые должны быть выделены в указанном пуле Spark для задания.</span><span class="sxs-lookup"><span data-stu-id="9721e-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9721e-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="9721e-123">-ExecutorSize</span></span>
<span data-ttu-id="9721e-124">Число ядер и памяти, используемых для исполнителей, выделенных в указанном пуле Spark для задания.</span><span class="sxs-lookup"><span data-stu-id="9721e-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="9721e-125">-Language</span><span class="sxs-lookup"><span data-stu-id="9721e-125">-Language</span></span>
<span data-ttu-id="9721e-126">Язык кода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9721e-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9721e-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9721e-127">-Name</span></span>
<span data-ttu-id="9721e-128">Имя сеанса Spark.</span><span class="sxs-lookup"><span data-stu-id="9721e-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="9721e-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="9721e-129">-ReferenceFile</span></span>
<span data-ttu-id="9721e-130">Дополнительные файлы, используемые для ссылки в основном файле определения.</span><span class="sxs-lookup"><span data-stu-id="9721e-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="9721e-131">Список URI хранилища с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="9721e-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="9721e-132">например " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="9721e-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="9721e-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9721e-133">-SparkPoolName</span></span>
<span data-ttu-id="9721e-134">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="9721e-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9721e-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9721e-135">-SparkPoolObject</span></span>
<span data-ttu-id="9721e-136">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="9721e-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9721e-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9721e-137">-WorkspaceName</span></span>
<span data-ttu-id="9721e-138">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9721e-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9721e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9721e-139">-Confirm</span></span>
<span data-ttu-id="9721e-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9721e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9721e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9721e-141">-WhatIf</span></span>
<span data-ttu-id="9721e-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9721e-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9721e-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9721e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9721e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9721e-144">CommonParameters</span></span>
<span data-ttu-id="9721e-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9721e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9721e-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9721e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9721e-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9721e-147">INPUTS</span></span>

### <span data-ttu-id="9721e-148">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9721e-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="9721e-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9721e-149">OUTPUTS</span></span>

### <span data-ttu-id="9721e-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9721e-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9721e-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="9721e-151">NOTES</span></span>

## <span data-ttu-id="9721e-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9721e-152">RELATED LINKS</span></span>
