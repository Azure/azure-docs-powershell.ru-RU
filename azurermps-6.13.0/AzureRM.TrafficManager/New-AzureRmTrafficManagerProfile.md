---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734096"
---
# <span data-ttu-id="81b34-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="81b34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81b34-102">SYNOPSIS</span></span>
<span data-ttu-id="81b34-103">Создание профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="81b34-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81b34-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81b34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81b34-105">DESCRIPTION</span></span>
<span data-ttu-id="81b34-106">Командлет **New-AzureRmTrafficManagerProfile** создает профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="81b34-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="81b34-107">Укажите параметр *Name (имя* ) и необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="81b34-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="81b34-108">Этот командлет возвращает локальный объект, который представляет новый профиль.</span><span class="sxs-lookup"><span data-stu-id="81b34-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="81b34-109">Этот командлет не настраивает конечные точки диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="81b34-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="81b34-110">Вы можете обновить объект локального профиля с помощью командлета Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="81b34-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="81b34-111">Затем добавьте изменения в диспетчер трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81b34-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="81b34-112">Кроме того, можно добавить конечные точки с помощью командлета New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="81b34-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="81b34-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81b34-113">EXAMPLES</span></span>

### <span data-ttu-id="81b34-114">Пример 1: Создание профиля</span><span class="sxs-lookup"><span data-stu-id="81b34-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="81b34-115">Эта команда создает профиль диспетчера трафика Azure с именем ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="81b34-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="81b34-116">Полное доменное имя DNS — contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="81b34-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="81b34-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81b34-117">PARAMETERS</span></span>

### <span data-ttu-id="81b34-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="81b34-118">-CustomHeader</span></span>
<span data-ttu-id="81b34-119">Список имен настраиваемых заголовков и пар значений для пробных запросов.</span><span class="sxs-lookup"><span data-stu-id="81b34-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-120">-DefaultProfile</span></span>
<span data-ttu-id="81b34-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81b34-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81b34-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="81b34-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="81b34-123">Список ожидаемых диапазонов кодов состояния HTTP для пробных запросов.</span><span class="sxs-lookup"><span data-stu-id="81b34-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="81b34-124">-MaxReturn</span></span>
<span data-ttu-id="81b34-125">Максимальное количество ответов, возвращенных для профилей, с несколькими методами маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="81b34-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="81b34-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="81b34-127">Интервал (в секундах), по прошествии которого диспетчер трафика проверяет работоспособность каждой конечной точки в этом профиле.</span><span class="sxs-lookup"><span data-stu-id="81b34-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="81b34-128">По умолчанию используется значение 30.</span><span class="sxs-lookup"><span data-stu-id="81b34-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="81b34-129">-MonitorPath</span></span>
<span data-ttu-id="81b34-130">Указывает путь, который используется для наблюдения за работоспособностью конечной точки.</span><span class="sxs-lookup"><span data-stu-id="81b34-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="81b34-131">Укажите значение, соответствующее доменному имени конечной точки.</span><span class="sxs-lookup"><span data-stu-id="81b34-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="81b34-132">Это значение должно начинаться с косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="81b34-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="81b34-133">-MonitorPort</span></span>
<span data-ttu-id="81b34-134">Указывает порт TCP, который используется для отслеживания работоспособности конечной точки.</span><span class="sxs-lookup"><span data-stu-id="81b34-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="81b34-135">Допустимые значения — целые числа от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="81b34-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="81b34-136">-MonitorProtocol</span></span>
<span data-ttu-id="81b34-137">Указывает протокол для наблюдения за работоспособностью конечной точки.</span><span class="sxs-lookup"><span data-stu-id="81b34-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="81b34-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="81b34-138">Valid values are:</span></span>

