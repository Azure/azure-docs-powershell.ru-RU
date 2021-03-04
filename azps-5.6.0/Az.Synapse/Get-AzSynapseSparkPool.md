---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: 48ecf7e0c840ca5054e19a250bc53d95de82c08d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015747"
---
# <span data-ttu-id="641e4-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="641e4-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="641e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="641e4-102">SYNOPSIS</span></span>
<span data-ttu-id="641e4-103">Получает пул спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="641e4-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="641e4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="641e4-104">SYNTAX</span></span>

### <span data-ttu-id="641e4-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="641e4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="641e4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="641e4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="641e4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="641e4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="641e4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="641e4-108">DESCRIPTION</span></span>
<span data-ttu-id="641e4-109">**Спарклет Get-AzSynapseSparkPool** получает сведения о пуле спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="641e4-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="641e4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="641e4-110">EXAMPLES</span></span>

### <span data-ttu-id="641e4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="641e4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="641e4-112">Эта команда получает все пулы спаркпарков под рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="641e4-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="641e4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="641e4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="641e4-114">Эта команда получает пул spark в рабочей области ContosoWorkspace с именем ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="641e4-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="641e4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="641e4-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="641e4-116">Эта команда получает все пулы спаркпарков под рабочей областью через канал.</span><span class="sxs-lookup"><span data-stu-id="641e4-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="641e4-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="641e4-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="641e4-118">Эта команда возвращает пул спарков с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="641e4-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="641e4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="641e4-119">PARAMETERS</span></span>

### <span data-ttu-id="641e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641e4-120">-DefaultProfile</span></span>
<span data-ttu-id="641e4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="641e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="641e4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="641e4-122">-Name</span></span>
<span data-ttu-id="641e4-123">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="641e4-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="641e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="641e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="641e4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="641e4-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="641e4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="641e4-126">-ResourceId</span></span>
<span data-ttu-id="641e4-127">Идентификатор ресурса пула synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="641e4-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="641e4-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="641e4-128">-WorkspaceName</span></span>
<span data-ttu-id="641e4-129">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="641e4-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="641e4-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="641e4-130">-WorkspaceObject</span></span>
<span data-ttu-id="641e4-131">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="641e4-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="641e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641e4-132">CommonParameters</span></span>
<span data-ttu-id="641e4-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="641e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641e4-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="641e4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641e4-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="641e4-135">INPUTS</span></span>

### <span data-ttu-id="641e4-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="641e4-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="641e4-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="641e4-137">OUTPUTS</span></span>

### <span data-ttu-id="641e4-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="641e4-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="641e4-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="641e4-139">NOTES</span></span>

## <span data-ttu-id="641e4-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="641e4-140">RELATED LINKS</span></span>
