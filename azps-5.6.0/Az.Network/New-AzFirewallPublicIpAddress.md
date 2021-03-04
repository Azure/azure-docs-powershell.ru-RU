---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: 2e7c1b0468ed3faf37c8f11bc0cb1eca707195bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958547"
---
# <span data-ttu-id="7f47c-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f47c-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="7f47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f47c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f47c-103">Это место для IP-адреса, которое можно использовать для много pip в брандмауэре Azure.</span><span class="sxs-lookup"><span data-stu-id="7f47c-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="7f47c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f47c-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f47c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f47c-105">DESCRIPTION</span></span>
<span data-ttu-id="7f47c-106">Это место для IP-адреса, которое можно использовать для много pip в брандмауэре Azure.</span><span class="sxs-lookup"><span data-stu-id="7f47c-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="7f47c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f47c-107">EXAMPLES</span></span>

### <span data-ttu-id="7f47c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f47c-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="7f47c-109">$publicIp будет использовать в этом адресе ip-адрес 20.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="7f47c-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="7f47c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f47c-110">PARAMETERS</span></span>

### <span data-ttu-id="7f47c-111">-Address</span><span class="sxs-lookup"><span data-stu-id="7f47c-111">-Address</span></span>
<span data-ttu-id="7f47c-112">IP-адреса брандмауэра, подключенного к центру</span><span class="sxs-lookup"><span data-stu-id="7f47c-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="7f47c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f47c-113">-DefaultProfile</span></span>
<span data-ttu-id="7f47c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f47c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f47c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f47c-115">-Confirm</span></span>
<span data-ttu-id="7f47c-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f47c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f47c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f47c-117">-WhatIf</span></span>
<span data-ttu-id="7f47c-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f47c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f47c-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f47c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f47c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f47c-120">CommonParameters</span></span>
<span data-ttu-id="7f47c-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f47c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f47c-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f47c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f47c-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f47c-123">INPUTS</span></span>

### <span data-ttu-id="7f47c-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7f47c-124">None</span></span>

## <span data-ttu-id="7f47c-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f47c-125">OUTPUTS</span></span>

### <span data-ttu-id="7f47c-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7f47c-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="7f47c-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f47c-127">NOTES</span></span>

## <span data-ttu-id="7f47c-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f47c-128">RELATED LINKS</span></span>
