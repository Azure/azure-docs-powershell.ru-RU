---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246229"
---
# <span data-ttu-id="e818d-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e818d-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e818d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e818d-102">SYNOPSIS</span></span>
<span data-ttu-id="e818d-103">Получает конфигурацию пула адресных адресов серверной подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e818d-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e818d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e818d-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e818d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e818d-105">DESCRIPTION</span></span>
<span data-ttu-id="e818d-106">Командлет **Get-AzLoadBalancerBackendAddressPoolConfig** возвращает один пул серверных адресов или список пулов серверных адресов в службе подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e818d-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="e818d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e818d-107">EXAMPLES</span></span>

### <span data-ttu-id="e818d-108">Пример 1: получение пула адресных адресов серверной части</span><span class="sxs-lookup"><span data-stu-id="e818d-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="e818d-109">Первая команда получает существующий балансировщик нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup и затем сохраняет его в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e818d-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="e818d-110">Вторая команда получает соответствующую конфигурацию пула адресных адресов серверной группы с именем BackendAddressPool02 для подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="e818d-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="e818d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e818d-111">PARAMETERS</span></span>

### <span data-ttu-id="e818d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e818d-112">-DefaultProfile</span></span>
<span data-ttu-id="e818d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e818d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e818d-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="e818d-114">-LoadBalancer</span></span>
<span data-ttu-id="e818d-115">Указывает подсистему балансировки нагрузки, связанную с пулом адресных адресов для получения.</span><span class="sxs-lookup"><span data-stu-id="e818d-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="e818d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e818d-116">-Name</span></span>
<span data-ttu-id="e818d-117">Указывает имя подсистемы балансировки нагрузки, содержащей необходимый пул серверных адресов.</span><span class="sxs-lookup"><span data-stu-id="e818d-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="e818d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e818d-118">CommonParameters</span></span>
<span data-ttu-id="e818d-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e818d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e818d-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e818d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e818d-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e818d-121">INPUTS</span></span>

### <span data-ttu-id="e818d-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e818d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e818d-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e818d-123">OUTPUTS</span></span>

### <span data-ttu-id="e818d-124">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e818d-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e818d-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e818d-125">NOTES</span></span>

## <span data-ttu-id="e818d-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e818d-126">RELATED LINKS</span></span>

[<span data-ttu-id="e818d-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e818d-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e818d-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e818d-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e818d-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e818d-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e818d-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e818d-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


