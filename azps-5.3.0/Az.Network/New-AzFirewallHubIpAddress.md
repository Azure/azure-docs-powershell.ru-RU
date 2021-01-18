---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506943"
---
# <span data-ttu-id="8bbe9-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bbe9-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="8bbe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="8bbe9-103">Ip addresses assoicated to the firewall on virtual hub</span><span class="sxs-lookup"><span data-stu-id="8bbe9-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="8bbe9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8bbe9-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bbe9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bbe9-105">DESCRIPTION</span></span>
<span data-ttu-id="8bbe9-106">Ip-адреса, которые ассоциированы с брандмауэром в виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="8bbe9-107">Это могут быть как общедоступные, так и частные адреса.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-107">These can be public and private addresses</span></span>

## <span data-ttu-id="8bbe9-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8bbe9-108">EXAMPLES</span></span>

### <span data-ttu-id="8bbe9-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bbe9-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="8bbe9-110">В этом примере создается IP-адрес концентратора с количеством общедоступных IP-адресов (2).</span><span class="sxs-lookup"><span data-stu-id="8bbe9-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="8bbe9-111">Объект HubIPAddress передается в брандмауэр в виртуальном центре.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="8bbe9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bbe9-112">PARAMETERS</span></span>

### <span data-ttu-id="8bbe9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bbe9-113">-DefaultProfile</span></span>
<span data-ttu-id="8bbe9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bbe9-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="8bbe9-115">-PrivateIPAddress</span></span>
<span data-ttu-id="8bbe9-116">Личный IP-адрес брандмауэра, подключенного к центру</span><span class="sxs-lookup"><span data-stu-id="8bbe9-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="8bbe9-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="8bbe9-117">-PublicIPs</span></span>
<span data-ttu-id="8bbe9-118">IP-адреса брандмауэра, подключенного к центру</span><span class="sxs-lookup"><span data-stu-id="8bbe9-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="8bbe9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bbe9-119">-Confirm</span></span>
<span data-ttu-id="8bbe9-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bbe9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bbe9-121">-WhatIf</span></span>
<span data-ttu-id="8bbe9-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8bbe9-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bbe9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bbe9-124">CommonParameters</span></span>
<span data-ttu-id="8bbe9-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bbe9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bbe9-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bbe9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bbe9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bbe9-127">INPUTS</span></span>

### <span data-ttu-id="8bbe9-128">Нет</span><span class="sxs-lookup"><span data-stu-id="8bbe9-128">None</span></span>

## <span data-ttu-id="8bbe9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8bbe9-129">OUTPUTS</span></span>

### <span data-ttu-id="8bbe9-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="8bbe9-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="8bbe9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8bbe9-131">NOTES</span></span>

## <span data-ttu-id="8bbe9-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bbe9-132">RELATED LINKS</span></span>
