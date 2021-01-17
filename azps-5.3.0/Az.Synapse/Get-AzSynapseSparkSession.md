---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424479"
---
# <span data-ttu-id="ffe31-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="ffe31-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="ffe31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffe31-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe31-103">Сеанс спаркпарков synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffe31-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="ffe31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffe31-104">SYNTAX</span></span>

### <span data-ttu-id="ffe31-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffe31-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffe31-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffe31-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffe31-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffe31-107">DESCRIPTION</span></span>
<span data-ttu-id="ffe31-108">**Спарклет Get-AzSynapseSparkSession** получает сведения о спарк-сеансе Аналитики Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="ffe31-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="ffe31-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffe31-109">EXAMPLES</span></span>

### <span data-ttu-id="ffe31-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ffe31-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="ffe31-111">Эта команда получает все сеансы спарк-спарков в указанном пуле спарков.</span><span class="sxs-lookup"><span data-stu-id="ffe31-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="ffe31-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ffe31-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="ffe31-113">Эта команда возвращает сеанс спарк-спарков с указанным livy ID.</span><span class="sxs-lookup"><span data-stu-id="ffe31-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="ffe31-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ffe31-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="ffe31-115">Эта команда получает все сеансы спарк-спарков в заданном пуле спарк-каналов.</span><span class="sxs-lookup"><span data-stu-id="ffe31-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="ffe31-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffe31-116">PARAMETERS</span></span>

### <span data-ttu-id="ffe31-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ffe31-117">-ApplicationId</span></span>
<span data-ttu-id="ffe31-118">Идентификатор приложения сеанса.</span><span class="sxs-lookup"><span data-stu-id="ffe31-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="ffe31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe31-119">-DefaultProfile</span></span>
<span data-ttu-id="ffe31-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffe31-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffe31-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="ffe31-121">-LivyId</span></span>
<span data-ttu-id="ffe31-122">Идентификатор спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="ffe31-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="ffe31-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ffe31-123">-Name</span></span>
<span data-ttu-id="ffe31-124">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="ffe31-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ffe31-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="ffe31-125">-SparkPoolName</span></span>
<span data-ttu-id="ffe31-126">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="ffe31-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe31-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="ffe31-127">-SparkPoolObject</span></span>
<span data-ttu-id="ffe31-128">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ffe31-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe31-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ffe31-129">-WorkspaceName</span></span>
<span data-ttu-id="ffe31-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="ffe31-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe31-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe31-131">CommonParameters</span></span>
<span data-ttu-id="ffe31-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffe31-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffe31-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffe31-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe31-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffe31-134">INPUTS</span></span>

### <span data-ttu-id="ffe31-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ffe31-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="ffe31-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffe31-136">OUTPUTS</span></span>

### <span data-ttu-id="ffe31-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="ffe31-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="ffe31-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffe31-138">NOTES</span></span>

## <span data-ttu-id="ffe31-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffe31-139">RELATED LINKS</span></span>
