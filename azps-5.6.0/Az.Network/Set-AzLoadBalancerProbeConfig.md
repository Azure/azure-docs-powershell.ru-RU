---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 2dd00c21a0badaca90419615df179299dc2d4240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003427"
---
# <span data-ttu-id="29da8-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="29da8-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="29da8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29da8-102">SYNOPSIS</span></span>
<span data-ttu-id="29da8-103">Обновляет конфигурацию формы для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="29da8-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="29da8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29da8-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29da8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29da8-105">DESCRIPTION</span></span>
<span data-ttu-id="29da8-106">Для **балансиента нагрузки сет-AzLoadBalancerProbeConfig** обновляется конфигурация захотеть.</span><span class="sxs-lookup"><span data-stu-id="29da8-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="29da8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29da8-107">EXAMPLES</span></span>

### <span data-ttu-id="29da8-108">Пример 1. Изменение конфигурации формы на балансе нагрузки</span><span class="sxs-lookup"><span data-stu-id="29da8-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="29da8-109">Первая команда получает балансирование MyLoadBalancer, а затем сохраняет его в $slb переменной.</span><span class="sxs-lookup"><span data-stu-id="29da8-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="29da8-110">Вторая команда использует оператор конвейера для переназначния балансиров нагрузки в $slb в Add-AzLoadBalancerProbeConfig, который добавляет в него новую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="29da8-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="29da8-111">Третья команда передает балансировку нагрузки в **set-AzLoadBalancerProbeConfig,** который задает новую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="29da8-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig**, which sets the new configuration.</span></span>
<span data-ttu-id="29da8-112">Обратите внимание, что необходимо указать несколько тех же параметров, которые были указаны в предыдущей команде, так как они являются необходимыми текущим командлетом.</span><span class="sxs-lookup"><span data-stu-id="29da8-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="29da8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29da8-113">PARAMETERS</span></span>

### <span data-ttu-id="29da8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29da8-114">-DefaultProfile</span></span>
<span data-ttu-id="29da8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29da8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29da8-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="29da8-116">-IntervalInSeconds</span></span>
<span data-ttu-id="29da8-117">Интервал (в секундах) между экземплярами службы с балансиза нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="29da8-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="29da8-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29da8-118">-LoadBalancer</span></span>
<span data-ttu-id="29da8-119">Определяет балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="29da8-119">Specifies a load balancer.</span></span>
<span data-ttu-id="29da8-120">Этот cmdlet обновляет конфигурацию формы для балансира нагрузки, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="29da8-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="29da8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="29da8-121">-Name</span></span>
<span data-ttu-id="29da8-122">Задает имя конфигурации, заданной этим набором cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29da8-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="29da8-123">-Port</span><span class="sxs-lookup"><span data-stu-id="29da8-123">-Port</span></span>
<span data-ttu-id="29da8-124">Указывает порт, по которому следует подключиться к службе с балансиза нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="29da8-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="29da8-125">-HorizonCount</span><span class="sxs-lookup"><span data-stu-id="29da8-125">-ProbeCount</span></span>
<span data-ttu-id="29da8-126">Количество последовательных неудач экземпляров, которые считаются неработоспособными.</span><span class="sxs-lookup"><span data-stu-id="29da8-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="29da8-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="29da8-127">-Protocol</span></span>
<span data-ttu-id="29da8-128">Протокол, который будет применяться для этого правила.</span><span class="sxs-lookup"><span data-stu-id="29da8-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="29da8-129">Допустимыми значениями для этого параметра являются Tcp или Http.</span><span class="sxs-lookup"><span data-stu-id="29da8-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="29da8-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="29da8-130">-RequestPath</span></span>
<span data-ttu-id="29da8-131">Путь к службе с балансиза нагрузкой, который будет задан для определения его состояния.</span><span class="sxs-lookup"><span data-stu-id="29da8-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="29da8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29da8-132">-Confirm</span></span>
<span data-ttu-id="29da8-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29da8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29da8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29da8-134">-WhatIf</span></span>
<span data-ttu-id="29da8-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29da8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29da8-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="29da8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29da8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29da8-137">CommonParameters</span></span>
<span data-ttu-id="29da8-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29da8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29da8-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29da8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29da8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29da8-140">INPUTS</span></span>

### <span data-ttu-id="29da8-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29da8-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="29da8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="29da8-142">System.String</span></span>

### <span data-ttu-id="29da8-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="29da8-143">System.Int32</span></span>

## <span data-ttu-id="29da8-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29da8-144">OUTPUTS</span></span>

### <span data-ttu-id="29da8-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29da8-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="29da8-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29da8-146">NOTES</span></span>

## <span data-ttu-id="29da8-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29da8-147">RELATED LINKS</span></span>

[<span data-ttu-id="29da8-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="29da8-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="29da8-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="29da8-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="29da8-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="29da8-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="29da8-151">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="29da8-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="29da8-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="29da8-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


