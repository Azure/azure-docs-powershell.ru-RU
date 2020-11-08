---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075953"
---
# <span data-ttu-id="af002-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="af002-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="af002-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af002-102">SYNOPSIS</span></span>
<span data-ttu-id="af002-103">Изменяет все конечные точки в подсистеме балансировки нагрузки, установленной в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="af002-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="af002-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af002-104">SYNTAX</span></span>

### <span data-ttu-id="af002-105">DefaultProbe (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af002-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="af002-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="af002-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="af002-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="af002-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="af002-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af002-108">DESCRIPTION</span></span>
<span data-ttu-id="af002-109">Командлет **Set-AzureLoadBalancedEndpoint** изменяет все конечные точки в подсистеме балансировки нагрузки, установленной в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="af002-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="af002-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af002-110">EXAMPLES</span></span>

### <span data-ttu-id="af002-111">Пример 1: изменение конечных точек в наборе средств для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="af002-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="af002-112">Эта команда изменяет все конечные точки в разделе подсистемы балансировки нагрузки с именем LBSet01, чтобы использовать протокол TCP и частный порт 80.</span><span class="sxs-lookup"><span data-stu-id="af002-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="af002-113">Эта команда задает для средства балансировки нагрузки использование протокола TCP на порту 8080.</span><span class="sxs-lookup"><span data-stu-id="af002-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="af002-114">Пример 2: Указание другого виртуального IP-адреса</span><span class="sxs-lookup"><span data-stu-id="af002-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="af002-115">Эта команда изменяет подсистему балансировки нагрузки с именем Set подсистемы балансировки нагрузки, чтобы использовать виртуальный IP-адрес с именем Vip01.</span><span class="sxs-lookup"><span data-stu-id="af002-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="af002-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af002-116">PARAMETERS</span></span>

### <span data-ttu-id="af002-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="af002-117">-ACL</span></span>
<span data-ttu-id="af002-118">Определяет объект конфигурации списка управления доступом (ACL), применяемый этим командлетом к конечным точкам.</span><span class="sxs-lookup"><span data-stu-id="af002-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="af002-119">-DirectServerReturn</span></span>
<span data-ttu-id="af002-120">Указывает, будет ли этот командлет включать прямой возврат сервера.</span><span class="sxs-lookup"><span data-stu-id="af002-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="af002-121">Укажите $True, которые нужно включить, или $False, чтобы отключить.</span><span class="sxs-lookup"><span data-stu-id="af002-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="af002-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="af002-123">Указывает тайм-аут простоя TCP (в минутах) для конечных точек.</span><span class="sxs-lookup"><span data-stu-id="af002-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="af002-124">-InformationAction</span></span>
<span data-ttu-id="af002-125">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="af002-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="af002-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="af002-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af002-127">Продолжал</span><span class="sxs-lookup"><span data-stu-id="af002-127">Continue</span></span>
- <span data-ttu-id="af002-128">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="af002-128">Ignore</span></span>
- <span data-ttu-id="af002-129">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="af002-129">Inquire</span></span>
- <span data-ttu-id="af002-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="af002-130">SilentlyContinue</span></span>
- <span data-ttu-id="af002-131">Остановить</span><span class="sxs-lookup"><span data-stu-id="af002-131">Stop</span></span>
- <span data-ttu-id="af002-132">Рвать</span><span class="sxs-lookup"><span data-stu-id="af002-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="af002-133">-InformationVariable</span></span>
<span data-ttu-id="af002-134">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="af002-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="af002-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="af002-136">Указывает имя внутренней подсистемы балансировки нагрузки, которое этот командлет включает в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="af002-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="af002-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="af002-137">-LBSetName</span></span>
<span data-ttu-id="af002-138">Указывает имя набора средств балансировки нагрузки, которое обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af002-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="af002-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="af002-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="af002-140">Указывает алгоритм распространения подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="af002-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="af002-141">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="af002-141">Valid values are:</span></span> 

