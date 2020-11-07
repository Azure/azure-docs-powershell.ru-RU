---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 0ad478b1e60008619e579abf868f4d6aba25bbd9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905186"
---
# <span data-ttu-id="f2b2b-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2b2b-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="f2b2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b2b-103">Добавляет конечную точку к локальному объекту профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f2b2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2b2b-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2b2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b2b-106">Командлет **Add-AzTrafficManagerEndpointConfig** добавляет конечную точку в локальный объект профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f2b2b-107">Вы можете получить профиль, используя командлеты New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f2b2b-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f2b2b-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f2b2b-110">Чтобы создать конечную точку и внести изменения в одну операцию, используйте командлет New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f2b2b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2b2b-111">EXAMPLES</span></span>

### <span data-ttu-id="f2b2b-112">Пример 1: Добавление конечной точки к профилю</span><span class="sxs-lookup"><span data-stu-id="f2b2b-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f2b2b-113">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f2b2b-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f2b2b-114">Команда хранит локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f2b2b-115">Вторая команда добавляет конечную точку с именем Contoso в профиль, хранящийся в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f2b2b-116">Команда содержит данные конфигурации для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="f2b2b-117">Эта команда изменяет только локальный объект.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-117">This command changes only the local object.</span></span>

<span data-ttu-id="f2b2b-118">Последняя команда обновляет профиль диспетчера трафика в Azure таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f2b2b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2b2b-119">PARAMETERS</span></span>

### <span data-ttu-id="f2b2b-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="f2b2b-120">-CustomHeader</span></span>
<span data-ttu-id="f2b2b-121">Список имен настраиваемых заголовков и пар значений для пробных запросов.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="f2b2b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b2b-122">-DefaultProfile</span></span>
<span data-ttu-id="f2b2b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2b2b-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="f2b2b-124">-EndpointLocation</span></span>
<span data-ttu-id="f2b2b-125">Указывает расположение конечной точки для использования в методе маршрутизации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="f2b2b-126">Этот параметр применим только к конечным точкам типа ExternalEndpoints или NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="f2b2b-127">Этот параметр необходимо указывать при использовании метода маршрутизации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="f2b2b-128">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-128">Specify an Azure region name.</span></span>
<span data-ttu-id="f2b2b-129">Полный список областей Azure см. в разделе регионы Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="f2b2b-129">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f2b2b-130">-EndpointName</span></span>
<span data-ttu-id="f2b2b-131">Указывает имя конечной точки диспетчера трафика, которую добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f2b2b-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="f2b2b-132">-EndpointStatus</span></span>
<span data-ttu-id="f2b2b-133">Задает состояние конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="f2b2b-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f2b2b-134">Valid values are:</span></span> 

- <span data-ttu-id="f2b2b-135">Включаем</span><span class="sxs-lookup"><span data-stu-id="f2b2b-135">Enabled</span></span> 
- <span data-ttu-id="f2b2b-136">Отключает</span><span class="sxs-lookup"><span data-stu-id="f2b2b-136">Disabled</span></span> 

