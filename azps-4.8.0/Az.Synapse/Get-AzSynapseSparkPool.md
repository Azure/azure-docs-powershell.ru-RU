---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077479"
---
# <span data-ttu-id="8bfa1-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8bfa1-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="8bfa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bfa1-102">SYNOPSIS</span></span>
<span data-ttu-id="8bfa1-103">Возвращает пул Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="8bfa1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bfa1-104">SYNTAX</span></span>

### <span data-ttu-id="8bfa1-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bfa1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bfa1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bfa1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bfa1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bfa1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bfa1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bfa1-108">DESCRIPTION</span></span>
<span data-ttu-id="8bfa1-109">Командлет **Get-AzSynapseSparkPool** получает сведения о пуле Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="8bfa1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bfa1-110">EXAMPLES</span></span>

### <span data-ttu-id="8bfa1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bfa1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8bfa1-112">Эта команда получает список всех пулов Spark в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="8bfa1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8bfa1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="8bfa1-114">Эта команда получает пул Spark из рабочей области ContosoWorkspace с именем ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="8bfa1-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8bfa1-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="8bfa1-116">Эта команда получает доступ ко всем пулам Spark из рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="8bfa1-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="8bfa1-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="8bfa1-118">Эта команда получает пул Spark с указанным ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="8bfa1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bfa1-119">PARAMETERS</span></span>

### <span data-ttu-id="8bfa1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bfa1-120">-DefaultProfile</span></span>
<span data-ttu-id="8bfa1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bfa1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8bfa1-122">-Name</span></span>
<span data-ttu-id="8bfa1-123">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8bfa1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bfa1-124">-ResourceGroupName</span></span>
<span data-ttu-id="8bfa1-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-125">Resource group name.</span></span>

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

### <span data-ttu-id="8bfa1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bfa1-126">-ResourceId</span></span>
<span data-ttu-id="8bfa1-127">Идентификатор ресурса для пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8bfa1-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8bfa1-128">-WorkspaceName</span></span>
<span data-ttu-id="8bfa1-129">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8bfa1-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8bfa1-130">-WorkspaceObject</span></span>
<span data-ttu-id="8bfa1-131">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8bfa1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bfa1-132">CommonParameters</span></span>
<span data-ttu-id="8bfa1-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bfa1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bfa1-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bfa1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bfa1-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bfa1-135">INPUTS</span></span>

### <span data-ttu-id="8bfa1-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8bfa1-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8bfa1-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bfa1-137">OUTPUTS</span></span>

### <span data-ttu-id="8bfa1-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8bfa1-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="8bfa1-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bfa1-139">NOTES</span></span>

## <span data-ttu-id="8bfa1-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bfa1-140">RELATED LINKS</span></span>
