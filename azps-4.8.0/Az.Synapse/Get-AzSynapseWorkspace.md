---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235688"
---
# <span data-ttu-id="434b4-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="434b4-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="434b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="434b4-102">SYNOPSIS</span></span>
<span data-ttu-id="434b4-103">Получает рабочую область Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="434b4-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="434b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="434b4-104">SYNTAX</span></span>

### <span data-ttu-id="434b4-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="434b4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434b4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="434b4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="434b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="434b4-107">DESCRIPTION</span></span>
<span data-ttu-id="434b4-108">Командлет **Get-AzSynapseWorkspace** получает сведения о рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="434b4-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="434b4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="434b4-109">EXAMPLES</span></span>

### <span data-ttu-id="434b4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="434b4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="434b4-111">Эта команда получает все рабочие области аналитики Azure Synapse Analytics в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="434b4-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="434b4-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="434b4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="434b4-113">Эта команда получает все рабочие области аналитики Azure Synapse Analytics в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="434b4-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="434b4-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="434b4-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="434b4-115">Эта команда получает рабочую область Azure Synapse Analytics с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="434b4-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="434b4-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="434b4-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="434b4-117">Эта команда получает рабочую область Azure Synapse Analytics с указанным ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="434b4-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="434b4-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="434b4-118">PARAMETERS</span></span>

### <span data-ttu-id="434b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434b4-119">-DefaultProfile</span></span>
<span data-ttu-id="434b4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="434b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434b4-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="434b4-121">-Name</span></span>
<span data-ttu-id="434b4-122">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="434b4-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="434b4-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="434b4-124">Resource group name.</span></span>

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

### <span data-ttu-id="434b4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="434b4-125">-ResourceId</span></span>
<span data-ttu-id="434b4-126">Идентификатор ресурса Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="434b4-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="434b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434b4-127">CommonParameters</span></span>
<span data-ttu-id="434b4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="434b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434b4-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="434b4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434b4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="434b4-130">INPUTS</span></span>

### <span data-ttu-id="434b4-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="434b4-131">None</span></span>

## <span data-ttu-id="434b4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="434b4-132">OUTPUTS</span></span>

### <span data-ttu-id="434b4-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="434b4-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="434b4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="434b4-134">NOTES</span></span>

## <span data-ttu-id="434b4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="434b4-135">RELATED LINKS</span></span>