<span data-ttu-id="f2b2b-137">Если состояние включено, конечная точка проверяется на предмет работоспособности конечной точки и включена в метод маршрутизации трафика.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-138">-Геосоответствие</span><span class="sxs-lookup"><span data-stu-id="f2b2b-138">-GeoMapping</span></span>
<span data-ttu-id="f2b2b-139">Список регионов, сопоставленных с этой конечной точкой, при использовании метода маршрутизации для географического трафика.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="f2b2b-140">[Полный список приемлемых значений](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)можно найти в документации диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2b2b-141">-MinChildEndpoints</span></span>
<span data-ttu-id="f2b2b-142">Минимальное количество конечных точек, которые должны быть доступны в дочернем профиле для того, чтобы вложенная конечная точка в родительском профиле считалась доступной.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="f2b2b-143">Применимо только к конечной точке типа "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="f2b2b-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-144">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="f2b2b-144">-Priority</span></span>
<span data-ttu-id="f2b2b-145">Задает приоритет, назначаемый диспетчером трафика конечной точке.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f2b2b-146">Этот параметр используется только в том случае, если в профиле диспетчера трафика указан метод маршрутизации трафика приоритета.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="f2b2b-147">Допустимые значения — целые числа от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f2b2b-148">Более низкие значения представляют более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="f2b2b-149">Если указан приоритет, необходимо задать приоритеты для всех конечных точек в профиле, но ни одна из двух конечных точек не может иметь одинаковое значение приоритета.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="f2b2b-150">Если вы не укажете приоритеты, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с единицы (1), в порядке, в котором в профиле указаны конечные точки.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="f2b2b-151">-SubnetMapping</span></span>
<span data-ttu-id="f2b2b-152">Список диапазонов адресов или подсетей, сопоставленных с этой конечной точкой при использовании метода маршрутизации трафика "подсеть".</span><span class="sxs-lookup"><span data-stu-id="f2b2b-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-153">-Target</span><span class="sxs-lookup"><span data-stu-id="f2b2b-153">-Target</span></span>
<span data-ttu-id="f2b2b-154">Указывает полное DNS-имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="f2b2b-155">Диспетчер трафика возвращает это значение в ответах DNS, когда он направляет трафик на эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="f2b2b-156">Указывайте этот параметр только для типа конечной точки ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="f2b2b-157">Для других типов конечных точек укажите вместо него параметр *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="f2b2b-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b2b-158">-TargetResourceId</span></span>
<span data-ttu-id="f2b2b-159">Указывает идентификатор ресурса для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="f2b2b-160">Указывайте этот параметр только для типов конечных точек AzureEndpoints и NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="f2b2b-161">Для типа конечной точки ExternalEndpoints вместо него укажите *конечный* параметр.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2b2b-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="f2b2b-163">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f2b2b-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f2b2b-164">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f2b2b-165">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-166">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f2b2b-166">-Type</span></span>
<span data-ttu-id="f2b2b-167">Указывает тип конечной точки, которую этот командлет добавляет в профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f2b2b-168">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f2b2b-168">Valid values are:</span></span> 

- <span data-ttu-id="f2b2b-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2b2b-169">AzureEndpoints</span></span>
- <span data-ttu-id="f2b2b-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2b2b-170">ExternalEndpoints</span></span>
- <span data-ttu-id="f2b2b-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="f2b2b-171">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-172">-Weight</span><span class="sxs-lookup"><span data-stu-id="f2b2b-172">-Weight</span></span>
<span data-ttu-id="f2b2b-173">Определяет вес, который диспетчер трафика назначает конечной точке.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f2b2b-174">Допустимые значения — целые числа от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f2b2b-175">Значение по умолчанию — единица (1).</span><span class="sxs-lookup"><span data-stu-id="f2b2b-175">The default value is one (1).</span></span>
<span data-ttu-id="f2b2b-176">Этот параметр используется только в том случае, если профиль диспетчера трафика настроен с помощью метода маршрутизации для взвешенного трафика.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b2b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b2b-177">CommonParameters</span></span>
<span data-ttu-id="f2b2b-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2b2b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b2b-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b2b-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b2b-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2b2b-180">INPUTS</span></span>

### <span data-ttu-id="f2b2b-181">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2b2b-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2b2b-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2b2b-182">OUTPUTS</span></span>

### <span data-ttu-id="f2b2b-183">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2b2b-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f2b2b-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2b2b-184">NOTES</span></span>

## <span data-ttu-id="f2b2b-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2b2b-185">RELATED LINKS</span></span>

[<span data-ttu-id="f2b2b-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2b2b-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f2b2b-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f2b2b-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="f2b2b-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f2b2b-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f2b2b-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f2b2b-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


