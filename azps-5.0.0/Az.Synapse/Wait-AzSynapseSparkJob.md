---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247130"
---
# <span data-ttu-id="77577-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="77577-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="77577-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77577-102">SYNOPSIS</span></span>
<span data-ttu-id="77577-103">Ожидание завершения задания Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="77577-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="77577-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77577-104">SYNTAX</span></span>

### <span data-ttu-id="77577-105">WaitSparkJobByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77577-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77577-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77577-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77577-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77577-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77577-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77577-108">DESCRIPTION</span></span>
<span data-ttu-id="77577-109">Командлет **Wait-AzSynapseSparkJob** ожидает завершения задания Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="77577-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="77577-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77577-110">EXAMPLES</span></span>

### <span data-ttu-id="77577-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77577-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="77577-112">Эта команда ожидает завершения задания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="77577-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="77577-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77577-113">PARAMETERS</span></span>

### <span data-ttu-id="77577-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77577-114">-DefaultProfile</span></span>
<span data-ttu-id="77577-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77577-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77577-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="77577-116">-LivyId</span></span>
<span data-ttu-id="77577-117">Идентификатор задания Spark.</span><span class="sxs-lookup"><span data-stu-id="77577-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77577-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="77577-118">-SparkJobObject</span></span>
<span data-ttu-id="77577-119">Объект ввода задания Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="77577-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77577-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="77577-120">-SparkPoolName</span></span>
<span data-ttu-id="77577-121">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="77577-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77577-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="77577-122">-SparkPoolObject</span></span>
<span data-ttu-id="77577-123">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="77577-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77577-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="77577-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="77577-125">Максимальное количество времени, в течение которого можно подождать, прежде чем поступать с ошибкой. Значение по умолчанию — никогда не ограничено временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="77577-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="77577-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="77577-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="77577-127">Интервал опроса между проверками состояния задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="77577-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="77577-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="77577-128">-WorkspaceName</span></span>
<span data-ttu-id="77577-129">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="77577-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77577-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77577-130">CommonParameters</span></span>
<span data-ttu-id="77577-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77577-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77577-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77577-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77577-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77577-133">INPUTS</span></span>

### <span data-ttu-id="77577-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="77577-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="77577-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="77577-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="77577-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77577-136">OUTPUTS</span></span>

### <span data-ttu-id="77577-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77577-137">System.Boolean</span></span>

## <span data-ttu-id="77577-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="77577-138">NOTES</span></span>

## <span data-ttu-id="77577-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77577-139">RELATED LINKS</span></span>
