---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410156"
---
# <span data-ttu-id="2a3f4-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a3f4-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="2a3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3f4-103">Получает конфигурацию переднего IP-адреса в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="2a3f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a3f4-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a3f4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="2a3f4-106">Для **этого вы** можете выбрать переднюю конфигурацию IP-адреса или список конфигураций переднего IP-адреса в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="2a3f4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a3f4-107">EXAMPLES</span></span>

### <span data-ttu-id="2a3f4-108">Пример 1. Настройка переднего IP-адреса в балансире нагрузки</span><span class="sxs-lookup"><span data-stu-id="2a3f4-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="2a3f4-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="2a3f4-110">Вторая команда получает конфигурацию переднего IP-адреса, связанную с этим балансировом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="2a3f4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a3f4-111">PARAMETERS</span></span>

### <span data-ttu-id="2a3f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3f4-112">-DefaultProfile</span></span>
<span data-ttu-id="2a3f4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a3f4-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a3f4-114">-LoadBalancer</span></span>
<span data-ttu-id="2a3f4-115">Определяет балансировку нагрузки, связанную с ip-конфигурацией переднего ip-адреса, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="2a3f4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2a3f4-116">-Name</span></span>
<span data-ttu-id="2a3f4-117">Указывает имя балансира нагрузки, который содержит ip-конфигурацию переднего ip-адреса, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="2a3f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3f4-118">CommonParameters</span></span>
<span data-ttu-id="2a3f4-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a3f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3f4-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a3f4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3f4-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a3f4-121">INPUTS</span></span>

### <span data-ttu-id="2a3f4-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a3f4-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2a3f4-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a3f4-123">OUTPUTS</span></span>

### <span data-ttu-id="2a3f4-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a3f4-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="2a3f4-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a3f4-125">NOTES</span></span>

## <span data-ttu-id="2a3f4-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a3f4-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a3f4-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a3f4-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2a3f4-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a3f4-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2a3f4-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a3f4-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2a3f4-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a3f4-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2a3f4-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a3f4-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

