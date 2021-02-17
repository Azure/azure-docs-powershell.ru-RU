---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216852"
---
# <span data-ttu-id="ee47d-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="ee47d-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="ee47d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee47d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee47d-103">Получает спарк-отчет Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ee47d-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="ee47d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee47d-104">SYNTAX</span></span>

### <span data-ttu-id="ee47d-105">GetSparkStatementsByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee47d-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee47d-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee47d-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee47d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee47d-107">DESCRIPTION</span></span>
<span data-ttu-id="ee47d-108">**Спарклет Get-AzSynapseSparkStatement** получает сведения о спарк-отчете Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ee47d-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="ee47d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee47d-109">EXAMPLES</span></span>

### <span data-ttu-id="ee47d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee47d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="ee47d-111">Эта команда получает все выписки по спарк-сеансу.</span><span class="sxs-lookup"><span data-stu-id="ee47d-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="ee47d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee47d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="ee47d-113">Эта команда получает выписку по спарку с указанным livy ID.</span><span class="sxs-lookup"><span data-stu-id="ee47d-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="ee47d-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ee47d-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="ee47d-115">Эта команда получает все спарк-отчеты в конвейере спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee47d-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="ee47d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee47d-116">PARAMETERS</span></span>

### <span data-ttu-id="ee47d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee47d-117">-DefaultProfile</span></span>
<span data-ttu-id="ee47d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee47d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee47d-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="ee47d-119">-LivyId</span></span>
<span data-ttu-id="ee47d-120">Идентификатор спарк-спарка.</span><span class="sxs-lookup"><span data-stu-id="ee47d-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="ee47d-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="ee47d-121">-SessionId</span></span>
<span data-ttu-id="ee47d-122">Идентификатор спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="ee47d-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee47d-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="ee47d-123">-SessionObject</span></span>
<span data-ttu-id="ee47d-124">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ee47d-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee47d-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="ee47d-125">-SparkPoolName</span></span>
<span data-ttu-id="ee47d-126">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="ee47d-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee47d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ee47d-127">-WorkspaceName</span></span>
<span data-ttu-id="ee47d-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="ee47d-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee47d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee47d-129">CommonParameters</span></span>
<span data-ttu-id="ee47d-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee47d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee47d-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee47d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee47d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee47d-132">INPUTS</span></span>

### <span data-ttu-id="ee47d-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="ee47d-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="ee47d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee47d-134">OUTPUTS</span></span>

### <span data-ttu-id="ee47d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="ee47d-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="ee47d-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee47d-136">NOTES</span></span>

## <span data-ttu-id="ee47d-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee47d-137">RELATED LINKS</span></span>
