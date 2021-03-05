---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: 25107456afbf85aa41dd0be600a20f7a5fcbb640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970104"
---
# <span data-ttu-id="5611a-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5611a-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="5611a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5611a-102">SYNOPSIS</span></span>
<span data-ttu-id="5611a-103">Получает рабочее пространство synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5611a-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5611a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5611a-104">SYNTAX</span></span>

### <span data-ttu-id="5611a-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5611a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5611a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5611a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5611a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5611a-107">DESCRIPTION</span></span>
<span data-ttu-id="5611a-108">Командлет **Get-AzSynapseWorkspace** получает сведения о рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5611a-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5611a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5611a-109">EXAMPLES</span></span>

### <span data-ttu-id="5611a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5611a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="5611a-111">Эта команда получает все бизнес-области Azure Synapse Analytics в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="5611a-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="5611a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5611a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="5611a-113">Эта команда получает все бизнес-области Azure Synapse Analytics в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="5611a-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="5611a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5611a-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="5611a-115">Эта команда получает рабочее пространство Azure Synapse Analytics с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="5611a-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="5611a-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5611a-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="5611a-117">Эта команда получает рабочее пространство Azure Synapse Analytics с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="5611a-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="5611a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5611a-118">PARAMETERS</span></span>

### <span data-ttu-id="5611a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5611a-119">-DefaultProfile</span></span>
<span data-ttu-id="5611a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5611a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5611a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5611a-121">-Name</span></span>
<span data-ttu-id="5611a-122">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="5611a-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5611a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5611a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5611a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5611a-124">Resource group name.</span></span>

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

### <span data-ttu-id="5611a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5611a-125">-ResourceId</span></span>
<span data-ttu-id="5611a-126">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="5611a-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="5611a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5611a-127">CommonParameters</span></span>
<span data-ttu-id="5611a-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5611a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5611a-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5611a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5611a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5611a-130">INPUTS</span></span>

### <span data-ttu-id="5611a-131">Нет</span><span class="sxs-lookup"><span data-stu-id="5611a-131">None</span></span>

## <span data-ttu-id="5611a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5611a-132">OUTPUTS</span></span>

### <span data-ttu-id="5611a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5611a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5611a-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5611a-134">NOTES</span></span>

## <span data-ttu-id="5611a-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5611a-135">RELATED LINKS</span></span>
