---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3fe5345e6d3cbad90d99f5a94e72873beaca7c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732794"
---
# <span data-ttu-id="00a7d-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00a7d-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="00a7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="00a7d-103">Задает состояние цели для конфигурации зонда.</span><span class="sxs-lookup"><span data-stu-id="00a7d-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00a7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00a7d-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="00a7d-106">Командлет **Set-AzureRmLoadBalancerProbeConfig** задает состояние цели для конфигурации зонда.</span><span class="sxs-lookup"><span data-stu-id="00a7d-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="00a7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00a7d-107">EXAMPLES</span></span>

### <span data-ttu-id="00a7d-108">Пример 1: изменение конфигурации зонда в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="00a7d-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="00a7d-109">Первая команда получает подсистему с именем MyLoadBalancer, а затем сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="00a7d-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="00a7d-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerProbeConfig, который добавляет в нее новую конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="00a7d-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="00a7d-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzureRmLoadBalancerProbeConfig** , задающую новую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="00a7d-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="00a7d-112">Обратите внимание, что необходимо указать несколько параметров, указанных в предыдущей команде, так как они необходимы для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="00a7d-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="00a7d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00a7d-113">PARAMETERS</span></span>

### <span data-ttu-id="00a7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a7d-114">-DefaultProfile</span></span>
<span data-ttu-id="00a7d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00a7d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00a7d-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="00a7d-116">-IntervalInSeconds</span></span>
<span data-ttu-id="00a7d-117">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00a7d-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00a7d-118">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="00a7d-118">-LoadBalancer</span></span>
<span data-ttu-id="00a7d-119">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00a7d-119">Specifies a load balancer.</span></span>
<span data-ttu-id="00a7d-120">Этот командлет задает состояние цели для конфигурации зонда для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="00a7d-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="00a7d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00a7d-121">-Name</span></span>
<span data-ttu-id="00a7d-122">Указывает имя конфигурации зонда, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="00a7d-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="00a7d-123">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="00a7d-123">-Port</span></span>
<span data-ttu-id="00a7d-124">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="00a7d-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00a7d-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="00a7d-125">-ProbeCount</span></span>
<span data-ttu-id="00a7d-126">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="00a7d-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00a7d-127">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="00a7d-127">-Protocol</span></span>
<span data-ttu-id="00a7d-128">Указывает протокол, который будет использоваться для зондирования.</span><span class="sxs-lookup"><span data-stu-id="00a7d-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="00a7d-129">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="00a7d-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00a7d-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="00a7d-130">-RequestPath</span></span>
<span data-ttu-id="00a7d-131">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="00a7d-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00a7d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00a7d-132">-Confirm</span></span>
<span data-ttu-id="00a7d-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00a7d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00a7d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a7d-134">-WhatIf</span></span>
<span data-ttu-id="00a7d-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00a7d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00a7d-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00a7d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00a7d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a7d-137">CommonParameters</span></span>
<span data-ttu-id="00a7d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00a7d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a7d-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00a7d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a7d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00a7d-140">INPUTS</span></span>

### <span data-ttu-id="00a7d-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00a7d-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="00a7d-142">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00a7d-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="00a7d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00a7d-143">OUTPUTS</span></span>

### <span data-ttu-id="00a7d-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00a7d-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="00a7d-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="00a7d-145">NOTES</span></span>

## <span data-ttu-id="00a7d-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00a7d-146">RELATED LINKS</span></span>

[<span data-ttu-id="00a7d-147">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00a7d-147">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="00a7d-148">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00a7d-148">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="00a7d-149">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00a7d-149">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="00a7d-150">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00a7d-150">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="00a7d-151">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00a7d-151">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


