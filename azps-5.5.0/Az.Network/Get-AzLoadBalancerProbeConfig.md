---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227905"
---
# <span data-ttu-id="5934d-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5934d-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5934d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5934d-102">SYNOPSIS</span></span>
<span data-ttu-id="5934d-103">Получает конфигурацию конфигурации для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5934d-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="5934d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5934d-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5934d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5934d-105">DESCRIPTION</span></span>
<span data-ttu-id="5934d-106">Для балансиров нагрузки с его стороны возвращается одна или несколько конфигураций **для get-AzLoadBalancerProbeConfig.**</span><span class="sxs-lookup"><span data-stu-id="5934d-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="5934d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5934d-107">EXAMPLES</span></span>

### <span data-ttu-id="5934d-108">Пример 1. Настройка баланса нагрузки</span><span class="sxs-lookup"><span data-stu-id="5934d-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="5934d-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="5934d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="5934d-110">Вторая команда получает связанную конфигурацию с именем MyProbe из балансиров нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="5934d-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="5934d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5934d-111">PARAMETERS</span></span>

### <span data-ttu-id="5934d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5934d-112">-DefaultProfile</span></span>
<span data-ttu-id="5934d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5934d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5934d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5934d-114">-LoadBalancer</span></span>
<span data-ttu-id="5934d-115">Определяет балансировую нагрузку, связанную с конфигурацией, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="5934d-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="5934d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5934d-116">-Name</span></span>
<span data-ttu-id="5934d-117">Указывает имя конфигурации, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="5934d-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="5934d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5934d-118">CommonParameters</span></span>
<span data-ttu-id="5934d-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5934d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5934d-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5934d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5934d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5934d-121">INPUTS</span></span>

### <span data-ttu-id="5934d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5934d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5934d-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5934d-123">OUTPUTS</span></span>

### <span data-ttu-id="5934d-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="5934d-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="5934d-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5934d-125">NOTES</span></span>

## <span data-ttu-id="5934d-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5934d-126">RELATED LINKS</span></span>

[<span data-ttu-id="5934d-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5934d-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5934d-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5934d-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5934d-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5934d-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5934d-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5934d-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5934d-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5934d-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


