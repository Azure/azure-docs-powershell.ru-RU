---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397300"
---
# <span data-ttu-id="3f91d-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3f91d-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="3f91d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f91d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f91d-103">Получает правило брандмауэра synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3f91d-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3f91d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f91d-104">SYNTAX</span></span>

### <span data-ttu-id="3f91d-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f91d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f91d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f91d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f91d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f91d-107">DESCRIPTION</span></span>
<span data-ttu-id="3f91d-108">Для **брандмауэра Get-AzSynapseFirewallRule** вы получаете правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3f91d-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="3f91d-109">Если не указать имя правила, этот cmdlet получит все правила.</span><span class="sxs-lookup"><span data-stu-id="3f91d-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="3f91d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f91d-110">EXAMPLES</span></span>

### <span data-ttu-id="3f91d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f91d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3f91d-112">Эта команда получает все правила брандмауэра в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3f91d-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="3f91d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f91d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="3f91d-114">Эта команда получает правило брандмауэра в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="3f91d-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="3f91d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3f91d-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="3f91d-116">Эта команда получает все правила брандмауэра в рабочей области через канал.</span><span class="sxs-lookup"><span data-stu-id="3f91d-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="3f91d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f91d-117">PARAMETERS</span></span>

### <span data-ttu-id="3f91d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f91d-118">-DefaultProfile</span></span>
<span data-ttu-id="3f91d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f91d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f91d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3f91d-120">-Name</span></span>
<span data-ttu-id="3f91d-121">Имя правила брандмауэра для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3f91d-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f91d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f91d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f91d-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f91d-123">Resource group name.</span></span>

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

### <span data-ttu-id="3f91d-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f91d-124">-WorkspaceName</span></span>
<span data-ttu-id="3f91d-125">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="3f91d-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3f91d-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="3f91d-126">-WorkSpaceObject</span></span>
<span data-ttu-id="3f91d-127">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3f91d-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3f91d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f91d-128">CommonParameters</span></span>
<span data-ttu-id="3f91d-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f91d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f91d-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f91d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f91d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f91d-131">INPUTS</span></span>

### <span data-ttu-id="3f91d-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f91d-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3f91d-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f91d-133">OUTPUTS</span></span>

### <span data-ttu-id="3f91d-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3f91d-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="3f91d-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f91d-135">NOTES</span></span>

## <span data-ttu-id="3f91d-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f91d-136">RELATED LINKS</span></span>
