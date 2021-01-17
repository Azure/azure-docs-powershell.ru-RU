---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424543"
---
# <span data-ttu-id="adda1-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="adda1-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="adda1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adda1-102">SYNOPSIS</span></span>
<span data-ttu-id="adda1-103">Получает правило брандмауэра synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="adda1-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="adda1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="adda1-104">SYNTAX</span></span>

### <span data-ttu-id="adda1-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adda1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adda1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adda1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adda1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adda1-107">DESCRIPTION</span></span>
<span data-ttu-id="adda1-108">Для **брандмауэра Get-AzSynapseFirewallRule** вы получаете правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="adda1-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="adda1-109">Если не указать имя правила, этот cmdlet получит все правила.</span><span class="sxs-lookup"><span data-stu-id="adda1-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="adda1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="adda1-110">EXAMPLES</span></span>

### <span data-ttu-id="adda1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="adda1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="adda1-112">Эта команда получает все правила брандмауэра в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="adda1-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="adda1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="adda1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="adda1-114">Эта команда получает правило брандмауэра в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="adda1-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="adda1-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="adda1-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="adda1-116">Эта команда получает все правила брандмауэра в рабочей области через канал.</span><span class="sxs-lookup"><span data-stu-id="adda1-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="adda1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adda1-117">PARAMETERS</span></span>

### <span data-ttu-id="adda1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adda1-118">-DefaultProfile</span></span>
<span data-ttu-id="adda1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adda1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adda1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="adda1-120">-Name</span></span>
<span data-ttu-id="adda1-121">Имя правила брандмауэра для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="adda1-121">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="adda1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adda1-122">-ResourceGroupName</span></span>
<span data-ttu-id="adda1-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="adda1-123">Resource group name.</span></span>

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

### <span data-ttu-id="adda1-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="adda1-124">-WorkspaceName</span></span>
<span data-ttu-id="adda1-125">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="adda1-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="adda1-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="adda1-126">-WorkSpaceObject</span></span>
<span data-ttu-id="adda1-127">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="adda1-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="adda1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adda1-128">CommonParameters</span></span>
<span data-ttu-id="adda1-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adda1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adda1-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adda1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adda1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adda1-131">INPUTS</span></span>

### <span data-ttu-id="adda1-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="adda1-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="adda1-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="adda1-133">OUTPUTS</span></span>

### <span data-ttu-id="adda1-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="adda1-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="adda1-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="adda1-135">NOTES</span></span>

## <span data-ttu-id="adda1-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adda1-136">RELATED LINKS</span></span>
