---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236055"
---
# <span data-ttu-id="ce517-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ce517-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="ce517-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce517-102">SYNOPSIS</span></span>
<span data-ttu-id="ce517-103">Это заполнитель для IP-адреса, который можно использовать для нескольких пунктов в брандмауэре Azure.</span><span class="sxs-lookup"><span data-stu-id="ce517-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="ce517-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce517-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce517-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce517-105">DESCRIPTION</span></span>
<span data-ttu-id="ce517-106">Это заполнитель для IP-адреса, который можно использовать для нескольких пунктов в брандмауэре Azure.</span><span class="sxs-lookup"><span data-stu-id="ce517-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="ce517-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce517-107">EXAMPLES</span></span>

### <span data-ttu-id="ce517-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce517-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="ce517-109">$publicIp будет заполнитель для IP-адреса 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="ce517-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="ce517-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce517-110">PARAMETERS</span></span>

### <span data-ttu-id="ce517-111">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="ce517-111">-Address</span></span>
<span data-ttu-id="ce517-112">IP-адреса брандмауэра, подключенного к концентратору</span><span class="sxs-lookup"><span data-stu-id="ce517-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="ce517-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce517-113">-DefaultProfile</span></span>
<span data-ttu-id="ce517-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce517-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce517-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce517-115">-Confirm</span></span>
<span data-ttu-id="ce517-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce517-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce517-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce517-117">-WhatIf</span></span>
<span data-ttu-id="ce517-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce517-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce517-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce517-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce517-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce517-120">CommonParameters</span></span>
<span data-ttu-id="ce517-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce517-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce517-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce517-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce517-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce517-123">INPUTS</span></span>

### <span data-ttu-id="ce517-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="ce517-124">None</span></span>

## <span data-ttu-id="ce517-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce517-125">OUTPUTS</span></span>

### <span data-ttu-id="ce517-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ce517-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="ce517-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce517-127">NOTES</span></span>

## <span data-ttu-id="ce517-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce517-128">RELATED LINKS</span></span>