- <span data-ttu-id="af002-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="af002-142">sourceIP.</span></span>
<span data-ttu-id="af002-143">Две сходствы кортежей: исходный IP-адрес, конечный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="af002-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="af002-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="af002-144">sourceIPProtocol.</span></span>
<span data-ttu-id="af002-145">Три сходства кортежей: исходный IP-адрес, IP-адрес назначения, протокол</span><span class="sxs-lookup"><span data-stu-id="af002-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="af002-146">ничего.</span><span class="sxs-lookup"><span data-stu-id="af002-146">none.</span></span>
<span data-ttu-id="af002-147">Пять сходств кортежей: исходный IP-адрес, порт источника, IP-адрес назначения, порт назначения, протокол</span><span class="sxs-lookup"><span data-stu-id="af002-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="af002-148">Значение по умолчанию — None (нет).</span><span class="sxs-lookup"><span data-stu-id="af002-148">The default value is none.</span></span>

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

### <span data-ttu-id="af002-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="af002-149">-LocalPort</span></span>
<span data-ttu-id="af002-150">Указывает локальный, частный порт, который используются этими конечными точками.</span><span class="sxs-lookup"><span data-stu-id="af002-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="af002-151">Приложения на виртуальной машине прослушивают этот порт для запросов на ввод данных для данной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="af002-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="af002-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="af002-153">Задает интервал опроса зонда для конечных точек в секундах.</span><span class="sxs-lookup"><span data-stu-id="af002-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="af002-154">-ProbePath</span></span>
<span data-ttu-id="af002-155">Указывает относительный путь для пробной версии HTTP.</span><span class="sxs-lookup"><span data-stu-id="af002-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="af002-156">-ProbePort</span></span>
<span data-ttu-id="af002-157">Указывает порт, используемый для проверки подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="af002-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="af002-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="af002-159">Указывает, что конечные точки подсистемы балансировки нагрузки используют HTTP-зонд.</span><span class="sxs-lookup"><span data-stu-id="af002-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="af002-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="af002-161">Указывает, что конечные точки подсистемы балансировки нагрузки используют пробный протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="af002-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="af002-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="af002-163">Указывает время ожидания для опроса пробной проверки в секундах.</span><span class="sxs-lookup"><span data-stu-id="af002-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-164">-Profile</span><span class="sxs-lookup"><span data-stu-id="af002-164">-Profile</span></span>
<span data-ttu-id="af002-165">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af002-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af002-166">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af002-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-167">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="af002-167">-Protocol</span></span>
<span data-ttu-id="af002-168">Указывает протокол конечных точек.</span><span class="sxs-lookup"><span data-stu-id="af002-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="af002-169">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="af002-169">Valid values are:</span></span> 

- <span data-ttu-id="af002-170">Номера</span><span class="sxs-lookup"><span data-stu-id="af002-170">TCP</span></span> 
- <span data-ttu-id="af002-171">ТРАФИКА</span><span class="sxs-lookup"><span data-stu-id="af002-171">UDP</span></span>

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

### <span data-ttu-id="af002-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="af002-172">-PublicPort</span></span>
<span data-ttu-id="af002-173">Указывает открытый порт, который использует конечная точка.</span><span class="sxs-lookup"><span data-stu-id="af002-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="af002-174">Если значение не задано, Azure назначает доступный порт.</span><span class="sxs-lookup"><span data-stu-id="af002-174">If you do not specify a value, Azure assigns an available port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af002-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="af002-175">-ServiceName</span></span>
<span data-ttu-id="af002-176">Указывает имя службы Azure, содержащей конечные точки, которые изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af002-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af002-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="af002-177">-VirtualIPName</span></span>
<span data-ttu-id="af002-178">Указывает имя виртуального IP-адреса, который Azure связывает с конечными точками.</span><span class="sxs-lookup"><span data-stu-id="af002-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="af002-179">Чтобы добавить в службу виртуальные IP-адреса, используйте командлет **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="af002-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="af002-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af002-180">CommonParameters</span></span>
<span data-ttu-id="af002-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af002-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af002-182">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af002-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af002-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af002-183">INPUTS</span></span>

## <span data-ttu-id="af002-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af002-184">OUTPUTS</span></span>

## <span data-ttu-id="af002-185">Пуск</span><span class="sxs-lookup"><span data-stu-id="af002-185">NOTES</span></span>

## <span data-ttu-id="af002-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af002-186">RELATED LINKS</span></span>

[<span data-ttu-id="af002-187">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="af002-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="af002-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="af002-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


