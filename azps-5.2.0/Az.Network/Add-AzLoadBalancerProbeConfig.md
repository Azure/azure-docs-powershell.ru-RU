---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 4da0085e3ee0b7e023d93f5b1d54bf500512e5d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413975"
---
# <span data-ttu-id="5f468-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f468-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5f468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f468-102">SYNOPSIS</span></span>
<span data-ttu-id="5f468-103">Добавляет конфигурацию формы в баланс для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5f468-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="5f468-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f468-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f468-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f468-105">DESCRIPTION</span></span>
<span data-ttu-id="5f468-106">Для балансиента нагрузки Azure к балансе нагрузки Добавляется конфигурация **Add-AzLoadBalancerProbeConfig.**</span><span class="sxs-lookup"><span data-stu-id="5f468-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="5f468-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f468-107">EXAMPLES</span></span>

### <span data-ttu-id="5f468-108">Пример 1. Добавление конфигурации в балансировую нагрузку</span><span class="sxs-lookup"><span data-stu-id="5f468-108">Example 1: Add a probe configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="5f468-109">Эта команда получает балансировку нагрузки с именем myLb, добавляет к ней указанную конфигурацию этой формы, а затем использует командлет **Set-AzLoadBalancer** для обновления балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5f468-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="5f468-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f468-110">PARAMETERS</span></span>

### <span data-ttu-id="5f468-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f468-111">-DefaultProfile</span></span>
<span data-ttu-id="5f468-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f468-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f468-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5f468-113">-IntervalInSeconds</span></span>
<span data-ttu-id="5f468-114">Интервал (в секундах) между экземплярами службы с балансиза нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="5f468-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="5f468-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f468-115">-LoadBalancer</span></span>
<span data-ttu-id="5f468-116">Определяет объект **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="5f468-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="5f468-117">Этот cmdlet добавляет конфигурацию формы к балансе нагрузки, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5f468-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f468-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5f468-118">-Name</span></span>
<span data-ttu-id="5f468-119">Указывает имя добавляемой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5f468-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="5f468-120">-Port</span><span class="sxs-lookup"><span data-stu-id="5f468-120">-Port</span></span>
<span data-ttu-id="5f468-121">Указывает порт, на котором следует подключиться к службе с балансиза нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="5f468-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="5f468-122">-HorizonCount</span><span class="sxs-lookup"><span data-stu-id="5f468-122">-ProbeCount</span></span>
<span data-ttu-id="5f468-123">Количество последовательных неудач экземпляров, которые считаются неработоспособными.</span><span class="sxs-lookup"><span data-stu-id="5f468-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="5f468-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5f468-124">-Protocol</span></span>
<span data-ttu-id="5f468-125">Протокол, который будет применяться к проекту.</span><span class="sxs-lookup"><span data-stu-id="5f468-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="5f468-126">Допустимыми значениями для этого параметра являются Tcp или Http.</span><span class="sxs-lookup"><span data-stu-id="5f468-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="5f468-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="5f468-127">-RequestPath</span></span>
<span data-ttu-id="5f468-128">Путь к службе с балансиза нагрузкой, который будет задан для определения его состояния.</span><span class="sxs-lookup"><span data-stu-id="5f468-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="5f468-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f468-129">-Confirm</span></span>
<span data-ttu-id="5f468-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5f468-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f468-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f468-131">-WhatIf</span></span>
<span data-ttu-id="5f468-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f468-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f468-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5f468-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f468-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f468-134">CommonParameters</span></span>
<span data-ttu-id="5f468-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f468-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f468-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f468-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f468-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f468-137">INPUTS</span></span>

### <span data-ttu-id="5f468-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f468-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5f468-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5f468-139">System.String</span></span>

### <span data-ttu-id="5f468-140">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5f468-140">System.Int32</span></span>

## <span data-ttu-id="5f468-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f468-141">OUTPUTS</span></span>

### <span data-ttu-id="5f468-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f468-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5f468-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f468-143">NOTES</span></span>

## <span data-ttu-id="5f468-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f468-144">RELATED LINKS</span></span>

[<span data-ttu-id="5f468-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f468-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5f468-146">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f468-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5f468-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f468-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5f468-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f468-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="5f468-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5f468-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


