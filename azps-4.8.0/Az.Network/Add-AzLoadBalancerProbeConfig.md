---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236074"
---
# <span data-ttu-id="5d8ed-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5d8ed-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5d8ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8ed-103">Добавляет конфигурацию зонда в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="5d8ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d8ed-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d8ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="5d8ed-106">Командлет **Add-AzLoadBalancerProbeConfig** добавляет конфигурацию зонда в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="5d8ed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="5d8ed-108">Пример 1: Добавление пробной конфигурации в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="5d8ed-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="5d8ed-109">Эта команда получает подсистему балансировки нагрузки с именем myLb, добавляет в нее указанную конфигурацию зонда, а затем использует командлет **Set-AzLoadBalancer** для обновления подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="5d8ed-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d8ed-110">PARAMETERS</span></span>

### <span data-ttu-id="5d8ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8ed-111">-DefaultProfile</span></span>
<span data-ttu-id="5d8ed-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d8ed-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5d8ed-113">-IntervalInSeconds</span></span>
<span data-ttu-id="5d8ed-114">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="5d8ed-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="5d8ed-115">-LoadBalancer</span></span>
<span data-ttu-id="5d8ed-116">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="5d8ed-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="5d8ed-117">Этот командлет добавляет конфигурацию зонда в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="5d8ed-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d8ed-118">-Name</span></span>
<span data-ttu-id="5d8ed-119">Указывает имя конфигурации зонда, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="5d8ed-120">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="5d8ed-120">-Port</span></span>
<span data-ttu-id="5d8ed-121">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="5d8ed-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="5d8ed-122">-ProbeCount</span></span>
<span data-ttu-id="5d8ed-123">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="5d8ed-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="5d8ed-124">-Protocol</span></span>
<span data-ttu-id="5d8ed-125">Указывает протокол для пробного использования.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="5d8ed-126">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="5d8ed-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="5d8ed-127">-RequestPath</span></span>
<span data-ttu-id="5d8ed-128">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="5d8ed-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d8ed-129">-Confirm</span></span>
<span data-ttu-id="5d8ed-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d8ed-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d8ed-131">-WhatIf</span></span>
<span data-ttu-id="5d8ed-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d8ed-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d8ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8ed-134">CommonParameters</span></span>
<span data-ttu-id="5d8ed-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d8ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8ed-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d8ed-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8ed-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d8ed-137">INPUTS</span></span>

### <span data-ttu-id="5d8ed-138">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5d8ed-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5d8ed-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5d8ed-139">System.String</span></span>

### <span data-ttu-id="5d8ed-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5d8ed-140">System.Int32</span></span>

## <span data-ttu-id="5d8ed-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d8ed-141">OUTPUTS</span></span>

### <span data-ttu-id="5d8ed-142">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5d8ed-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5d8ed-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d8ed-143">NOTES</span></span>

## <span data-ttu-id="5d8ed-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d8ed-144">RELATED LINKS</span></span>

[<span data-ttu-id="5d8ed-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5d8ed-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5d8ed-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5d8ed-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5d8ed-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5d8ed-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5d8ed-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5d8ed-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="5d8ed-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5d8ed-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


