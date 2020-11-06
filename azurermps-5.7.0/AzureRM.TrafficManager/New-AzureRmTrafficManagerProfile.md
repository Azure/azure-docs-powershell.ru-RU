---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563236"
---
# <span data-ttu-id="97a2f-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="97a2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="97a2f-103">Создание профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="97a2f-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97a2f-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="97a2f-106">Командлет **New-AzureRmTrafficManagerProfile** создает профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="97a2f-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="97a2f-107">Укажите параметр *Name (имя* ) и необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="97a2f-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="97a2f-108">Этот командлет возвращает локальный объект, который представляет новый профиль.</span><span class="sxs-lookup"><span data-stu-id="97a2f-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="97a2f-109">Этот командлет не настраивает конечные точки диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="97a2f-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="97a2f-110">Вы можете обновить объект локального профиля с помощью командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="97a2f-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="97a2f-111">Затем добавьте изменения в диспетчер трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="97a2f-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="97a2f-112">Кроме того, можно добавить конечные точки с помощью командлета New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="97a2f-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="97a2f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97a2f-113">EXAMPLES</span></span>

### <span data-ttu-id="97a2f-114">Пример 1: Создание профиля</span><span class="sxs-lookup"><span data-stu-id="97a2f-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="97a2f-115">Эта команда создает профиль диспетчера трафика Azure с именем ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="97a2f-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="97a2f-116">Полное доменное имя DNS — contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="97a2f-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="97a2f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97a2f-117">PARAMETERS</span></span>

