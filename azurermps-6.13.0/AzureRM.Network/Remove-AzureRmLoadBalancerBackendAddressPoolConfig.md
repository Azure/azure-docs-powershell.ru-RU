---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 065aa3718f1a66949265e7dca39880c1eff21fa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732470"
---
# <span data-ttu-id="661d7-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="661d7-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="661d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="661d7-102">SYNOPSIS</span></span>
<span data-ttu-id="661d7-103">Удаляет конфигурацию пула адресных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="661d7-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="661d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="661d7-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="661d7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="661d7-105">DESCRIPTION</span></span>
<span data-ttu-id="661d7-106">Командлет **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** удаляет пул серверных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="661d7-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="661d7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="661d7-107">EXAMPLES</span></span>

### <span data-ttu-id="661d7-108">Пример 1: Удаление конфигурации пула адресов серверной части из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="661d7-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="661d7-109">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и передает ее в **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , удаляя конфигурацию BackendAddressPool02 из MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="661d7-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="661d7-110">Наконец, командлет Set-AzureRmLoadBalancer обновляет MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="661d7-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="661d7-111">Обратите внимание, что конфигурация пула адресных адресов сервера должна существовать, прежде чем ее можно будет удалить.</span><span class="sxs-lookup"><span data-stu-id="661d7-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="661d7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="661d7-112">PARAMETERS</span></span>

### <span data-ttu-id="661d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661d7-113">-DefaultProfile</span></span>
<span data-ttu-id="661d7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="661d7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661d7-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="661d7-115">-LoadBalancer</span></span>
<span data-ttu-id="661d7-116">Указывает подсистему балансировки нагрузки, которая содержит пул серверных адресов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="661d7-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="661d7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="661d7-117">-Name</span></span>
<span data-ttu-id="661d7-118">Указывает имя пула адресных адресов серверной платформы, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="661d7-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="661d7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="661d7-119">-Confirm</span></span>
<span data-ttu-id="661d7-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="661d7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661d7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="661d7-121">-WhatIf</span></span>
<span data-ttu-id="661d7-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="661d7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="661d7-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="661d7-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="661d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661d7-124">CommonParameters</span></span>
<span data-ttu-id="661d7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="661d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661d7-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661d7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661d7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="661d7-127">INPUTS</span></span>

### <span data-ttu-id="661d7-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661d7-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="661d7-129">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="661d7-129">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="661d7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="661d7-130">OUTPUTS</span></span>

### <span data-ttu-id="661d7-131">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661d7-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="661d7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="661d7-132">NOTES</span></span>

## <span data-ttu-id="661d7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="661d7-133">RELATED LINKS</span></span>

[<span data-ttu-id="661d7-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="661d7-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="661d7-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="661d7-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="661d7-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="661d7-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="661d7-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="661d7-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


