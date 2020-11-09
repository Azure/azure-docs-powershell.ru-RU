---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317957"
---
# <span data-ttu-id="329ee-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="329ee-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="329ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="329ee-102">SYNOPSIS</span></span>
<span data-ttu-id="329ee-103">Создание правила NAT для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="329ee-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="329ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="329ee-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="329ee-105">DESCRIPTION</span></span>
<span data-ttu-id="329ee-106">Командлет **New-AzFirewallPolicyNatRule** создает правило NAT для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="329ee-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="329ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="329ee-107">EXAMPLES</span></span>

### <span data-ttu-id="329ee-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="329ee-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="329ee-109">В этом примере создается правило NAT с исходным адресом, протоколом, адресом назначения, конечным портом, адресом перевода и переводным портом.</span><span class="sxs-lookup"><span data-stu-id="329ee-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="329ee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="329ee-110">PARAMETERS</span></span>

### <span data-ttu-id="329ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329ee-111">-DefaultProfile</span></span>
<span data-ttu-id="329ee-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="329ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="329ee-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="329ee-113">-Name</span></span>
<span data-ttu-id="329ee-114">Имя коллекции правил NAT</span><span class="sxs-lookup"><span data-stu-id="329ee-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="329ee-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="329ee-115">-Description</span></span>
<span data-ttu-id="329ee-116">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="329ee-116">The description of the rule</span></span>

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

### <span data-ttu-id="329ee-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="329ee-117">-DestinationAddress</span></span>
<span data-ttu-id="329ee-118">Конечные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="329ee-118">The destination addresses of the rule.</span></span> <span data-ttu-id="329ee-119">Оно должно быть общедоступным IP-адресом брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="329ee-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="329ee-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="329ee-120">-DestinationPort</span></span>
<span data-ttu-id="329ee-121">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="329ee-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="329ee-122">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="329ee-122">-Protocols</span></span>
<span data-ttu-id="329ee-123">Протоколы правила.</span><span class="sxs-lookup"><span data-stu-id="329ee-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="329ee-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="329ee-124">-SourceAddress</span></span>
<span data-ttu-id="329ee-125">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="329ee-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="329ee-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="329ee-126">-SourceIpGroup</span></span>
<span data-ttu-id="329ee-127">Исходная ipgroups правила</span><span class="sxs-lookup"><span data-stu-id="329ee-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="329ee-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="329ee-128">-TranslatedAddress</span></span>
<span data-ttu-id="329ee-129">Преобразованный адрес для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="329ee-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="329ee-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="329ee-130">-TranslatedPort</span></span>
<span data-ttu-id="329ee-131">Переводной порт для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="329ee-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="329ee-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="329ee-132">-Confirm</span></span>
<span data-ttu-id="329ee-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="329ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="329ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329ee-134">-WhatIf</span></span>
<span data-ttu-id="329ee-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="329ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329ee-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="329ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="329ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329ee-137">CommonParameters</span></span>
<span data-ttu-id="329ee-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="329ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329ee-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="329ee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329ee-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="329ee-140">INPUTS</span></span>

### <span data-ttu-id="329ee-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="329ee-141">None</span></span>

## <span data-ttu-id="329ee-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="329ee-142">OUTPUTS</span></span>

### <span data-ttu-id="329ee-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="329ee-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="329ee-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="329ee-144">NOTES</span></span>

## <span data-ttu-id="329ee-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="329ee-145">RELATED LINKS</span></span>
