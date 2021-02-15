---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232313"
---
# <span data-ttu-id="f0126-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="f0126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0126-102">SYNOPSIS</span></span>
<span data-ttu-id="f0126-103">Создает профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f0126-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="f0126-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0126-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0126-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0126-105">DESCRIPTION</span></span>
<span data-ttu-id="f0126-106">Для создания профиля Azure Traffic Manager будет создаваться новый **cmdlet AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="f0126-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f0126-107">Укажите *параметр Name* и необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="f0126-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="f0126-108">Этот cmdlet возвращает локальный объект, который представляет новый профиль.</span><span class="sxs-lookup"><span data-stu-id="f0126-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="f0126-109">Этот cmdlet не настраивает конечные точки Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f0126-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="f0126-110">Объект локального профиля можно обновить с помощью Add-AzTrafficManagerEndpointConfig управления.</span><span class="sxs-lookup"><span data-stu-id="f0126-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="f0126-111">Затем загрузите изменения в Диспетчер трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="f0126-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f0126-112">Кроме того, можно добавить конечные точки с помощью New-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="f0126-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f0126-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0126-113">EXAMPLES</span></span>

### <span data-ttu-id="f0126-114">Пример 1. Создание профиля</span><span class="sxs-lookup"><span data-stu-id="f0126-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="f0126-115">Эта команда создает профиль Диспетчера трафика Azure с именем ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f0126-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="f0126-116">FQDN DNS не contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="f0126-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="f0126-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0126-117">PARAMETERS</span></span>

### <span data-ttu-id="f0126-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="f0126-118">-CustomHeader</span></span>
<span data-ttu-id="f0126-119">Список пользовательских пар имен и значений для запросов к запросам на имя и значение.</span><span class="sxs-lookup"><span data-stu-id="f0126-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="f0126-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-120">-DefaultProfile</span></span>
<span data-ttu-id="f0126-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0126-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0126-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f0126-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="f0126-123">Список ожидаемых диапазонов кода состояния HTTP для запросов в отношении проверки в отношении проверки.</span><span class="sxs-lookup"><span data-stu-id="f0126-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="f0126-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="f0126-124">-MaxReturn</span></span>
<span data-ttu-id="f0126-125">Максимальное количество ответов, возвращенных для профилей с методом маршрутки MultiValue.</span><span class="sxs-lookup"><span data-stu-id="f0126-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="f0126-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f0126-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="f0126-127">Интервал (в секундах), через который диспетчер трафика будет проверять состояние каждой конечной точки в этом профиле.</span><span class="sxs-lookup"><span data-stu-id="f0126-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="f0126-128">Значение по умолчанию — 30.</span><span class="sxs-lookup"><span data-stu-id="f0126-128">The default is 30.</span></span>

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

### <span data-ttu-id="f0126-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="f0126-129">-MonitorPath</span></span>
<span data-ttu-id="f0126-130">Путь, используемый для отслеживания состояния конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f0126-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="f0126-131">Укажите значение относительно доменного имени конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f0126-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="f0126-132">Это значение должно начинаться с косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="f0126-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="f0126-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="f0126-133">-MonitorPort</span></span>
<span data-ttu-id="f0126-134">Указывает порт TCP, используемый для отслеживания состояния конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f0126-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="f0126-135">Допустимые значения — это integers from 1–65535.</span><span class="sxs-lookup"><span data-stu-id="f0126-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="f0126-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="f0126-136">-MonitorProtocol</span></span>
<span data-ttu-id="f0126-137">Протокол, который будет применяться для отслеживания состояния конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f0126-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="f0126-138">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f0126-138">Valid values are:</span></span>

- <span data-ttu-id="f0126-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="f0126-139">HTTP</span></span>
- <span data-ttu-id="f0126-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f0126-140">HTTPS</span></span>

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

### <span data-ttu-id="f0126-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="f0126-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="f0126-142">Время (в секундах) диспетчера трафика, которое позволяет конечным точкам в этом профиле реагировать на проверку.</span><span class="sxs-lookup"><span data-stu-id="f0126-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="f0126-143">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="f0126-143">The default is 10.</span></span>

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

