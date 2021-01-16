---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393807"
---
# <span data-ttu-id="acd63-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="acd63-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="acd63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd63-102">SYNOPSIS</span></span>
<span data-ttu-id="acd63-103">Получает рабочее пространство synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="acd63-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="acd63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acd63-104">SYNTAX</span></span>

### <span data-ttu-id="acd63-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acd63-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acd63-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd63-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd63-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acd63-107">DESCRIPTION</span></span>
<span data-ttu-id="acd63-108">Командлет **Get-AzSynapseWorkspace** получает сведения о рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="acd63-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="acd63-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acd63-109">EXAMPLES</span></span>

### <span data-ttu-id="acd63-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acd63-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="acd63-111">Эта команда получает все бизнес-области Azure Synapse Analytics в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="acd63-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="acd63-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="acd63-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="acd63-113">Эта команда получает все бизнес-области Azure Synapse Analytics в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="acd63-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="acd63-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="acd63-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="acd63-115">Эта команда получает рабочее пространство Azure Synapse Analytics с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="acd63-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="acd63-116">Пример 4</span><span class="sxs-lookup"><span data-stu-id="acd63-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="acd63-117">Эта команда получает рабочее пространство Azure Synapse Analytics с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="acd63-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="acd63-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd63-118">PARAMETERS</span></span>

### <span data-ttu-id="acd63-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd63-119">-DefaultProfile</span></span>
<span data-ttu-id="acd63-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acd63-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd63-121">-Name</span><span class="sxs-lookup"><span data-stu-id="acd63-121">-Name</span></span>
<span data-ttu-id="acd63-122">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="acd63-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="acd63-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd63-123">-ResourceGroupName</span></span>
<span data-ttu-id="acd63-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acd63-124">Resource group name.</span></span>

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

### <span data-ttu-id="acd63-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acd63-125">-ResourceId</span></span>
<span data-ttu-id="acd63-126">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="acd63-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="acd63-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd63-127">CommonParameters</span></span>
<span data-ttu-id="acd63-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd63-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd63-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acd63-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd63-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acd63-130">INPUTS</span></span>

### <span data-ttu-id="acd63-131">Нет</span><span class="sxs-lookup"><span data-stu-id="acd63-131">None</span></span>

## <span data-ttu-id="acd63-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acd63-132">OUTPUTS</span></span>

### <span data-ttu-id="acd63-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="acd63-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="acd63-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acd63-134">NOTES</span></span>

## <span data-ttu-id="acd63-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acd63-135">RELATED LINKS</span></span>
