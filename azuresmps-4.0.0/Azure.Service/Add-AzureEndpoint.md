---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075733"
---
# <span data-ttu-id="3ea1e-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ea1e-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="3ea1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ea1e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea1e-103">Добавляет конечную точку к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="3ea1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ea1e-104">SYNTAX</span></span>

### <span data-ttu-id="3ea1e-105">NoLB (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ea1e-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ea1e-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="3ea1e-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ea1e-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="3ea1e-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ea1e-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="3ea1e-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3ea1e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ea1e-109">DESCRIPTION</span></span>
<span data-ttu-id="3ea1e-110">Командлет **Add-AzureEndpoint** добавляет конечную точку в объект виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="3ea1e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ea1e-111">EXAMPLES</span></span>

### <span data-ttu-id="3ea1e-112">Пример 1: Добавление конечной точки</span><span class="sxs-lookup"><span data-stu-id="3ea1e-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="3ea1e-113">Эта команда извлекает конфигурацию виртуальной машины с именем VirtualMachine01 с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="3ea1e-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="3ea1e-114">Команда передается текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3ea1e-115">Этот командлет добавляет конечную точку с именем HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="3ea1e-116">Конечная точка имеет общедоступный порт 80 и локальный порт 8080.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="3ea1e-117">Команда передает объект виртуальной машины в командлет **Update-AzureVM** , который реализует ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="3ea1e-118">Пример 2: Добавление конечной точки, которая входит в группу балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="3ea1e-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="3ea1e-119">Эта команда извлекает конфигурацию виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="3ea1e-120">Текущий командлет добавляет конечную точку с именем HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="3ea1e-121">Конечная точка имеет общедоступный порт 80 и локальный порт 8080.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="3ea1e-122">Конечная точка принадлежит к общей группе балансировки нагрузки с именем "ферма".</span><span class="sxs-lookup"><span data-stu-id="3ea1e-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="3ea1e-123">Пробная версия HTTP для порта 80 с путем "/" отслеживает доступность конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="3ea1e-124">Эти изменения реализованы в команде.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-124">The command implements your changes.</span></span>

### <span data-ttu-id="3ea1e-125">Пример 3: связывание виртуального IP-адреса с конечной точкой</span><span class="sxs-lookup"><span data-stu-id="3ea1e-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="3ea1e-126">Эта команда извлекает конфигурацию виртуальной машины с именем VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="3ea1e-127">Текущий командлет добавляет конечную точку с именем HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="3ea1e-128">Конечная точка имеет общедоступный порт 80 и локальный порт 8080.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="3ea1e-129">Эта команда связывает виртуальный IP-адрес с конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="3ea1e-130">Эти изменения реализованы в команде.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-130">The command implements your changes.</span></span>

## <span data-ttu-id="3ea1e-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ea1e-131">PARAMETERS</span></span>

### <span data-ttu-id="3ea1e-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="3ea1e-132">-ACL</span></span>
<span data-ttu-id="3ea1e-133">Задает объект конфигурации списка управления доступом (ACL) для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="3ea1e-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="3ea1e-134">-DefaultProbe</span></span>
<span data-ttu-id="3ea1e-135">Указывает на то, что этот командлет использует параметр проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="3ea1e-136">-DirectServerReturn</span></span>
<span data-ttu-id="3ea1e-137">Указывает, будет ли этот командлет включать прямой возврат сервера.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="3ea1e-138">Укажите $True, которые нужно включить, или $False, чтобы отключить.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="3ea1e-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3ea1e-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3ea1e-140">Указывает тайм-аут простоя TCP для конечной точки (в минутах).</span><span class="sxs-lookup"><span data-stu-id="3ea1e-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="3ea1e-141">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3ea1e-141">-InformationAction</span></span>
<span data-ttu-id="3ea1e-142">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3ea1e-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3ea1e-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ea1e-144">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3ea1e-144">Continue</span></span>
- <span data-ttu-id="3ea1e-145">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3ea1e-145">Ignore</span></span>
- <span data-ttu-id="3ea1e-146">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3ea1e-146">Inquire</span></span>
- <span data-ttu-id="3ea1e-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3ea1e-147">SilentlyContinue</span></span>
- <span data-ttu-id="3ea1e-148">Остановить</span><span class="sxs-lookup"><span data-stu-id="3ea1e-148">Stop</span></span>
- <span data-ttu-id="3ea1e-149">Рвать</span><span class="sxs-lookup"><span data-stu-id="3ea1e-149">Suspend</span></span>

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

### <span data-ttu-id="3ea1e-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3ea1e-150">-InformationVariable</span></span>
<span data-ttu-id="3ea1e-151">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3ea1e-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3ea1e-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="3ea1e-153">Указывает имя внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="3ea1e-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="3ea1e-154">-LBSetName</span></span>
<span data-ttu-id="3ea1e-155">Указывает имя для подсистемы балансировки нагрузки, установленное для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="3ea1e-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="3ea1e-157">Указывает алгоритм распространения подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="3ea1e-158">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3ea1e-158">Valid values are:</span></span> 

