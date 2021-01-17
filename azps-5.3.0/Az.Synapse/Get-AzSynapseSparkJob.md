---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424487"
---
# <span data-ttu-id="b24b1-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b24b1-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="b24b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b24b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b24b1-103">Получает задание Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="b24b1-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="b24b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b24b1-104">SYNTAX</span></span>

### <span data-ttu-id="b24b1-105">GetSparkJobsByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b24b1-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b24b1-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b24b1-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b24b1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b24b1-107">DESCRIPTION</span></span>
<span data-ttu-id="b24b1-108">Для **этого спарклет Get-AzSynapseSparkJob** получает задание спаркпарка Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b24b1-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="b24b1-109">Если задание не указано, этот cmdlet получает все задания.</span><span class="sxs-lookup"><span data-stu-id="b24b1-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="b24b1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b24b1-110">EXAMPLES</span></span>

### <span data-ttu-id="b24b1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b24b1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="b24b1-112">Эта команда получает все задания в пуле спаркпарков.</span><span class="sxs-lookup"><span data-stu-id="b24b1-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="b24b1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b24b1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="b24b1-114">Эта команда получает задание с указанным ид.</span><span class="sxs-lookup"><span data-stu-id="b24b1-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="b24b1-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b24b1-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="b24b1-116">Эта команда получает задание с указанным ИД приложения.</span><span class="sxs-lookup"><span data-stu-id="b24b1-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="b24b1-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b24b1-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="b24b1-118">Эта команда получает все задания в пуле спаркпарков по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="b24b1-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="b24b1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b24b1-119">PARAMETERS</span></span>

### <span data-ttu-id="b24b1-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b24b1-120">-ApplicationId</span></span>
<span data-ttu-id="b24b1-121">Идентификатор приложения сеанса.</span><span class="sxs-lookup"><span data-stu-id="b24b1-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="b24b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24b1-122">-DefaultProfile</span></span>
<span data-ttu-id="b24b1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b24b1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24b1-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="b24b1-124">-LivyId</span></span>
<span data-ttu-id="b24b1-125">Идентификатор задания "Спарк".</span><span class="sxs-lookup"><span data-stu-id="b24b1-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="b24b1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b24b1-126">-Name</span></span>
<span data-ttu-id="b24b1-127">Имя задания "Спарк".</span><span class="sxs-lookup"><span data-stu-id="b24b1-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="b24b1-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b24b1-128">-SparkPoolName</span></span>
<span data-ttu-id="b24b1-129">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="b24b1-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="b24b1-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="b24b1-130">-SparkPoolObject</span></span>
<span data-ttu-id="b24b1-131">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b24b1-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b24b1-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b24b1-132">-WorkspaceName</span></span>
<span data-ttu-id="b24b1-133">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="b24b1-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b24b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24b1-134">CommonParameters</span></span>
<span data-ttu-id="b24b1-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24b1-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b24b1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24b1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b24b1-137">INPUTS</span></span>

### <span data-ttu-id="b24b1-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b24b1-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="b24b1-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b24b1-139">OUTPUTS</span></span>

### <span data-ttu-id="b24b1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="b24b1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="b24b1-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b24b1-141">NOTES</span></span>

## <span data-ttu-id="b24b1-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b24b1-142">RELATED LINKS</span></span>
