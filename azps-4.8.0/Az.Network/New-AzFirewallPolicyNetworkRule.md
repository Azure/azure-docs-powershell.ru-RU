---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234993"
---
# <span data-ttu-id="8a052-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8a052-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="8a052-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a052-102">SYNOPSIS</span></span>
<span data-ttu-id="8a052-103">Создание нового сетевого правила для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="8a052-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="8a052-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a052-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a052-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a052-105">DESCRIPTION</span></span>
<span data-ttu-id="8a052-106">Командлет **New-AzFirewallPolicyNetworkRule** создает сетевое правило для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8a052-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="8a052-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a052-107">EXAMPLES</span></span>

### <span data-ttu-id="8a052-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a052-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="8a052-109">В этом примере создается сетевое правило с исходным адресом, протоколом, адресом назначения и портом назначения.</span><span class="sxs-lookup"><span data-stu-id="8a052-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="8a052-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a052-110">PARAMETERS</span></span>

### <span data-ttu-id="8a052-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a052-111">-DefaultProfile</span></span>
<span data-ttu-id="8a052-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a052-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a052-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="8a052-113">-Description</span></span>
<span data-ttu-id="8a052-114">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-114">The description of the rule</span></span>

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

### <span data-ttu-id="8a052-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8a052-115">-DestinationAddress</span></span>
<span data-ttu-id="8a052-116">Адреса назначения правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="8a052-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="8a052-117">-DestinationFqdn</span></span>
<span data-ttu-id="8a052-118">Полное доменное имя назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="8a052-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="8a052-119">-DestinationIpGroup</span></span>
<span data-ttu-id="8a052-120">Конечная ipgroups правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="8a052-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8a052-121">-DestinationPort</span></span>
<span data-ttu-id="8a052-122">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="8a052-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a052-123">-Name</span></span>
<span data-ttu-id="8a052-124">Имя сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="8a052-125">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8a052-125">-Protocol</span></span>
<span data-ttu-id="8a052-126">Протоколы правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="8a052-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="8a052-127">-SourceAddress</span></span>
<span data-ttu-id="8a052-128">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="8a052-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="8a052-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="8a052-129">-SourceIpGroup</span></span>
<span data-ttu-id="8a052-130">Исходная ipgroups правила</span><span class="sxs-lookup"><span data-stu-id="8a052-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="8a052-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a052-131">-Confirm</span></span>
<span data-ttu-id="8a052-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a052-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a052-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a052-133">-WhatIf</span></span>
<span data-ttu-id="8a052-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a052-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a052-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a052-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a052-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a052-136">CommonParameters</span></span>
<span data-ttu-id="8a052-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a052-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a052-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a052-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a052-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a052-139">INPUTS</span></span>

### <span data-ttu-id="8a052-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="8a052-140">None</span></span>

## <span data-ttu-id="8a052-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a052-141">OUTPUTS</span></span>

### <span data-ttu-id="8a052-142">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8a052-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="8a052-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a052-143">NOTES</span></span>

## <span data-ttu-id="8a052-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a052-144">RELATED LINKS</span></span>