- <span data-ttu-id="81b34-139">ЧЕРЕЗ</span><span class="sxs-lookup"><span data-stu-id="81b34-139">HTTP</span></span>
- <span data-ttu-id="81b34-140">Протокол</span><span class="sxs-lookup"><span data-stu-id="81b34-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="81b34-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="81b34-142">Время (в секундах), в течение которого диспетчер трафика разрешает конечные точки в этом профиле отвечать на проверку работоспособности.</span><span class="sxs-lookup"><span data-stu-id="81b34-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="81b34-143">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="81b34-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="81b34-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="81b34-145">Количество последовательных проверок работоспособности, которые диспетчер трафика допускает, прежде чем объявлять конечную точку в этом профиле с ошибкой после следующей пропускной проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="81b34-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="81b34-146">Значение по умолчанию — 3.</span><span class="sxs-lookup"><span data-stu-id="81b34-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81b34-147">-Name</span></span>
<span data-ttu-id="81b34-148">Задает имя профиля диспетчера трафика, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="81b34-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="81b34-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="81b34-149">-ProfileStatus</span></span>
<span data-ttu-id="81b34-150">Указывает состояние профиля.</span><span class="sxs-lookup"><span data-stu-id="81b34-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="81b34-151">Допустимые значения: Enabled и Disabled.</span><span class="sxs-lookup"><span data-stu-id="81b34-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="81b34-152">-RelativeDnsName</span></span>
<span data-ttu-id="81b34-153">Указывает относительное DNS-имя, предоставленное этим профилем диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="81b34-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="81b34-154">Диспетчер трафика объединяет это значение и доменное имя DNS, используемое диспетчером трафика Azure, для формирования полного доменного имени (FQDN) профиля.</span><span class="sxs-lookup"><span data-stu-id="81b34-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="81b34-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b34-155">-ResourceGroupName</span></span>
<span data-ttu-id="81b34-156">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81b34-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="81b34-157">Этот командлет создает профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="81b34-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="81b34-158">-Тег</span><span class="sxs-lookup"><span data-stu-id="81b34-158">-Tag</span></span>
<span data-ttu-id="81b34-159">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="81b34-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="81b34-160">Например:</span><span class="sxs-lookup"><span data-stu-id="81b34-160">For example:</span></span>

<span data-ttu-id="81b34-161">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="81b34-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="81b34-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="81b34-163">Указывает метод маршрутизации трафика.</span><span class="sxs-lookup"><span data-stu-id="81b34-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="81b34-164">Этот метод определяет, какой диспетчер трафика конечной точки возвращает ответ на входящие DNS-запросы.</span><span class="sxs-lookup"><span data-stu-id="81b34-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="81b34-165">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="81b34-165">Valid values are:</span></span>

- <span data-ttu-id="81b34-166">Эффективности</span><span class="sxs-lookup"><span data-stu-id="81b34-166">Performance</span></span>
- <span data-ttu-id="81b34-167">Взвешенное</span><span class="sxs-lookup"><span data-stu-id="81b34-167">Weighted</span></span>
- <span data-ttu-id="81b34-168">Priority</span><span class="sxs-lookup"><span data-stu-id="81b34-168">Priority</span></span>
- <span data-ttu-id="81b34-169">Регионах</span><span class="sxs-lookup"><span data-stu-id="81b34-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="81b34-170">-Ttl</span></span>
<span data-ttu-id="81b34-171">Указывает значение срока жизни (TTL) DNS.</span><span class="sxs-lookup"><span data-stu-id="81b34-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b34-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b34-172">CommonParameters</span></span>
<span data-ttu-id="81b34-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81b34-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b34-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b34-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b34-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81b34-175">INPUTS</span></span>

### <span data-ttu-id="81b34-176">Ничего</span><span class="sxs-lookup"><span data-stu-id="81b34-176">None</span></span>
<span data-ttu-id="81b34-177">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="81b34-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81b34-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81b34-178">OUTPUTS</span></span>

### <span data-ttu-id="81b34-179">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-179">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="81b34-180">Этот командлет возвращает новый объект TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="81b34-180">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="81b34-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="81b34-181">NOTES</span></span>

## <span data-ttu-id="81b34-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81b34-182">RELATED LINKS</span></span>

[<span data-ttu-id="81b34-183">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="81b34-183">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="81b34-184">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-184">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="81b34-185">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-185">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="81b34-186">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-186">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="81b34-187">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-187">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="81b34-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="81b34-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


