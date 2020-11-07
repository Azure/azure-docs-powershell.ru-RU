---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911038"
---
# <span data-ttu-id="9f32c-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9f32c-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9f32c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f32c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f32c-103">Задает состояние цели для конфигурации зонда.</span><span class="sxs-lookup"><span data-stu-id="9f32c-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="9f32c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f32c-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f32c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f32c-105">DESCRIPTION</span></span>
<span data-ttu-id="9f32c-106">Командлет **Set-AzLoadBalancerProbeConfig** задает состояние цели для конфигурации зонда.</span><span class="sxs-lookup"><span data-stu-id="9f32c-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="9f32c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f32c-107">EXAMPLES</span></span>

### <span data-ttu-id="9f32c-108">Пример 1: изменение конфигурации зонда в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="9f32c-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="9f32c-109">Первая команда получает подсистему с именем MyLoadBalancer, а затем сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="9f32c-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="9f32c-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerProbeConfig, который добавляет в нее новую конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="9f32c-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="9f32c-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancerProbeConfig** , задающую новую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9f32c-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="9f32c-112">Обратите внимание, что необходимо указать несколько параметров, указанных в предыдущей команде, так как они необходимы для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="9f32c-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="9f32c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f32c-113">PARAMETERS</span></span>

### <span data-ttu-id="9f32c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f32c-114">-DefaultProfile</span></span>
<span data-ttu-id="9f32c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f32c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f32c-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9f32c-116">-IntervalInSeconds</span></span>
<span data-ttu-id="9f32c-117">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9f32c-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f32c-118">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="9f32c-118">-LoadBalancer</span></span>
<span data-ttu-id="9f32c-119">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9f32c-119">Specifies a load balancer.</span></span>
<span data-ttu-id="9f32c-120">Этот командлет задает состояние цели для конфигурации зонда для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9f32c-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f32c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f32c-121">-Name</span></span>
<span data-ttu-id="9f32c-122">Указывает имя конфигурации зонда, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9f32c-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f32c-123">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="9f32c-123">-Port</span></span>
<span data-ttu-id="9f32c-124">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9f32c-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f32c-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="9f32c-125">-ProbeCount</span></span>
<span data-ttu-id="9f32c-126">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9f32c-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f32c-127">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9f32c-127">-Protocol</span></span>
<span data-ttu-id="9f32c-128">Указывает протокол, который будет использоваться для зондирования.</span><span class="sxs-lookup"><span data-stu-id="9f32c-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="9f32c-129">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="9f32c-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f32c-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="9f32c-130">-RequestPath</span></span>
<span data-ttu-id="9f32c-131">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="9f32c-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="9f32c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f32c-132">CommonParameters</span></span>
<span data-ttu-id="9f32c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f32c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f32c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f32c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f32c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f32c-135">INPUTS</span></span>

### <span data-ttu-id="9f32c-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9f32c-136">PSLoadBalancer</span></span>
<span data-ttu-id="9f32c-137">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9f32c-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9f32c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f32c-138">OUTPUTS</span></span>

### <span data-ttu-id="9f32c-139">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9f32c-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9f32c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f32c-140">NOTES</span></span>

## <span data-ttu-id="9f32c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f32c-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f32c-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9f32c-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9f32c-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9f32c-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9f32c-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9f32c-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9f32c-145">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9f32c-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9f32c-146">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9f32c-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


