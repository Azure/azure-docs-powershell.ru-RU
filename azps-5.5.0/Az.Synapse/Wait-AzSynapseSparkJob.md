---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216692"
---
# <span data-ttu-id="5ca2d-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="5ca2d-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="5ca2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca2d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca2d-103">Ожидание завершения задания спаркпарка synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="5ca2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ca2d-104">SYNTAX</span></span>

### <span data-ttu-id="5ca2d-105">WaitSparkJobByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ca2d-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ca2d-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ca2d-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ca2d-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ca2d-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ca2d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ca2d-108">DESCRIPTION</span></span>
<span data-ttu-id="5ca2d-109">Для выполнения задания аналитики Azure Synapse Analytics выполнится cmdlet **Wait-AzSynapseSparkJob.**</span><span class="sxs-lookup"><span data-stu-id="5ca2d-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="5ca2d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ca2d-110">EXAMPLES</span></span>

### <span data-ttu-id="5ca2d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ca2d-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="5ca2d-112">Эта команда ждет завершения задания с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="5ca2d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ca2d-113">PARAMETERS</span></span>

### <span data-ttu-id="5ca2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca2d-114">-DefaultProfile</span></span>
<span data-ttu-id="5ca2d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca2d-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="5ca2d-116">-LivyId</span></span>
<span data-ttu-id="5ca2d-117">Идентификатор задания "Спарк".</span><span class="sxs-lookup"><span data-stu-id="5ca2d-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="5ca2d-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="5ca2d-118">-SparkJobObject</span></span>
<span data-ttu-id="5ca2d-119">Объект ввода задания спарк-задания, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5ca2d-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="5ca2d-120">-SparkPoolName</span></span>
<span data-ttu-id="5ca2d-121">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="5ca2d-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="5ca2d-122">-SparkPoolObject</span></span>
<span data-ttu-id="5ca2d-123">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5ca2d-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5ca2d-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="5ca2d-125">Максимальное время, необходимое для ожидания ошибки. Значением по умолчанию является никогда неисполнение времени.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="5ca2d-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5ca2d-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="5ca2d-127">Интервал опроса (в секундах) между проверками состояния задания.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="5ca2d-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ca2d-128">-WorkspaceName</span></span>
<span data-ttu-id="5ca2d-129">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5ca2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca2d-130">CommonParameters</span></span>
<span data-ttu-id="5ca2d-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca2d-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ca2d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca2d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ca2d-133">INPUTS</span></span>

### <span data-ttu-id="5ca2d-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="5ca2d-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="5ca2d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="5ca2d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="5ca2d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ca2d-136">OUTPUTS</span></span>

### <span data-ttu-id="5ca2d-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ca2d-137">System.Boolean</span></span>

## <span data-ttu-id="5ca2d-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ca2d-138">NOTES</span></span>

## <span data-ttu-id="5ca2d-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ca2d-139">RELATED LINKS</span></span>
