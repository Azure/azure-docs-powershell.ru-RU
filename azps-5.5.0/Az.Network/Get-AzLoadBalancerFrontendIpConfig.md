---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213945"
---
# <span data-ttu-id="98894-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98894-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="98894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98894-102">SYNOPSIS</span></span>
<span data-ttu-id="98894-103">Получает конфигурацию переднего IP-адреса в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98894-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="98894-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98894-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98894-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98894-105">DESCRIPTION</span></span>
<span data-ttu-id="98894-106">Для **этого вы** можете выбрать переднюю конфигурацию IP-адреса или список конфигураций переднего IP-адреса в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98894-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="98894-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98894-107">EXAMPLES</span></span>

### <span data-ttu-id="98894-108">Пример 1. Настройка переднего IP-адреса в балансире нагрузки</span><span class="sxs-lookup"><span data-stu-id="98894-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="98894-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="98894-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="98894-110">Вторая команда получает конфигурацию переднего IP-адреса, связанную с этим балансировом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98894-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="98894-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98894-111">PARAMETERS</span></span>

### <span data-ttu-id="98894-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98894-112">-DefaultProfile</span></span>
<span data-ttu-id="98894-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98894-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98894-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98894-114">-LoadBalancer</span></span>
<span data-ttu-id="98894-115">Определяет балансировку нагрузки, связанную с ip-конфигурацией переднего ip-адреса, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="98894-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="98894-116">-Name</span><span class="sxs-lookup"><span data-stu-id="98894-116">-Name</span></span>
<span data-ttu-id="98894-117">Указывает имя балансира нагрузки, который содержит ip-конфигурацию переднего ip-адреса, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="98894-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="98894-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98894-118">CommonParameters</span></span>
<span data-ttu-id="98894-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98894-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98894-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98894-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98894-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98894-121">INPUTS</span></span>

### <span data-ttu-id="98894-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98894-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="98894-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98894-123">OUTPUTS</span></span>

### <span data-ttu-id="98894-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="98894-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="98894-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98894-125">NOTES</span></span>

## <span data-ttu-id="98894-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98894-126">RELATED LINKS</span></span>

[<span data-ttu-id="98894-127">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98894-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="98894-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98894-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="98894-129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98894-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="98894-130">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98894-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="98894-131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="98894-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


