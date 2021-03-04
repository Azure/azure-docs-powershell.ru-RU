---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 86e15e54a0091839bdce6a66f891c12e6c0376f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007736"
---
# <span data-ttu-id="22b28-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="22b28-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="22b28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22b28-102">SYNOPSIS</span></span>
<span data-ttu-id="22b28-103">Создание правила сети брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="22b28-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="22b28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22b28-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22b28-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22b28-105">DESCRIPTION</span></span>
<span data-ttu-id="22b28-106">Командлет **New-AzFirewallPolicyNetworkRule** создает правило сети для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="22b28-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="22b28-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22b28-107">EXAMPLES</span></span>

### <span data-ttu-id="22b28-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22b28-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="22b28-109">В этом примере создается правило сети с исходным адресом, протоколом, адресом назначения и портом назначения.</span><span class="sxs-lookup"><span data-stu-id="22b28-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="22b28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22b28-110">PARAMETERS</span></span>

### <span data-ttu-id="22b28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b28-111">-DefaultProfile</span></span>
<span data-ttu-id="22b28-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22b28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b28-113">-Description</span><span class="sxs-lookup"><span data-stu-id="22b28-113">-Description</span></span>
<span data-ttu-id="22b28-114">Описание правила</span><span class="sxs-lookup"><span data-stu-id="22b28-114">The description of the rule</span></span>

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

### <span data-ttu-id="22b28-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="22b28-115">-DestinationAddress</span></span>
<span data-ttu-id="22b28-116">Адреса назначения правила</span><span class="sxs-lookup"><span data-stu-id="22b28-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="22b28-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="22b28-117">-DestinationFqdn</span></span>
<span data-ttu-id="22b28-118">Конечное FQDN правила</span><span class="sxs-lookup"><span data-stu-id="22b28-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="22b28-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="22b28-119">-DestinationIpGroup</span></span>
<span data-ttu-id="22b28-120">Ipgroups назначения правила</span><span class="sxs-lookup"><span data-stu-id="22b28-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="22b28-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="22b28-121">-DestinationPort</span></span>
<span data-ttu-id="22b28-122">Порты назначения правила</span><span class="sxs-lookup"><span data-stu-id="22b28-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="22b28-123">-Name</span><span class="sxs-lookup"><span data-stu-id="22b28-123">-Name</span></span>
<span data-ttu-id="22b28-124">Имя правила сети</span><span class="sxs-lookup"><span data-stu-id="22b28-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="22b28-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="22b28-125">-Protocol</span></span>
<span data-ttu-id="22b28-126">Протоколы правила</span><span class="sxs-lookup"><span data-stu-id="22b28-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="22b28-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="22b28-127">-SourceAddress</span></span>
<span data-ttu-id="22b28-128">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="22b28-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="22b28-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="22b28-129">-SourceIpGroup</span></span>
<span data-ttu-id="22b28-130">Исходные IP-группы правила</span><span class="sxs-lookup"><span data-stu-id="22b28-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="22b28-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22b28-131">-Confirm</span></span>
<span data-ttu-id="22b28-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22b28-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b28-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b28-133">-WhatIf</span></span>
<span data-ttu-id="22b28-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22b28-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b28-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22b28-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b28-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b28-136">CommonParameters</span></span>
<span data-ttu-id="22b28-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b28-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b28-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22b28-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b28-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22b28-139">INPUTS</span></span>

### <span data-ttu-id="22b28-140">Нет</span><span class="sxs-lookup"><span data-stu-id="22b28-140">None</span></span>

## <span data-ttu-id="22b28-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22b28-141">OUTPUTS</span></span>

### <span data-ttu-id="22b28-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="22b28-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="22b28-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22b28-143">NOTES</span></span>

## <span data-ttu-id="22b28-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22b28-144">RELATED LINKS</span></span>
