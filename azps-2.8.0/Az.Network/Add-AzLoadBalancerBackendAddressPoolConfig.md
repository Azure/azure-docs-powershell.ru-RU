---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 9e353eb6682e4985ff278ddc8c0207bf0f1ab45b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903098"
---
# <span data-ttu-id="c634b-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c634b-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="c634b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c634b-102">SYNOPSIS</span></span>
<span data-ttu-id="c634b-103">Добавляет конфигурацию пула адресных баз данных в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c634b-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="c634b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c634b-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c634b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c634b-105">DESCRIPTION</span></span>
<span data-ttu-id="c634b-106">Командлет **Add-AzLoadBalancerBackend** добавляет пул серверных адресов в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="c634b-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="c634b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c634b-107">EXAMPLES</span></span>

### <span data-ttu-id="c634b-108">Пример 1. Добавление конфигурации пула адресов серверной части в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="c634b-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="c634b-109">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer, добавляет пул серверных адресов с именем BackendAddressPool02 в MyLoadBalancer, а затем использует командлет **Set-AzLoadBalancer** для обновления MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="c634b-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="c634b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c634b-110">PARAMETERS</span></span>

### <span data-ttu-id="c634b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c634b-111">-DefaultProfile</span></span>
<span data-ttu-id="c634b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c634b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c634b-113">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="c634b-113">-LoadBalancer</span></span>
<span data-ttu-id="c634b-114">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="c634b-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="c634b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c634b-115">-Name</span></span>
<span data-ttu-id="c634b-116">Указывает имя конфигурации пула адресов серверной базы данных, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="c634b-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="c634b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c634b-117">-Confirm</span></span>
<span data-ttu-id="c634b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c634b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c634b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c634b-119">-WhatIf</span></span>
<span data-ttu-id="c634b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c634b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c634b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c634b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c634b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c634b-122">CommonParameters</span></span>
<span data-ttu-id="c634b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c634b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c634b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c634b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c634b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c634b-125">INPUTS</span></span>

### <span data-ttu-id="c634b-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c634b-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c634b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c634b-127">OUTPUTS</span></span>

### <span data-ttu-id="c634b-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c634b-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c634b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c634b-129">NOTES</span></span>

## <span data-ttu-id="c634b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c634b-130">RELATED LINKS</span></span>

[<span data-ttu-id="c634b-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c634b-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c634b-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c634b-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="c634b-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c634b-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c634b-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c634b-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c634b-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c634b-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


