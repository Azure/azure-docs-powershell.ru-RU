---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506922"
---
# <span data-ttu-id="7f565-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7f565-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="7f565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f565-102">SYNOPSIS</span></span>
<span data-ttu-id="7f565-103">Создание правила сети брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="7f565-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="7f565-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f565-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f565-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f565-105">DESCRIPTION</span></span>
<span data-ttu-id="7f565-106">Командлет **New-AzFirewallPolicyNetworkRule** создает правило сети для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7f565-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="7f565-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f565-107">EXAMPLES</span></span>

### <span data-ttu-id="7f565-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f565-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="7f565-109">В этом примере создается правило сети с исходным адресом, протоколом, адресом назначения и портом назначения.</span><span class="sxs-lookup"><span data-stu-id="7f565-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="7f565-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f565-110">PARAMETERS</span></span>

### <span data-ttu-id="7f565-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f565-111">-DefaultProfile</span></span>
<span data-ttu-id="7f565-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f565-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-113">-Description</span><span class="sxs-lookup"><span data-stu-id="7f565-113">-Description</span></span>
<span data-ttu-id="7f565-114">Описание правила</span><span class="sxs-lookup"><span data-stu-id="7f565-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7f565-115">-DestinationAddress</span></span>
<span data-ttu-id="7f565-116">Адреса назначения правила</span><span class="sxs-lookup"><span data-stu-id="7f565-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="7f565-117">-DestinationFqdn</span></span>
<span data-ttu-id="7f565-118">Конечное FQDN правила</span><span class="sxs-lookup"><span data-stu-id="7f565-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="7f565-119">-DestinationIpGroup</span></span>
<span data-ttu-id="7f565-120">Ipgroups назначения правила</span><span class="sxs-lookup"><span data-stu-id="7f565-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7f565-121">-DestinationPort</span></span>
<span data-ttu-id="7f565-122">Порты назначения правила</span><span class="sxs-lookup"><span data-stu-id="7f565-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7f565-123">-Name</span></span>
<span data-ttu-id="7f565-124">Имя правила сети</span><span class="sxs-lookup"><span data-stu-id="7f565-124">The name of the Network Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7f565-125">-Protocol</span></span>
<span data-ttu-id="7f565-126">Протоколы правила</span><span class="sxs-lookup"><span data-stu-id="7f565-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7f565-127">-SourceAddress</span></span>
<span data-ttu-id="7f565-128">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="7f565-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="7f565-129">-SourceIpGroup</span></span>
<span data-ttu-id="7f565-130">Исходные IP-группы правила</span><span class="sxs-lookup"><span data-stu-id="7f565-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f565-131">-Confirm</span></span>
<span data-ttu-id="7f565-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7f565-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f565-133">-WhatIf</span></span>
<span data-ttu-id="7f565-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f565-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f565-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f565-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f565-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f565-136">CommonParameters</span></span>
<span data-ttu-id="7f565-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f565-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f565-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f565-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f565-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f565-139">INPUTS</span></span>

### <span data-ttu-id="7f565-140">Нет</span><span class="sxs-lookup"><span data-stu-id="7f565-140">None</span></span>

## <span data-ttu-id="7f565-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f565-141">OUTPUTS</span></span>

### <span data-ttu-id="7f565-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7f565-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="7f565-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f565-143">NOTES</span></span>

## <span data-ttu-id="7f565-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f565-144">RELATED LINKS</span></span>
