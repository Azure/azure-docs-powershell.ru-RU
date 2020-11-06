---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9a6999dc379a5a39acea9b17107cabf2cae5ee25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562428"
---
# <span data-ttu-id="0e992-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e992-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="0e992-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e992-102">SYNOPSIS</span></span>
<span data-ttu-id="0e992-103">Задает состояние цели для конфигурации зонда.</span><span class="sxs-lookup"><span data-stu-id="0e992-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e992-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e992-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e992-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e992-105">DESCRIPTION</span></span>
<span data-ttu-id="0e992-106">Командлет **Set-AzureRmLoadBalancerProbeConfig** задает состояние цели для конфигурации зонда.</span><span class="sxs-lookup"><span data-stu-id="0e992-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="0e992-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e992-107">EXAMPLES</span></span>

### <span data-ttu-id="0e992-108">Пример 1: изменение конфигурации зонда в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="0e992-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="0e992-109">Первая команда получает подсистему с именем MyLoadBalancer, а затем сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="0e992-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="0e992-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerProbeConfig, который добавляет в нее новую конфигурацию зонда.</span><span class="sxs-lookup"><span data-stu-id="0e992-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="0e992-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzureRmLoadBalancerProbeConfig** , задающую новую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="0e992-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="0e992-112">Обратите внимание, что необходимо указать несколько параметров, указанных в предыдущей команде, так как они необходимы для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="0e992-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="0e992-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e992-113">PARAMETERS</span></span>

### <span data-ttu-id="0e992-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0e992-114">-IntervalInSeconds</span></span>
<span data-ttu-id="0e992-115">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0e992-115">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e992-116">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="0e992-116">-LoadBalancer</span></span>
<span data-ttu-id="0e992-117">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0e992-117">Specifies a load balancer.</span></span>
<span data-ttu-id="0e992-118">Этот командлет задает состояние цели для конфигурации зонда для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0e992-118">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e992-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e992-119">-Name</span></span>
<span data-ttu-id="0e992-120">Указывает имя конфигурации зонда, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0e992-120">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="0e992-121">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="0e992-121">-Port</span></span>
<span data-ttu-id="0e992-122">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0e992-122">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e992-123">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="0e992-123">-ProbeCount</span></span>
<span data-ttu-id="0e992-124">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0e992-124">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e992-125">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="0e992-125">-Protocol</span></span>
<span data-ttu-id="0e992-126">Указывает протокол, который будет использоваться для зондирования.</span><span class="sxs-lookup"><span data-stu-id="0e992-126">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="0e992-127">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e992-127">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e992-128">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="0e992-128">-RequestPath</span></span>
<span data-ttu-id="0e992-129">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="0e992-129">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="0e992-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e992-130">-DefaultProfile</span></span>
<span data-ttu-id="0e992-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e992-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e992-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e992-132">CommonParameters</span></span>
<span data-ttu-id="0e992-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e992-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e992-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e992-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e992-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e992-135">INPUTS</span></span>

### <span data-ttu-id="0e992-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0e992-136">PSLoadBalancer</span></span>
<span data-ttu-id="0e992-137">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0e992-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0e992-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e992-138">OUTPUTS</span></span>

### <span data-ttu-id="0e992-139">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0e992-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0e992-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e992-140">NOTES</span></span>

## <span data-ttu-id="0e992-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e992-141">RELATED LINKS</span></span>

[<span data-ttu-id="0e992-142">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e992-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0e992-143">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0e992-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0e992-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e992-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0e992-145">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e992-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="0e992-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0e992-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


