---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 9abff0880be98c01b4953957e719fc4e6553f6ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910137"
---
# <span data-ttu-id="79fae-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fae-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="79fae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79fae-102">SYNOPSIS</span></span>
<span data-ttu-id="79fae-103">Добавляет конфигурацию зонда в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79fae-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="79fae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79fae-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79fae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79fae-105">DESCRIPTION</span></span>
<span data-ttu-id="79fae-106">Командлет **Add-AzLoadBalancerProbeConfig** добавляет конфигурацию зонда в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="79fae-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="79fae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79fae-107">EXAMPLES</span></span>

### <span data-ttu-id="79fae-108">Пример 1. Добавление пробной конфигурации в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="79fae-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="79fae-109">Эта команда получает подсистему балансировки нагрузки с именем myLb, добавляет в нее указанную конфигурацию зонда, а затем использует командлет **Set-AzLoadBalancer** для обновления подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79fae-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="79fae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79fae-110">PARAMETERS</span></span>

### <span data-ttu-id="79fae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fae-111">-DefaultProfile</span></span>
<span data-ttu-id="79fae-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79fae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79fae-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="79fae-113">-IntervalInSeconds</span></span>
<span data-ttu-id="79fae-114">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79fae-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="79fae-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="79fae-115">-LoadBalancer</span></span>
<span data-ttu-id="79fae-116">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="79fae-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="79fae-117">Этот командлет добавляет конфигурацию зонда в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="79fae-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="79fae-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79fae-118">-Name</span></span>
<span data-ttu-id="79fae-119">Указывает имя конфигурации зонда, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="79fae-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="79fae-120">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="79fae-120">-Port</span></span>
<span data-ttu-id="79fae-121">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79fae-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="79fae-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="79fae-122">-ProbeCount</span></span>
<span data-ttu-id="79fae-123">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="79fae-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="79fae-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="79fae-124">-Protocol</span></span>
<span data-ttu-id="79fae-125">Указывает протокол для пробного использования.</span><span class="sxs-lookup"><span data-stu-id="79fae-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="79fae-126">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="79fae-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="79fae-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="79fae-127">-RequestPath</span></span>
<span data-ttu-id="79fae-128">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="79fae-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="79fae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fae-129">CommonParameters</span></span>
<span data-ttu-id="79fae-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79fae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fae-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fae-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fae-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79fae-132">INPUTS</span></span>

### <span data-ttu-id="79fae-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79fae-133">PSLoadBalancer</span></span>
<span data-ttu-id="79fae-134">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="79fae-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="79fae-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79fae-135">OUTPUTS</span></span>

### <span data-ttu-id="79fae-136">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79fae-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="79fae-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="79fae-137">NOTES</span></span>

## <span data-ttu-id="79fae-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79fae-138">RELATED LINKS</span></span>

[<span data-ttu-id="79fae-139">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fae-139">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="79fae-140">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fae-140">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="79fae-141">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fae-141">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="79fae-142">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79fae-142">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="79fae-143">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79fae-143">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