### <span data-ttu-id="97a2f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-118">-DefaultProfile</span></span>
<span data-ttu-id="97a2f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97a2f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97a2f-120">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="97a2f-120">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="97a2f-121">Интервал (в секундах), по прошествии которого диспетчер трафика проверяет работоспособность каждой конечной точки в этом профиле.</span><span class="sxs-lookup"><span data-stu-id="97a2f-121">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="97a2f-122">По умолчанию используется значение 30.</span><span class="sxs-lookup"><span data-stu-id="97a2f-122">The default is 30.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-123">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="97a2f-123">-MonitorPath</span></span>
<span data-ttu-id="97a2f-124">Указывает путь, который используется для наблюдения за работоспособностью конечной точки.</span><span class="sxs-lookup"><span data-stu-id="97a2f-124">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="97a2f-125">Укажите значение, соответствующее доменному имени конечной точки.</span><span class="sxs-lookup"><span data-stu-id="97a2f-125">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="97a2f-126">Это значение должно начинаться с косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="97a2f-126">This value must begin with a slash (/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="97a2f-127">-MonitorPort</span></span>
<span data-ttu-id="97a2f-128">Указывает порт TCP, который используется для отслеживания работоспособности конечной точки.</span><span class="sxs-lookup"><span data-stu-id="97a2f-128">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="97a2f-129">Допустимые значения — целые числа от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="97a2f-129">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="97a2f-130">-MonitorProtocol</span></span>
<span data-ttu-id="97a2f-131">Указывает протокол для наблюдения за работоспособностью конечной точки.</span><span class="sxs-lookup"><span data-stu-id="97a2f-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="97a2f-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="97a2f-132">Valid values are:</span></span>

- <span data-ttu-id="97a2f-133">ЧЕРЕЗ</span><span class="sxs-lookup"><span data-stu-id="97a2f-133">HTTP</span></span>
- <span data-ttu-id="97a2f-134">Протокол</span><span class="sxs-lookup"><span data-stu-id="97a2f-134">HTTPS</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-135">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="97a2f-135">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="97a2f-136">Время (в секундах), в течение которого диспетчер трафика разрешает конечные точки в этом профиле отвечать на проверку работоспособности.</span><span class="sxs-lookup"><span data-stu-id="97a2f-136">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="97a2f-137">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="97a2f-137">The default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-138">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="97a2f-138">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="97a2f-139">Количество последовательных проверок работоспособности, которые диспетчер трафика допускает, прежде чем объявлять конечную точку в этом профиле с ошибкой после следующей пропускной проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="97a2f-139">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="97a2f-140">Значение по умолчанию — 3.</span><span class="sxs-lookup"><span data-stu-id="97a2f-140">The default is 3.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97a2f-141">-Name</span></span>
<span data-ttu-id="97a2f-142">Задает имя профиля диспетчера трафика, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="97a2f-142">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="97a2f-143">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="97a2f-143">-ProfileStatus</span></span>
<span data-ttu-id="97a2f-144">Указывает состояние профиля.</span><span class="sxs-lookup"><span data-stu-id="97a2f-144">Specifies the status of the profile.</span></span>
<span data-ttu-id="97a2f-145">Допустимые значения: Enabled и Disabled.</span><span class="sxs-lookup"><span data-stu-id="97a2f-145">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-146">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="97a2f-146">-RelativeDnsName</span></span>
<span data-ttu-id="97a2f-147">Указывает относительное DNS-имя, предоставленное этим профилем диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="97a2f-147">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="97a2f-148">Диспетчер трафика объединяет это значение и доменное имя DNS, используемое диспетчером трафика Azure, для формирования полного доменного имени (FQDN) профиля.</span><span class="sxs-lookup"><span data-stu-id="97a2f-148">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="97a2f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a2f-149">-ResourceGroupName</span></span>
<span data-ttu-id="97a2f-150">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97a2f-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="97a2f-151">Этот командлет создает профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="97a2f-151">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="97a2f-152">-Тег</span><span class="sxs-lookup"><span data-stu-id="97a2f-152">-Tag</span></span>
<span data-ttu-id="97a2f-153">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="97a2f-153">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="97a2f-154">Например:</span><span class="sxs-lookup"><span data-stu-id="97a2f-154">For example:</span></span>

<span data-ttu-id="97a2f-155">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="97a2f-155">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-156">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="97a2f-156">-TrafficRoutingMethod</span></span>
<span data-ttu-id="97a2f-157">Указывает метод маршрутизации трафика.</span><span class="sxs-lookup"><span data-stu-id="97a2f-157">Specifies the traffic routing method.</span></span>
<span data-ttu-id="97a2f-158">Этот метод определяет, какой диспетчер трафика конечной точки возвращает ответ на входящие DNS-запросы.</span><span class="sxs-lookup"><span data-stu-id="97a2f-158">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="97a2f-159">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="97a2f-159">Valid values are:</span></span>

- <span data-ttu-id="97a2f-160">Эффективности</span><span class="sxs-lookup"><span data-stu-id="97a2f-160">Performance</span></span>
- <span data-ttu-id="97a2f-161">Взвешенное</span><span class="sxs-lookup"><span data-stu-id="97a2f-161">Weighted</span></span>
- <span data-ttu-id="97a2f-162">Priority</span><span class="sxs-lookup"><span data-stu-id="97a2f-162">Priority</span></span>
- <span data-ttu-id="97a2f-163">Регионах</span><span class="sxs-lookup"><span data-stu-id="97a2f-163">Geographic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-164">-TTL</span><span class="sxs-lookup"><span data-stu-id="97a2f-164">-Ttl</span></span>
<span data-ttu-id="97a2f-165">Указывает значение срока жизни (TTL) DNS.</span><span class="sxs-lookup"><span data-stu-id="97a2f-165">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a2f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a2f-166">CommonParameters</span></span>
<span data-ttu-id="97a2f-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97a2f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a2f-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a2f-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a2f-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97a2f-169">INPUTS</span></span>

### <span data-ttu-id="97a2f-170">Ничего</span><span class="sxs-lookup"><span data-stu-id="97a2f-170">None</span></span>
<span data-ttu-id="97a2f-171">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="97a2f-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97a2f-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97a2f-172">OUTPUTS</span></span>

### <span data-ttu-id="97a2f-173">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-173">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="97a2f-174">Этот командлет возвращает новый объект TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="97a2f-174">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="97a2f-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="97a2f-175">NOTES</span></span>

## <span data-ttu-id="97a2f-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97a2f-176">RELATED LINKS</span></span>

[<span data-ttu-id="97a2f-177">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="97a2f-177">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="97a2f-178">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-178">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="97a2f-179">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-179">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="97a2f-180">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-180">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="97a2f-181">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-181">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="97a2f-182">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97a2f-182">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


