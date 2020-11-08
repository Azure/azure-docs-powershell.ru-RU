---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247959"
---
# <span data-ttu-id="67fa8-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="67fa8-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="67fa8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="67fa8-103">Получает задание Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="67fa8-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="67fa8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67fa8-104">SYNTAX</span></span>

### <span data-ttu-id="67fa8-105">GetSparkJobsByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67fa8-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67fa8-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67fa8-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67fa8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67fa8-107">DESCRIPTION</span></span>
<span data-ttu-id="67fa8-108">Командлет **Get-AzSynapseSparkJob** получает задание Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="67fa8-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="67fa8-109">Если задание не задано, этот командлет получает все задания.</span><span class="sxs-lookup"><span data-stu-id="67fa8-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="67fa8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67fa8-110">EXAMPLES</span></span>

### <span data-ttu-id="67fa8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67fa8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="67fa8-112">Эта команда получает все задания в пуле Spark.</span><span class="sxs-lookup"><span data-stu-id="67fa8-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="67fa8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="67fa8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="67fa8-114">Эта команда получает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="67fa8-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="67fa8-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="67fa8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="67fa8-116">Эта команда получает задание с указанным ИДЕНТИФИКАТОРом приложения.</span><span class="sxs-lookup"><span data-stu-id="67fa8-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="67fa8-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="67fa8-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="67fa8-118">Эта команда получает все задания из пула Spark с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="67fa8-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="67fa8-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67fa8-119">PARAMETERS</span></span>

### <span data-ttu-id="67fa8-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67fa8-120">-ApplicationId</span></span>
<span data-ttu-id="67fa8-121">Идентификатор приложения сеанса.</span><span class="sxs-lookup"><span data-stu-id="67fa8-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="67fa8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67fa8-122">-DefaultProfile</span></span>
<span data-ttu-id="67fa8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67fa8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67fa8-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="67fa8-124">-LivyId</span></span>
<span data-ttu-id="67fa8-125">Идентификатор задания Spark.</span><span class="sxs-lookup"><span data-stu-id="67fa8-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fa8-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67fa8-126">-Name</span></span>
<span data-ttu-id="67fa8-127">Имя задания Spark.</span><span class="sxs-lookup"><span data-stu-id="67fa8-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="67fa8-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="67fa8-128">-SparkPoolName</span></span>
<span data-ttu-id="67fa8-129">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="67fa8-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fa8-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="67fa8-130">-SparkPoolObject</span></span>
<span data-ttu-id="67fa8-131">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="67fa8-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67fa8-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67fa8-132">-WorkspaceName</span></span>
<span data-ttu-id="67fa8-133">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="67fa8-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67fa8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67fa8-134">CommonParameters</span></span>
<span data-ttu-id="67fa8-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67fa8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67fa8-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67fa8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67fa8-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67fa8-137">INPUTS</span></span>

### <span data-ttu-id="67fa8-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="67fa8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="67fa8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67fa8-139">OUTPUTS</span></span>

### <span data-ttu-id="67fa8-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="67fa8-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="67fa8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="67fa8-141">NOTES</span></span>

## <span data-ttu-id="67fa8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67fa8-142">RELATED LINKS</span></span>
