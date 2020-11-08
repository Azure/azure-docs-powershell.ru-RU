---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066287"
---
# <span data-ttu-id="49cad-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="49cad-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="49cad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49cad-102">SYNOPSIS</span></span>
<span data-ttu-id="49cad-103">Создание нового сетевого правила для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="49cad-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="49cad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49cad-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49cad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49cad-105">DESCRIPTION</span></span>
<span data-ttu-id="49cad-106">Командлет **New-AzFirewallPolicyNetworkRule** создает сетевое правило для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="49cad-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="49cad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49cad-107">EXAMPLES</span></span>

### <span data-ttu-id="49cad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49cad-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="49cad-109">В этом примере создается сетевое правило с исходным адресом, протоколом, адресом назначения и портом назначения.</span><span class="sxs-lookup"><span data-stu-id="49cad-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="49cad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49cad-110">PARAMETERS</span></span>

### <span data-ttu-id="49cad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cad-111">-DefaultProfile</span></span>
<span data-ttu-id="49cad-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49cad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49cad-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="49cad-113">-Description</span></span>
<span data-ttu-id="49cad-114">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="49cad-114">The description of the rule</span></span>

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

### <span data-ttu-id="49cad-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="49cad-115">-DestinationAddress</span></span>
<span data-ttu-id="49cad-116">Адреса назначения правила.</span><span class="sxs-lookup"><span data-stu-id="49cad-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="49cad-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="49cad-117">-DestinationPort</span></span>
<span data-ttu-id="49cad-118">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="49cad-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="49cad-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49cad-119">-Name</span></span>
<span data-ttu-id="49cad-120">Имя сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="49cad-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="49cad-121">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="49cad-121">-Protocols</span></span>
<span data-ttu-id="49cad-122">Протоколы правила.</span><span class="sxs-lookup"><span data-stu-id="49cad-122">The protocols of the rule</span></span>

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

### <span data-ttu-id="49cad-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="49cad-123">-SourceAddress</span></span>
<span data-ttu-id="49cad-124">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="49cad-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="49cad-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49cad-125">-Confirm</span></span>
<span data-ttu-id="49cad-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49cad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49cad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49cad-127">-WhatIf</span></span>
<span data-ttu-id="49cad-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49cad-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49cad-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49cad-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49cad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cad-130">CommonParameters</span></span>
<span data-ttu-id="49cad-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49cad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cad-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49cad-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cad-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49cad-133">INPUTS</span></span>

### <span data-ttu-id="49cad-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="49cad-134">None</span></span>

## <span data-ttu-id="49cad-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49cad-135">OUTPUTS</span></span>

### <span data-ttu-id="49cad-136">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="49cad-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="49cad-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="49cad-137">NOTES</span></span>

## <span data-ttu-id="49cad-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49cad-138">RELATED LINKS</span></span>
