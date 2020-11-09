---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317954"
---
# <span data-ttu-id="db676-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="db676-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="db676-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db676-102">SYNOPSIS</span></span>
<span data-ttu-id="db676-103">Возвращает конфигурацию внутреннего адреса подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="db676-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="db676-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db676-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db676-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db676-105">DESCRIPTION</span></span>
<span data-ttu-id="db676-106">Возвращает конфигурацию внутреннего адреса подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="db676-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="db676-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db676-107">EXAMPLES</span></span>

### <span data-ttu-id="db676-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db676-108">Example 1</span></span>
### <span data-ttu-id="db676-109">Пример 2: Новая конфигурация адреса подсистемы балансировки нагрузки со ссылкой на виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="db676-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="db676-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db676-110">PARAMETERS</span></span>

### <span data-ttu-id="db676-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db676-111">-DefaultProfile</span></span>
<span data-ttu-id="db676-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db676-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db676-113">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="db676-113">-IpAddress</span></span>
<span data-ttu-id="db676-114">IP-адрес, который нужно добавить в пул серверной части</span><span class="sxs-lookup"><span data-stu-id="db676-114">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db676-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db676-115">-Name</span></span>
<span data-ttu-id="db676-116">Имя конфигурации серверного адреса</span><span class="sxs-lookup"><span data-stu-id="db676-116">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db676-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="db676-117">-VirtualNetworkId</span></span>
<span data-ttu-id="db676-118">Виртуальная сеть, связанная с конфигурацией адресного сервера</span><span class="sxs-lookup"><span data-stu-id="db676-118">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db676-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db676-119">-Confirm</span></span>
<span data-ttu-id="db676-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db676-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db676-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db676-121">-WhatIf</span></span>
<span data-ttu-id="db676-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db676-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db676-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db676-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db676-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db676-124">CommonParameters</span></span>
<span data-ttu-id="db676-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db676-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db676-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db676-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db676-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db676-127">INPUTS</span></span>

### <span data-ttu-id="db676-128">System. String</span><span class="sxs-lookup"><span data-stu-id="db676-128">System.String</span></span>

### <span data-ttu-id="db676-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="db676-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="db676-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db676-130">OUTPUTS</span></span>

### <span data-ttu-id="db676-131">Microsoft. Azure. Commands. Network. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="db676-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="db676-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="db676-132">NOTES</span></span>

## <span data-ttu-id="db676-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db676-133">RELATED LINKS</span></span>
