---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218577"
---
# <span data-ttu-id="9c8be-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9c8be-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="9c8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c8be-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8be-103">Создает правило брандмауэра сети.</span><span class="sxs-lookup"><span data-stu-id="9c8be-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="9c8be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c8be-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c8be-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c8be-105">DESCRIPTION</span></span>
<span data-ttu-id="9c8be-106">Командлет **New-AzFirewallNetworkRule** создает правило сети для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8be-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="9c8be-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c8be-107">EXAMPLES</span></span>

### <span data-ttu-id="9c8be-108">Пример 1. Создание правила для всего трафика TCP</span><span class="sxs-lookup"><span data-stu-id="9c8be-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="9c8be-109">В этом примере создается правило для всего трафика TCP.</span><span class="sxs-lookup"><span data-stu-id="9c8be-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="9c8be-110">Пользователь на основании связанного с ним правила в зависимости от того, будет ли разрешен трафик или запрещен для правила.</span><span class="sxs-lookup"><span data-stu-id="9c8be-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="9c8be-111">Пример 2. Создание правила для всего трафика TCP от 10.0.0.0 до 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="9c8be-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="9c8be-112">В этом примере создается правило для всего трафика TCP от 10.0.0.0 до 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="9c8be-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="9c8be-113">Пользователь на основании связанного с ним правила в зависимости от того, будет ли разрешен трафик или запрещен для правила.</span><span class="sxs-lookup"><span data-stu-id="9c8be-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="9c8be-114">Пример 3. Создание правила для всего трафика TCP и ICMP из любого источника до 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="9c8be-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="9c8be-115">В этом примере создается правило для всего трафика TCP из любого источника до 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="9c8be-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="9c8be-116">Пользователь на основании связанного с ним правила в зависимости от того, будет ли разрешен трафик или запрещен для правила.</span><span class="sxs-lookup"><span data-stu-id="9c8be-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="9c8be-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c8be-117">PARAMETERS</span></span>

### <span data-ttu-id="9c8be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8be-118">-DefaultProfile</span></span>
<span data-ttu-id="9c8be-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c8be-120">-Description</span><span class="sxs-lookup"><span data-stu-id="9c8be-120">-Description</span></span>
<span data-ttu-id="9c8be-121">Указывает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="9c8be-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9c8be-122">-DestinationAddress</span></span>
<span data-ttu-id="9c8be-123">Адреса назначения правила</span><span class="sxs-lookup"><span data-stu-id="9c8be-123">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="9c8be-124">-DestinationFqdn</span></span>
<span data-ttu-id="9c8be-125">Конечное FQDN правила</span><span class="sxs-lookup"><span data-stu-id="9c8be-125">The destination FQDN of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="9c8be-126">-DestinationIpGroup</span></span>
<span data-ttu-id="9c8be-127">Destination ipgroup of the rule</span><span class="sxs-lookup"><span data-stu-id="9c8be-127">The destination ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9c8be-128">-DestinationPort</span></span>
<span data-ttu-id="9c8be-129">Порты назначения правила</span><span class="sxs-lookup"><span data-stu-id="9c8be-129">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9c8be-130">-Name</span></span>
<span data-ttu-id="9c8be-131">Указывает имя этого правила сети.</span><span class="sxs-lookup"><span data-stu-id="9c8be-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="9c8be-132">Имя должно быть уникальным в наборе правил.</span><span class="sxs-lookup"><span data-stu-id="9c8be-132">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9c8be-133">-Protocol</span></span>
<span data-ttu-id="9c8be-134">Определяет тип трафика, отфильтрованного этим правилом.</span><span class="sxs-lookup"><span data-stu-id="9c8be-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="9c8be-135">Возможные значения: TCP, UDP, ICMP и Any.</span><span class="sxs-lookup"><span data-stu-id="9c8be-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9c8be-136">-SourceAddress</span></span>
<span data-ttu-id="9c8be-137">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="9c8be-137">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="9c8be-138">-SourceIpGroup</span></span>
<span data-ttu-id="9c8be-139">Ipgroup-источник правила</span><span class="sxs-lookup"><span data-stu-id="9c8be-139">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c8be-140">-Confirm</span></span>
<span data-ttu-id="9c8be-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c8be-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c8be-142">-WhatIf</span></span>
<span data-ttu-id="9c8be-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c8be-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c8be-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9c8be-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8be-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8be-145">CommonParameters</span></span>
<span data-ttu-id="9c8be-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c8be-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8be-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c8be-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8be-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c8be-148">INPUTS</span></span>

### <span data-ttu-id="9c8be-149">Нет</span><span class="sxs-lookup"><span data-stu-id="9c8be-149">None</span></span>

## <span data-ttu-id="9c8be-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c8be-150">OUTPUTS</span></span>

### <span data-ttu-id="9c8be-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9c8be-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="9c8be-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c8be-152">NOTES</span></span>

## <span data-ttu-id="9c8be-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c8be-153">RELATED LINKS</span></span>

[<span data-ttu-id="9c8be-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9c8be-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="9c8be-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9c8be-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="9c8be-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9c8be-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
