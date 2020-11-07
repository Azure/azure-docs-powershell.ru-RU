---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: a6fe4515fe6e6df213abb667eb83bccfa9ac6095
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915254"
---
# <span data-ttu-id="75a5a-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75a5a-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="75a5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="75a5a-103">Добавляет конфигурацию зонда в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="75a5a-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75a5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75a5a-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="75a5a-106">Командлет **Add-AzureRmLoadBalancerProbeConfig** добавляет конфигурацию зонда в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="75a5a-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="75a5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="75a5a-108">Пример 1. Добавление пробной конфигурации в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="75a5a-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="75a5a-109">Эта команда получает подсистему балансировки нагрузки с именем myLb, добавляет в нее указанную конфигурацию зонда, а затем использует командлет **Set-AzureRmLoadBalancer** для обновления подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="75a5a-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="75a5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75a5a-110">PARAMETERS</span></span>

### <span data-ttu-id="75a5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a5a-111">-DefaultProfile</span></span>
<span data-ttu-id="75a5a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75a5a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75a5a-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="75a5a-113">-IntervalInSeconds</span></span>
<span data-ttu-id="75a5a-114">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="75a5a-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="75a5a-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="75a5a-115">-LoadBalancer</span></span>
<span data-ttu-id="75a5a-116">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="75a5a-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="75a5a-117">Этот командлет добавляет конфигурацию зонда в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="75a5a-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="75a5a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75a5a-118">-Name</span></span>
<span data-ttu-id="75a5a-119">Указывает имя конфигурации зонда, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="75a5a-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="75a5a-120">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="75a5a-120">-Port</span></span>
<span data-ttu-id="75a5a-121">Указывает порт, на котором зонды должны подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="75a5a-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="75a5a-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="75a5a-122">-ProbeCount</span></span>
<span data-ttu-id="75a5a-123">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="75a5a-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="75a5a-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="75a5a-124">-Protocol</span></span>
<span data-ttu-id="75a5a-125">Указывает протокол для пробного использования.</span><span class="sxs-lookup"><span data-stu-id="75a5a-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="75a5a-126">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="75a5a-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="75a5a-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="75a5a-127">-RequestPath</span></span>
<span data-ttu-id="75a5a-128">Указывает путь в службе балансировки нагрузки, проверяемый для определения работоспособности.</span><span class="sxs-lookup"><span data-stu-id="75a5a-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="75a5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a5a-129">CommonParameters</span></span>
<span data-ttu-id="75a5a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75a5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a5a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a5a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a5a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75a5a-132">INPUTS</span></span>

### <span data-ttu-id="75a5a-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75a5a-133">PSLoadBalancer</span></span>
<span data-ttu-id="75a5a-134">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="75a5a-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="75a5a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75a5a-135">OUTPUTS</span></span>

### <span data-ttu-id="75a5a-136">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75a5a-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="75a5a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="75a5a-137">NOTES</span></span>

## <span data-ttu-id="75a5a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75a5a-138">RELATED LINKS</span></span>

[<span data-ttu-id="75a5a-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75a5a-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="75a5a-140">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75a5a-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="75a5a-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75a5a-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="75a5a-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="75a5a-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="75a5a-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75a5a-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


