---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: e7e873638e38ed8c0c561fce5c4cd425be7bafbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992029"
---
# <span data-ttu-id="cabc3-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="cabc3-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="cabc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabc3-102">SYNOPSIS</span></span>
<span data-ttu-id="cabc3-103">Запускает сеанс спарк-сеанса synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cabc3-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="cabc3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cabc3-104">SYNTAX</span></span>

### <span data-ttu-id="cabc3-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cabc3-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cabc3-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cabc3-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cabc3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cabc3-107">DESCRIPTION</span></span>
<span data-ttu-id="cabc3-108">Для запуска сеанса спарк-сеанса Synapse Analytics запускается cmdlet **Start-AzSynapseSparkSession.**</span><span class="sxs-lookup"><span data-stu-id="cabc3-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="cabc3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cabc3-109">EXAMPLES</span></span>

### <span data-ttu-id="cabc3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cabc3-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="cabc3-111">Эта команда запускает сеанс спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cabc3-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="cabc3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cabc3-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="cabc3-113">Эта команда запускает сеанс спаркпарков Azure Synapse Analytics через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cabc3-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="cabc3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cabc3-114">PARAMETERS</span></span>

### <span data-ttu-id="cabc3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cabc3-115">-AsJob</span></span>
<span data-ttu-id="cabc3-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cabc3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cabc3-117">-Configuration</span><span class="sxs-lookup"><span data-stu-id="cabc3-117">-Configuration</span></span>
<span data-ttu-id="cabc3-118">Свойства конфигурации спарк.</span><span class="sxs-lookup"><span data-stu-id="cabc3-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="cabc3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabc3-119">-DefaultProfile</span></span>
<span data-ttu-id="cabc3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cabc3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cabc3-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="cabc3-121">-ExecutorCount</span></span>
<span data-ttu-id="cabc3-122">Количество исполнятелей, которые должны быть выделены в указанном пуле спарков для задания.</span><span class="sxs-lookup"><span data-stu-id="cabc3-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="cabc3-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="cabc3-123">-ExecutorSize</span></span>
<span data-ttu-id="cabc3-124">Количество ядра и памяти, используемых для исполнятелей, выделенных в указанном пуле спарков для задания.</span><span class="sxs-lookup"><span data-stu-id="cabc3-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="cabc3-125">-Language</span><span class="sxs-lookup"><span data-stu-id="cabc3-125">-Language</span></span>
<span data-ttu-id="cabc3-126">Язык кода выполнения.</span><span class="sxs-lookup"><span data-stu-id="cabc3-126">Language of the execution code.</span></span>

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

### <span data-ttu-id="cabc3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="cabc3-127">-Name</span></span>
<span data-ttu-id="cabc3-128">Имя сеанса спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="cabc3-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="cabc3-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="cabc3-129">-ReferenceFile</span></span>
<span data-ttu-id="cabc3-130">Дополнительные файлы, используемые для справки в основном файле определения.</span><span class="sxs-lookup"><span data-stu-id="cabc3-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="cabc3-131">Список URI хранилища с разделами-запятой.</span><span class="sxs-lookup"><span data-stu-id="cabc3-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="cabc3-132">например, " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="cabc3-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="cabc3-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="cabc3-133">-SparkPoolName</span></span>
<span data-ttu-id="cabc3-134">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="cabc3-134">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="cabc3-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="cabc3-135">-SparkPoolObject</span></span>
<span data-ttu-id="cabc3-136">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cabc3-136">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cabc3-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cabc3-137">-WorkspaceName</span></span>
<span data-ttu-id="cabc3-138">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cabc3-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cabc3-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cabc3-139">-Confirm</span></span>
<span data-ttu-id="cabc3-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cabc3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cabc3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cabc3-141">-WhatIf</span></span>
<span data-ttu-id="cabc3-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cabc3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cabc3-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cabc3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cabc3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabc3-144">CommonParameters</span></span>
<span data-ttu-id="cabc3-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabc3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabc3-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cabc3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabc3-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cabc3-147">INPUTS</span></span>

### <span data-ttu-id="cabc3-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="cabc3-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="cabc3-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cabc3-149">OUTPUTS</span></span>

### <span data-ttu-id="cabc3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="cabc3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="cabc3-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cabc3-151">NOTES</span></span>

## <span data-ttu-id="cabc3-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cabc3-152">RELATED LINKS</span></span>
