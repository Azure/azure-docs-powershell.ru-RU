---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236780"
---
# <span data-ttu-id="59604-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="59604-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="59604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59604-102">SYNOPSIS</span></span>
<span data-ttu-id="59604-103">Это место для IP-адреса, которое можно использовать для много pip в брандмауэре Azure.</span><span class="sxs-lookup"><span data-stu-id="59604-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="59604-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59604-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59604-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59604-105">DESCRIPTION</span></span>
<span data-ttu-id="59604-106">Это место для IP-адреса, которое можно использовать для много pip в брандмауэре Azure.</span><span class="sxs-lookup"><span data-stu-id="59604-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="59604-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59604-107">EXAMPLES</span></span>

### <span data-ttu-id="59604-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59604-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="59604-109">$publicIp будет использовать в этом адресе ip-адрес 20.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="59604-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="59604-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59604-110">PARAMETERS</span></span>

### <span data-ttu-id="59604-111">-Address</span><span class="sxs-lookup"><span data-stu-id="59604-111">-Address</span></span>
<span data-ttu-id="59604-112">IP-адреса брандмауэра, подключенного к концентратору</span><span class="sxs-lookup"><span data-stu-id="59604-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="59604-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59604-113">-DefaultProfile</span></span>
<span data-ttu-id="59604-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59604-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59604-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59604-115">-Confirm</span></span>
<span data-ttu-id="59604-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="59604-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59604-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59604-117">-WhatIf</span></span>
<span data-ttu-id="59604-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59604-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59604-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="59604-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59604-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59604-120">CommonParameters</span></span>
<span data-ttu-id="59604-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59604-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59604-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59604-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59604-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59604-123">INPUTS</span></span>

### <span data-ttu-id="59604-124">Нет</span><span class="sxs-lookup"><span data-stu-id="59604-124">None</span></span>

## <span data-ttu-id="59604-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59604-125">OUTPUTS</span></span>

### <span data-ttu-id="59604-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="59604-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="59604-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59604-127">NOTES</span></span>

## <span data-ttu-id="59604-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59604-128">RELATED LINKS</span></span>