- <span data-ttu-id="3ea1e-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-159">sourceIP.</span></span>
<span data-ttu-id="3ea1e-160">Две сходствы кортежей: исходный IP-адрес, конечный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="3ea1e-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="3ea1e-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-161">sourceIPProtocol.</span></span>
<span data-ttu-id="3ea1e-162">Три сходства кортежей: исходный IP-адрес, IP-адрес назначения, протокол</span><span class="sxs-lookup"><span data-stu-id="3ea1e-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="3ea1e-163">ничего.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-163">none.</span></span>
<span data-ttu-id="3ea1e-164">Пять сходств кортежей: исходный IP-адрес, порт источника, IP-адрес назначения, порт назначения, протокол</span><span class="sxs-lookup"><span data-stu-id="3ea1e-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="3ea1e-165">Значение по умолчанию — None (нет).</span><span class="sxs-lookup"><span data-stu-id="3ea1e-165">The default value is none.</span></span>

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

### <span data-ttu-id="3ea1e-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="3ea1e-166">-LocalPort</span></span>
<span data-ttu-id="3ea1e-167">Указывает локальный, частный порт, который использует эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="3ea1e-168">Приложения на виртуальной машине прослушивают этот порт для запросов на входные данные для этой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-169">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ea1e-169">-Name</span></span>
<span data-ttu-id="3ea1e-170">Задает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-171">-"Непроверяемый"</span><span class="sxs-lookup"><span data-stu-id="3ea1e-171">-NoProbe</span></span>
<span data-ttu-id="3ea1e-172">Указывает на то, что этот командлет использует параметр "без проверки".</span><span class="sxs-lookup"><span data-stu-id="3ea1e-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3ea1e-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="3ea1e-174">Задает интервал опроса для проверки конечной точки (в секундах).</span><span class="sxs-lookup"><span data-stu-id="3ea1e-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="3ea1e-175">-ProbePath</span></span>
<span data-ttu-id="3ea1e-176">Указывает относительный путь к зонду HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="3ea1e-177">-ProbePort</span></span>
<span data-ttu-id="3ea1e-178">Указывает порт, который использует конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="3ea1e-179">-ProbeProtocol</span></span>
<span data-ttu-id="3ea1e-180">Указывает протокол порта.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-180">Specifies the port protocol.</span></span>
<span data-ttu-id="3ea1e-181">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3ea1e-181">Valid values are:</span></span> 

- <span data-ttu-id="3ea1e-182">Номера</span><span class="sxs-lookup"><span data-stu-id="3ea1e-182">tcp</span></span> 
- <span data-ttu-id="3ea1e-183">через</span><span class="sxs-lookup"><span data-stu-id="3ea1e-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="3ea1e-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="3ea1e-185">Указывает время ожидания для опроса пробного периода в секундах.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-186">-Profile</span><span class="sxs-lookup"><span data-stu-id="3ea1e-186">-Profile</span></span>
<span data-ttu-id="3ea1e-187">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ea1e-188">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ea1e-189">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="3ea1e-189">-Protocol</span></span>
<span data-ttu-id="3ea1e-190">Указывает протокол конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="3ea1e-191">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3ea1e-191">Valid values are:</span></span> 

- <span data-ttu-id="3ea1e-192">Номера</span><span class="sxs-lookup"><span data-stu-id="3ea1e-192">tcp</span></span> 
- <span data-ttu-id="3ea1e-193">трафика</span><span class="sxs-lookup"><span data-stu-id="3ea1e-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="3ea1e-194">-PublicPort</span></span>
<span data-ttu-id="3ea1e-195">Указывает открытый порт, который использует конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="3ea1e-196">Если значение не задано, Azure назначает доступный порт.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="3ea1e-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="3ea1e-197">-VirtualIPName</span></span>
<span data-ttu-id="3ea1e-198">Указывает имя виртуального IP-адреса, который Azure связывает с конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="3ea1e-199">Ваша служба может иметь несколько виртуальных IP – адресов.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="3ea1e-200">Чтобы создать виртуальные IP-адреса, используйте командлет **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="3ea1e-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="3ea1e-201">-VM</span><span class="sxs-lookup"><span data-stu-id="3ea1e-201">-VM</span></span>
<span data-ttu-id="3ea1e-202">Указывает виртуальную машину, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1e-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea1e-203">CommonParameters</span></span>
<span data-ttu-id="3ea1e-204">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ea1e-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea1e-205">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea1e-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea1e-206">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ea1e-206">INPUTS</span></span>

## <span data-ttu-id="3ea1e-207">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ea1e-207">OUTPUTS</span></span>

### <span data-ttu-id="3ea1e-208">System. Object</span><span class="sxs-lookup"><span data-stu-id="3ea1e-208">System.Object</span></span>

## <span data-ttu-id="3ea1e-209">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ea1e-209">NOTES</span></span>

## <span data-ttu-id="3ea1e-210">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ea1e-210">RELATED LINKS</span></span>

[<span data-ttu-id="3ea1e-211">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="3ea1e-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="3ea1e-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ea1e-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="3ea1e-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3ea1e-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="3ea1e-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ea1e-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="3ea1e-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ea1e-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="3ea1e-216">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3ea1e-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


