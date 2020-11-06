---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9840476e64c78293b747f96d1a689a3ce5099bff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558991"
---
# <span data-ttu-id="ff2f6-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff2f6-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ff2f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2f6-103">Удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff2f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff2f6-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff2f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ff2f6-106">Командлет **Remove-AzureRmLoadBalancerProbeConfig** удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="ff2f6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ff2f6-108">Пример 1: Удаление конфигурации зонда из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="ff2f6-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ff2f6-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="ff2f6-110">Вторая команда удаляет конфигурацию с именем MyProbe из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="ff2f6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff2f6-111">PARAMETERS</span></span>

### <span data-ttu-id="ff2f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2f6-112">-DefaultProfile</span></span>
<span data-ttu-id="ff2f6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2f6-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="ff2f6-114">-LoadBalancer</span></span>
<span data-ttu-id="ff2f6-115">Указывает подсистему балансировки нагрузки, которая содержит конфигурацию зонда, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff2f6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff2f6-116">-Name</span></span>
<span data-ttu-id="ff2f6-117">Указывает имя конфигурации зонда, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ff2f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2f6-118">CommonParameters</span></span>
<span data-ttu-id="ff2f6-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2f6-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2f6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2f6-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff2f6-121">INPUTS</span></span>

### <span data-ttu-id="ff2f6-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff2f6-122">PSLoadBalancer</span></span>
<span data-ttu-id="ff2f6-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ff2f6-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ff2f6-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff2f6-124">OUTPUTS</span></span>

### <span data-ttu-id="ff2f6-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff2f6-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ff2f6-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff2f6-126">NOTES</span></span>

## <span data-ttu-id="ff2f6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff2f6-127">RELATED LINKS</span></span>

[<span data-ttu-id="ff2f6-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff2f6-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ff2f6-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ff2f6-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ff2f6-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff2f6-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ff2f6-131">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff2f6-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ff2f6-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff2f6-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


