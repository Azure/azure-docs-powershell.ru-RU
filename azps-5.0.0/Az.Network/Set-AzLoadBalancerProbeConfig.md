---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247976"
---
# <span data-ttu-id="98858-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98858-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="98858-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98858-102">SYNOPSIS</span></span>
<span data-ttu-id="98858-103">Обновляет конфигурацию зонда для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98858-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="98858-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98858-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98858-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98858-105">DESCRIPTION</span></span>
<span data-ttu-id="98858-106">Командлет **Set-AzLoadBalancerProbeConfig** обновляет конфигурацию пробной версии для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98858-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="98858-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98858-107">EXAMPLES</span></span>

### <span data-ttu-id="98858-108">Пример 1: изменение конфигурации зонда в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="98858-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="98858-109">Первая команда получает подсистему с именем MyLoadBalancer, а затем сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="98858-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="98858-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerProbeConfig, который добавляет в нее новую конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="98858-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="98858-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancerProbeConfig** , задающую новую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="98858-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="98858-112">Обратите внимание, что необходимо указать несколько параметров, указанных в предыдущей команде, так как они необходимы для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="98858-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="98858-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98858-113">PARAMETERS</span></span>

### <span data-ttu-id="98858-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98858-114">-DefaultProfile</span></span>
<span data-ttu-id="98858-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98858-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98858-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="98858-116">-IntervalInSeconds</span></span>
<span data-ttu-id="98858-117">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98858-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="98858-118">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="98858-118">-LoadBalancer</span></span>
<span data-ttu-id="98858-119">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98858-119">Specifies a load balancer.</span></span>
<span data-ttu-id="98858-120">Этот командлет обновляет конфигурацию пробной версии для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="98858-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="98858-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98858-121">-Name</span></span>
<span data-ttu-id="98858-122">Указывает имя конфигурации зонда, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="98858-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="98858-123">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="98858-123">-Port</span></span>
<span data-ttu-id="98858-124">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="98858-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="98858-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="98858-125">-ProbeCount</span></span>
<span data-ttu-id="98858-126">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="98858-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="98858-127">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="98858-127">-Protocol</span></span>
<span data-ttu-id="98858-128">Указывает протокол, который будет использоваться для зондирования.</span><span class="sxs-lookup"><span data-stu-id="98858-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="98858-129">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="98858-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="98858-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="98858-130">-RequestPath</span></span>
<span data-ttu-id="98858-131">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="98858-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="98858-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98858-132">-Confirm</span></span>
<span data-ttu-id="98858-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98858-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98858-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98858-134">-WhatIf</span></span>
<span data-ttu-id="98858-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98858-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98858-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98858-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98858-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98858-137">CommonParameters</span></span>
<span data-ttu-id="98858-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98858-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98858-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98858-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98858-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98858-140">INPUTS</span></span>

### <span data-ttu-id="98858-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98858-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="98858-142">System. String</span><span class="sxs-lookup"><span data-stu-id="98858-142">System.String</span></span>

### <span data-ttu-id="98858-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="98858-143">System.Int32</span></span>

## <span data-ttu-id="98858-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98858-144">OUTPUTS</span></span>

### <span data-ttu-id="98858-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98858-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="98858-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="98858-146">NOTES</span></span>

## <span data-ttu-id="98858-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98858-147">RELATED LINKS</span></span>

[<span data-ttu-id="98858-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98858-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="98858-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="98858-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="98858-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98858-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="98858-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98858-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="98858-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98858-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


