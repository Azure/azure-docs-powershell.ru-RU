---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410479"
---
# <span data-ttu-id="157db-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="157db-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="157db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="157db-102">SYNOPSIS</span></span>
<span data-ttu-id="157db-103">Получает пул спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="157db-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="157db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="157db-104">SYNTAX</span></span>

### <span data-ttu-id="157db-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="157db-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="157db-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="157db-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="157db-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="157db-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="157db-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="157db-108">DESCRIPTION</span></span>
<span data-ttu-id="157db-109">**Спарклет Get-AzSynapseSparkPool** получает сведения о пуле спаркпарков Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="157db-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="157db-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="157db-110">EXAMPLES</span></span>

### <span data-ttu-id="157db-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="157db-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="157db-112">Эта команда получает все пулы спаркпарков под рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="157db-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="157db-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="157db-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="157db-114">Эта команда получает пул spark в рабочей области ContosoWorkspace с именем ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="157db-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="157db-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="157db-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="157db-116">Эта команда получает все пулы спаркпарков под рабочей областью через канал.</span><span class="sxs-lookup"><span data-stu-id="157db-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="157db-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="157db-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="157db-118">Эта команда возвращает пул спарков с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="157db-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="157db-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="157db-119">PARAMETERS</span></span>

### <span data-ttu-id="157db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157db-120">-DefaultProfile</span></span>
<span data-ttu-id="157db-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="157db-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="157db-122">-Name</span><span class="sxs-lookup"><span data-stu-id="157db-122">-Name</span></span>
<span data-ttu-id="157db-123">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="157db-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="157db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157db-124">-ResourceGroupName</span></span>
<span data-ttu-id="157db-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="157db-125">Resource group name.</span></span>

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

### <span data-ttu-id="157db-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="157db-126">-ResourceId</span></span>
<span data-ttu-id="157db-127">Идентификатор ресурса пула synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="157db-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="157db-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="157db-128">-WorkspaceName</span></span>
<span data-ttu-id="157db-129">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="157db-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="157db-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="157db-130">-WorkspaceObject</span></span>
<span data-ttu-id="157db-131">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="157db-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="157db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157db-132">CommonParameters</span></span>
<span data-ttu-id="157db-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157db-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="157db-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157db-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="157db-135">INPUTS</span></span>

### <span data-ttu-id="157db-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="157db-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="157db-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="157db-137">OUTPUTS</span></span>

### <span data-ttu-id="157db-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="157db-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="157db-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="157db-139">NOTES</span></span>

## <span data-ttu-id="157db-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="157db-140">RELATED LINKS</span></span>
