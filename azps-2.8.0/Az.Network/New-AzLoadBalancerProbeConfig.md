---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6bcf0957d389f45bb0e010446381303c6124146b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903634"
---
# <span data-ttu-id="ec033-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec033-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ec033-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec033-102">SYNOPSIS</span></span>
<span data-ttu-id="ec033-103">Создает конфигурацию зонда для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ec033-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="ec033-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec033-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec033-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec033-105">DESCRIPTION</span></span>
<span data-ttu-id="ec033-106">Командлет **New-AzLoadBalancerProbeConfig** создает конфигурацию зонда для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="ec033-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ec033-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec033-107">EXAMPLES</span></span>

### <span data-ttu-id="ec033-108">Пример 1: создание конфигурации зонда</span><span class="sxs-lookup"><span data-stu-id="ec033-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="ec033-109">Эта команда создает конфигурацию зонда с именем MyProbe, используя HTTP-протокол.</span><span class="sxs-lookup"><span data-stu-id="ec033-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="ec033-110">Новый зонд будет подключаться к службе балансировки нагрузки на порте 80.</span><span class="sxs-lookup"><span data-stu-id="ec033-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="ec033-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec033-111">PARAMETERS</span></span>

### <span data-ttu-id="ec033-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec033-112">-DefaultProfile</span></span>
<span data-ttu-id="ec033-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec033-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec033-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ec033-114">-IntervalInSeconds</span></span>
<span data-ttu-id="ec033-115">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ec033-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="ec033-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec033-116">-Name</span></span>
<span data-ttu-id="ec033-117">Указывает имя конфигурации зонда, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="ec033-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="ec033-118">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="ec033-118">-Port</span></span>
<span data-ttu-id="ec033-119">Указывает порт, на котором новый зонд должен подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ec033-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="ec033-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="ec033-120">-ProbeCount</span></span>
<span data-ttu-id="ec033-121">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ec033-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="ec033-122">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ec033-122">-Protocol</span></span>
<span data-ttu-id="ec033-123">Указывает протокол, используемый для конфигурации пробы.</span><span class="sxs-lookup"><span data-stu-id="ec033-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="ec033-124">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="ec033-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="ec033-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="ec033-125">-RequestPath</span></span>
<span data-ttu-id="ec033-126">Указывает путь в службе балансировки нагрузки для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="ec033-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="ec033-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec033-127">-Confirm</span></span>
<span data-ttu-id="ec033-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ec033-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec033-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec033-129">-WhatIf</span></span>
<span data-ttu-id="ec033-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ec033-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec033-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ec033-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec033-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec033-132">CommonParameters</span></span>
<span data-ttu-id="ec033-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec033-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec033-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec033-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec033-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec033-135">INPUTS</span></span>

### <span data-ttu-id="ec033-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ec033-136">System.String</span></span>

### <span data-ttu-id="ec033-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ec033-137">System.Int32</span></span>

## <span data-ttu-id="ec033-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec033-138">OUTPUTS</span></span>

### <span data-ttu-id="ec033-139">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="ec033-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="ec033-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec033-140">NOTES</span></span>

## <span data-ttu-id="ec033-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec033-141">RELATED LINKS</span></span>

[<span data-ttu-id="ec033-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec033-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ec033-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec033-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ec033-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec033-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ec033-145">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec033-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


