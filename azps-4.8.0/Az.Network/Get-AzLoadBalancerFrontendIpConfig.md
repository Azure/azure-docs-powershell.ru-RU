---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235050"
---
# <span data-ttu-id="da021-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da021-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="da021-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da021-102">SYNOPSIS</span></span>
<span data-ttu-id="da021-103">Получает интерфейсную конфигурацию IP в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="da021-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="da021-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da021-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da021-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da021-105">DESCRIPTION</span></span>
<span data-ttu-id="da021-106">Командлет **Get-AzLoadBalancerFrontendIpConfig** получает интерфейсную конфигурацию IP или список IP-конфигураций интерфейсов в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="da021-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="da021-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da021-107">EXAMPLES</span></span>

### <span data-ttu-id="da021-108">Пример 1: получение интерфейсной конфигурации IP в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="da021-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="da021-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="da021-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="da021-110">Вторая команда возвращает IP-конфигурацию переднего плана, связанную с этим балансировщикм нагрузки.</span><span class="sxs-lookup"><span data-stu-id="da021-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="da021-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da021-111">PARAMETERS</span></span>

### <span data-ttu-id="da021-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da021-112">-DefaultProfile</span></span>
<span data-ttu-id="da021-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da021-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da021-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="da021-114">-LoadBalancer</span></span>
<span data-ttu-id="da021-115">Указывает подсистему балансировки нагрузки, связанную с интерфейсной конфигурацией IP-интерфейса, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="da021-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="da021-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da021-116">-Name</span></span>
<span data-ttu-id="da021-117">Указывает имя подсистемы балансировки нагрузки, содержащей интерфейсную конфигурацию IP-адресов, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="da021-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="da021-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da021-118">CommonParameters</span></span>
<span data-ttu-id="da021-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da021-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da021-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da021-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da021-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da021-121">INPUTS</span></span>

### <span data-ttu-id="da021-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da021-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="da021-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da021-123">OUTPUTS</span></span>

### <span data-ttu-id="da021-124">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="da021-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="da021-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="da021-125">NOTES</span></span>

## <span data-ttu-id="da021-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da021-126">RELATED LINKS</span></span>

[<span data-ttu-id="da021-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da021-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da021-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da021-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="da021-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da021-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da021-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da021-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da021-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da021-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

