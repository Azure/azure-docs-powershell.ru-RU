---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078903"
---
# <span data-ttu-id="59134-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="59134-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="59134-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59134-102">SYNOPSIS</span></span>
<span data-ttu-id="59134-103">Создание правила NAT для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="59134-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="59134-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59134-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59134-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59134-105">DESCRIPTION</span></span>
<span data-ttu-id="59134-106">Командлет **New-AzFirewallPolicyNatRule** создает правило NAT для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="59134-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="59134-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59134-107">EXAMPLES</span></span>

### <span data-ttu-id="59134-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59134-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="59134-109">В этом примере создается правило NAT с исходным адресом, протоколом, адресом назначения, конечным портом, адресом перевода и переводным портом.</span><span class="sxs-lookup"><span data-stu-id="59134-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="59134-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59134-110">PARAMETERS</span></span>

### <span data-ttu-id="59134-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59134-111">-DefaultProfile</span></span>
<span data-ttu-id="59134-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59134-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59134-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59134-113">-Name</span></span>
<span data-ttu-id="59134-114">Имя коллекции правил NAT</span><span class="sxs-lookup"><span data-stu-id="59134-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="59134-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="59134-115">-Description</span></span>
<span data-ttu-id="59134-116">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="59134-116">The description of the rule</span></span>

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

### <span data-ttu-id="59134-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="59134-117">-DestinationAddress</span></span>
<span data-ttu-id="59134-118">Конечные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="59134-118">The destination addresses of the rule.</span></span> <span data-ttu-id="59134-119">Оно должно быть общедоступным IP-адресом брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="59134-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="59134-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="59134-120">-DestinationPort</span></span>
<span data-ttu-id="59134-121">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="59134-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="59134-122">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="59134-122">-Protocols</span></span>
<span data-ttu-id="59134-123">Протоколы правила.</span><span class="sxs-lookup"><span data-stu-id="59134-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="59134-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="59134-124">-SourceAddress</span></span>
<span data-ttu-id="59134-125">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="59134-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="59134-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="59134-126">-SourceIpGroup</span></span>
<span data-ttu-id="59134-127">Исходная ipgroups правила</span><span class="sxs-lookup"><span data-stu-id="59134-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="59134-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="59134-128">-TranslatedAddress</span></span>
<span data-ttu-id="59134-129">Преобразованный адрес для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="59134-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="59134-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="59134-130">-TranslatedPort</span></span>
<span data-ttu-id="59134-131">Переводной порт для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="59134-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="59134-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59134-132">-Confirm</span></span>
<span data-ttu-id="59134-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59134-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59134-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59134-134">-WhatIf</span></span>
<span data-ttu-id="59134-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59134-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59134-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59134-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59134-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59134-137">CommonParameters</span></span>
<span data-ttu-id="59134-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59134-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59134-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59134-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59134-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59134-140">INPUTS</span></span>

### <span data-ttu-id="59134-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="59134-141">None</span></span>

## <span data-ttu-id="59134-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59134-142">OUTPUTS</span></span>

### <span data-ttu-id="59134-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="59134-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="59134-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="59134-144">NOTES</span></span>

## <span data-ttu-id="59134-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59134-145">RELATED LINKS</span></span>
