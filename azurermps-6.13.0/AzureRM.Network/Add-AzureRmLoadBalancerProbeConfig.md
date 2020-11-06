---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567721"
---
# <span data-ttu-id="1955c-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1955c-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="1955c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1955c-102">SYNOPSIS</span></span>
<span data-ttu-id="1955c-103">Добавляет конфигурацию зонда в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1955c-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1955c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1955c-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1955c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1955c-105">DESCRIPTION</span></span>
<span data-ttu-id="1955c-106">Командлет **Add-AzureRmLoadBalancerProbeConfig** добавляет конфигурацию зонда в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="1955c-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="1955c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1955c-107">EXAMPLES</span></span>

### <span data-ttu-id="1955c-108">Пример 1. Добавление пробной конфигурации в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="1955c-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="1955c-109">Эта команда получает подсистему балансировки нагрузки с именем myLb, добавляет в нее указанную конфигурацию зонда, а затем использует командлет **Set-AzureRmLoadBalancer** для обновления подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1955c-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="1955c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1955c-110">PARAMETERS</span></span>

### <span data-ttu-id="1955c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1955c-111">-DefaultProfile</span></span>
<span data-ttu-id="1955c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1955c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1955c-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1955c-113">-IntervalInSeconds</span></span>
<span data-ttu-id="1955c-114">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1955c-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="1955c-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="1955c-115">-LoadBalancer</span></span>
<span data-ttu-id="1955c-116">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="1955c-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="1955c-117">Этот командлет добавляет конфигурацию зонда в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="1955c-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="1955c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1955c-118">-Name</span></span>
<span data-ttu-id="1955c-119">Указывает имя конфигурации зонда, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="1955c-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="1955c-120">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="1955c-120">-Port</span></span>
<span data-ttu-id="1955c-121">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1955c-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="1955c-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="1955c-122">-ProbeCount</span></span>
<span data-ttu-id="1955c-123">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1955c-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="1955c-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1955c-124">-Protocol</span></span>
<span data-ttu-id="1955c-125">Указывает протокол для пробного использования.</span><span class="sxs-lookup"><span data-stu-id="1955c-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="1955c-126">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="1955c-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="1955c-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="1955c-127">-RequestPath</span></span>
<span data-ttu-id="1955c-128">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="1955c-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="1955c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1955c-129">-Confirm</span></span>
<span data-ttu-id="1955c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1955c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1955c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1955c-131">-WhatIf</span></span>
<span data-ttu-id="1955c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1955c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1955c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1955c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1955c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1955c-134">CommonParameters</span></span>
<span data-ttu-id="1955c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1955c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1955c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1955c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1955c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1955c-137">INPUTS</span></span>

### <span data-ttu-id="1955c-138">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1955c-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="1955c-139">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1955c-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="1955c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1955c-140">OUTPUTS</span></span>

### <span data-ttu-id="1955c-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1955c-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1955c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1955c-142">NOTES</span></span>

## <span data-ttu-id="1955c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1955c-143">RELATED LINKS</span></span>

[<span data-ttu-id="1955c-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1955c-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="1955c-145">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1955c-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="1955c-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1955c-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="1955c-147">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1955c-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="1955c-148">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1955c-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


