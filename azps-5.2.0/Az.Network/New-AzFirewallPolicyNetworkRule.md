---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327085"
---
# <span data-ttu-id="035e2-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="035e2-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="035e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="035e2-102">SYNOPSIS</span></span>
<span data-ttu-id="035e2-103">Создание правила сети брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="035e2-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="035e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="035e2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="035e2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="035e2-105">DESCRIPTION</span></span>
<span data-ttu-id="035e2-106">Командлет **New-AzFirewallPolicyNetworkRule** создает правило сети для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="035e2-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="035e2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="035e2-107">EXAMPLES</span></span>

### <span data-ttu-id="035e2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="035e2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="035e2-109">В этом примере создается правило сети с исходным адресом, протоколом, адресом назначения и портом назначения.</span><span class="sxs-lookup"><span data-stu-id="035e2-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="035e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="035e2-110">PARAMETERS</span></span>

### <span data-ttu-id="035e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035e2-111">-DefaultProfile</span></span>
<span data-ttu-id="035e2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="035e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="035e2-113">-Description</span><span class="sxs-lookup"><span data-stu-id="035e2-113">-Description</span></span>
<span data-ttu-id="035e2-114">Описание правила</span><span class="sxs-lookup"><span data-stu-id="035e2-114">The description of the rule</span></span>

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

### <span data-ttu-id="035e2-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="035e2-115">-DestinationAddress</span></span>
<span data-ttu-id="035e2-116">Адреса назначения правила</span><span class="sxs-lookup"><span data-stu-id="035e2-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="035e2-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="035e2-117">-DestinationFqdn</span></span>
<span data-ttu-id="035e2-118">Конечное FQDN правила</span><span class="sxs-lookup"><span data-stu-id="035e2-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="035e2-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="035e2-119">-DestinationIpGroup</span></span>
<span data-ttu-id="035e2-120">Ipgroups назначения правила</span><span class="sxs-lookup"><span data-stu-id="035e2-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="035e2-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="035e2-121">-DestinationPort</span></span>
<span data-ttu-id="035e2-122">Порты назначения правила</span><span class="sxs-lookup"><span data-stu-id="035e2-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="035e2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="035e2-123">-Name</span></span>
<span data-ttu-id="035e2-124">Имя правила сети</span><span class="sxs-lookup"><span data-stu-id="035e2-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="035e2-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="035e2-125">-Protocol</span></span>
<span data-ttu-id="035e2-126">Протоколы правила</span><span class="sxs-lookup"><span data-stu-id="035e2-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="035e2-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="035e2-127">-SourceAddress</span></span>
<span data-ttu-id="035e2-128">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="035e2-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="035e2-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="035e2-129">-SourceIpGroup</span></span>
<span data-ttu-id="035e2-130">Исходные IP-группы правила</span><span class="sxs-lookup"><span data-stu-id="035e2-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="035e2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="035e2-131">-Confirm</span></span>
<span data-ttu-id="035e2-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035e2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035e2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035e2-133">-WhatIf</span></span>
<span data-ttu-id="035e2-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035e2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="035e2-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="035e2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035e2-136">CommonParameters</span></span>
<span data-ttu-id="035e2-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035e2-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="035e2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035e2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="035e2-139">INPUTS</span></span>

### <span data-ttu-id="035e2-140">Нет</span><span class="sxs-lookup"><span data-stu-id="035e2-140">None</span></span>

## <span data-ttu-id="035e2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="035e2-141">OUTPUTS</span></span>

### <span data-ttu-id="035e2-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="035e2-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="035e2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="035e2-143">NOTES</span></span>

## <span data-ttu-id="035e2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="035e2-144">RELATED LINKS</span></span>