### <span data-ttu-id="f0126-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="f0126-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="f0126-145">Количество последовательных сбойных проверок, которые диспетчер трафика проверял перед объявлением конечной точки в этом профиле "Ухудшения" после следующей повторной проверки.</span><span class="sxs-lookup"><span data-stu-id="f0126-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="f0126-146">Значение по умолчанию — 3.</span><span class="sxs-lookup"><span data-stu-id="f0126-146">The default is 3.</span></span>

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

### <span data-ttu-id="f0126-147">-Name</span><span class="sxs-lookup"><span data-stu-id="f0126-147">-Name</span></span>
<span data-ttu-id="f0126-148">Указывает имя профиля Диспетчера трафика, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0126-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f0126-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="f0126-149">-ProfileStatus</span></span>
<span data-ttu-id="f0126-150">Определяет состояние профиля.</span><span class="sxs-lookup"><span data-stu-id="f0126-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="f0126-151">Допустимые значения: Enabled (Включено) и Disabled (Отключено).</span><span class="sxs-lookup"><span data-stu-id="f0126-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="f0126-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="f0126-152">-RelativeDnsName</span></span>
<span data-ttu-id="f0126-153">Указывает относительное имя DNS, которое предоставляет этот профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f0126-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="f0126-154">Диспетчер трафика объединяет это значение и доменное имя DNS, которое Диспетчер трафика Azure использует для формирования полного доменного имени профиля.</span><span class="sxs-lookup"><span data-stu-id="f0126-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="f0126-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0126-155">-ResourceGroupName</span></span>
<span data-ttu-id="f0126-156">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0126-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f0126-157">Этот cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="f0126-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0126-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0126-158">-Tag</span></span>
<span data-ttu-id="f0126-159">Пары значений ключа в виде hash table set as tags (Теги на сервере).</span><span class="sxs-lookup"><span data-stu-id="f0126-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="f0126-160">Например:</span><span class="sxs-lookup"><span data-stu-id="f0126-160">For example:</span></span>

<span data-ttu-id="f0126-161">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f0126-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f0126-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="f0126-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="f0126-163">Определяет способ маршрутинга трафика.</span><span class="sxs-lookup"><span data-stu-id="f0126-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="f0126-164">Этот метод определяет, какая конечная точка диспетчера трафика возвращается в ответ на входящие запросы DNS.</span><span class="sxs-lookup"><span data-stu-id="f0126-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="f0126-165">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f0126-165">Valid values are:</span></span>

- <span data-ttu-id="f0126-166">Производительность</span><span class="sxs-lookup"><span data-stu-id="f0126-166">Performance</span></span>
- <span data-ttu-id="f0126-167">Взвеш</span><span class="sxs-lookup"><span data-stu-id="f0126-167">Weighted</span></span>
- <span data-ttu-id="f0126-168">Priority (Приоритет)</span><span class="sxs-lookup"><span data-stu-id="f0126-168">Priority</span></span>
- <span data-ttu-id="f0126-169">Географический</span><span class="sxs-lookup"><span data-stu-id="f0126-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0126-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="f0126-170">-Ttl</span></span>
<span data-ttu-id="f0126-171">Указывает значение DNS Time to Live (TTL) (Срок жизни).</span><span class="sxs-lookup"><span data-stu-id="f0126-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="f0126-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0126-172">CommonParameters</span></span>
<span data-ttu-id="f0126-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0126-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0126-174">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0126-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0126-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0126-175">INPUTS</span></span>

### <span data-ttu-id="f0126-176">Нет</span><span class="sxs-lookup"><span data-stu-id="f0126-176">None</span></span>

## <span data-ttu-id="f0126-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0126-177">OUTPUTS</span></span>

### <span data-ttu-id="f0126-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f0126-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0126-179">NOTES</span></span>

## <span data-ttu-id="f0126-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0126-180">RELATED LINKS</span></span>

[<span data-ttu-id="f0126-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f0126-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f0126-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f0126-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f0126-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f0126-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="f0126-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f0126-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


