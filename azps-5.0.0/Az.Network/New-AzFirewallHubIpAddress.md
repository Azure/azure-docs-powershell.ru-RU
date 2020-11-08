---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248324"
---
# <span data-ttu-id="d76df-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="d76df-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="d76df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d76df-102">SYNOPSIS</span></span>
<span data-ttu-id="d76df-103">IP-адреса assoicated в брандмауэр на виртуальном концентраторе</span><span class="sxs-lookup"><span data-stu-id="d76df-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="d76df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d76df-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d76df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d76df-105">DESCRIPTION</span></span>
<span data-ttu-id="d76df-106">IP-адреса assoicated в брандмауэр на виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="d76df-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="d76df-107">Они могут быть общедоступными и частными адресами</span><span class="sxs-lookup"><span data-stu-id="d76df-107">These can be public and private addresses</span></span>

## <span data-ttu-id="d76df-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d76df-108">EXAMPLES</span></span>

### <span data-ttu-id="d76df-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d76df-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="d76df-110">В этом примере создается объект IP-адреса Hub со счетом из двух общедоступных адресов.</span><span class="sxs-lookup"><span data-stu-id="d76df-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="d76df-111">Объект HubIPAddress ssociated в брандмауэр на виртуальном концентраторе.</span><span class="sxs-lookup"><span data-stu-id="d76df-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="d76df-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d76df-112">PARAMETERS</span></span>

### <span data-ttu-id="d76df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76df-113">-DefaultProfile</span></span>
<span data-ttu-id="d76df-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d76df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d76df-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="d76df-115">-PrivateIPAddress</span></span>
<span data-ttu-id="d76df-116">Частный IP-адрес брандмауэра, подключенного к концентратору</span><span class="sxs-lookup"><span data-stu-id="d76df-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="d76df-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="d76df-117">-PublicIPs</span></span>
<span data-ttu-id="d76df-118">IP-адреса брандмауэра, подключенного к концентратору</span><span class="sxs-lookup"><span data-stu-id="d76df-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d76df-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d76df-119">-Confirm</span></span>
<span data-ttu-id="d76df-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d76df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d76df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d76df-121">-WhatIf</span></span>
<span data-ttu-id="d76df-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d76df-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d76df-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d76df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d76df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76df-124">CommonParameters</span></span>
<span data-ttu-id="d76df-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d76df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76df-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d76df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76df-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d76df-127">INPUTS</span></span>

### <span data-ttu-id="d76df-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="d76df-128">None</span></span>

## <span data-ttu-id="d76df-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d76df-129">OUTPUTS</span></span>

### <span data-ttu-id="d76df-130">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="d76df-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="d76df-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d76df-131">NOTES</span></span>

## <span data-ttu-id="d76df-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d76df-132">RELATED LINKS</span></span>
