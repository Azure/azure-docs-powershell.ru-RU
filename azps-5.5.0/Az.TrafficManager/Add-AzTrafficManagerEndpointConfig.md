---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241584"
---
# <span data-ttu-id="31e99-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="31e99-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="31e99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e99-102">SYNOPSIS</span></span>
<span data-ttu-id="31e99-103">Добавляет конечную точку в локальный объект профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="31e99-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="31e99-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31e99-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e99-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31e99-105">DESCRIPTION</span></span>
<span data-ttu-id="31e99-106">Cmdlet **Add-AzTrafficManagerEndpointConfig** добавляет конечную точку к локальному объекту профиля Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="31e99-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="31e99-107">Вы можете получить профиль с помощью New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="31e99-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="31e99-108">Этот cmdlet выполняется с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="31e99-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="31e99-109">Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="31e99-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="31e99-110">Чтобы создать конечную точку и зафиксировать изменение за одну операцию, используйте New-AzTrafficManagerEndpoint конечную точку.</span><span class="sxs-lookup"><span data-stu-id="31e99-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="31e99-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31e99-111">EXAMPLES</span></span>

### <span data-ttu-id="31e99-112">Пример 1. Добавление конечной точки в профиль</span><span class="sxs-lookup"><span data-stu-id="31e99-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="31e99-113">Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="31e99-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="31e99-114">Команда сохраняет локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="31e99-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="31e99-115">Вторая команда добавляет конечную точку contoso в профиль, $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="31e99-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="31e99-116">Команда содержит данные конфигурации для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="31e99-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="31e99-117">Эта команда изменяет только локальный объект.</span><span class="sxs-lookup"><span data-stu-id="31e99-117">This command changes only the local object.</span></span>

<span data-ttu-id="31e99-118">Конечная команда обновляет профиль Диспетчера трафика в Azure в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="31e99-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="31e99-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31e99-119">PARAMETERS</span></span>

### <span data-ttu-id="31e99-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="31e99-120">-CustomHeader</span></span>
<span data-ttu-id="31e99-121">Список пользовательских пар имен и значений для запросов к ветвям.</span><span class="sxs-lookup"><span data-stu-id="31e99-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="31e99-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e99-122">-DefaultProfile</span></span>
<span data-ttu-id="31e99-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31e99-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e99-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="31e99-124">-EndpointLocation</span></span>
<span data-ttu-id="31e99-125">Определяет расположение конечной точки, используемой методом маршрутации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="31e99-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="31e99-126">Этот параметр применяется только к конечным точкам типа ExternalEndpoints или NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="31e99-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="31e99-127">Этот параметр необходимо указать при перена указании метода маршрутизировать трафик производительности.</span><span class="sxs-lookup"><span data-stu-id="31e99-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="31e99-128">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="31e99-128">Specify an Azure region name.</span></span>
<span data-ttu-id="31e99-129">Полный список регионов Azure см. в azure Regions http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.</span><span class="sxs-lookup"><span data-stu-id="31e99-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="31e99-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="31e99-130">-EndpointName</span></span>
<span data-ttu-id="31e99-131">Указывает имя конечной точки Диспетчера трафика, которую добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e99-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="31e99-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="31e99-132">-EndpointStatus</span></span>
<span data-ttu-id="31e99-133">Определяет состояние конечной точки.</span><span class="sxs-lookup"><span data-stu-id="31e99-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="31e99-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="31e99-134">Valid values are:</span></span> 

- <span data-ttu-id="31e99-135">Включено</span><span class="sxs-lookup"><span data-stu-id="31e99-135">Enabled</span></span> 
- <span data-ttu-id="31e99-136">Отключено</span><span class="sxs-lookup"><span data-stu-id="31e99-136">Disabled</span></span> 

<span data-ttu-id="31e99-137">Если состояние включено, конечная точка переназначна на состояние "Состояние конечной точки" и включена в способ маршрутинга трафика.</span><span class="sxs-lookup"><span data-stu-id="31e99-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="31e99-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="31e99-138">-GeoMapping</span></span>
<span data-ttu-id="31e99-139">Список регионов, которые были назначены этой конечной точке при использовании метода маршрутинга для географических данных.</span><span class="sxs-lookup"><span data-stu-id="31e99-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="31e99-140">Полный список принятых значений можно получить в документации [Диспетчера трафика.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)</span><span class="sxs-lookup"><span data-stu-id="31e99-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="31e99-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="31e99-141">-MinChildEndpoints</span></span>
<span data-ttu-id="31e99-142">Минимальное количество конечных точек, которые должны быть доступны в профиле ребенка, чтобы вложенная конечная точка в родительском профиле считалась доступной.</span><span class="sxs-lookup"><span data-stu-id="31e99-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="31e99-143">Применимо только к конечной точке типа "Вложенныеendpoints".</span><span class="sxs-lookup"><span data-stu-id="31e99-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="31e99-144">-Priority</span><span class="sxs-lookup"><span data-stu-id="31e99-144">-Priority</span></span>
<span data-ttu-id="31e99-145">Определяет приоритет, который Диспетчер трафика назначает конечной точке.</span><span class="sxs-lookup"><span data-stu-id="31e99-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="31e99-146">Этот параметр используется только в том случае, если в профиле Диспетчера трафика настроен метод маршрутинга "Приоритетный трафик".</span><span class="sxs-lookup"><span data-stu-id="31e99-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="31e99-147">Допустимые значения — это значения от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="31e99-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="31e99-148">Нижние значения представляют более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="31e99-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="31e99-149">При указании приоритета необходимо указать приоритеты для всех конечных точек профиля, и две конечные точки не могут иметь одинаковое значение приоритета.</span><span class="sxs-lookup"><span data-stu-id="31e99-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="31e99-150">Если приоритеты не указаны, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с одной (1), в том порядке, в который перечислены конечные точки профиля.</span><span class="sxs-lookup"><span data-stu-id="31e99-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="31e99-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="31e99-151">-SubnetMapping</span></span>
<span data-ttu-id="31e99-152">Список диапазонов адресов или подсетей, которые были назначены данной конечной точке при использовании метода маршрутизации трафика "Подсеть".</span><span class="sxs-lookup"><span data-stu-id="31e99-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="31e99-153">-Target</span><span class="sxs-lookup"><span data-stu-id="31e99-153">-Target</span></span>
<span data-ttu-id="31e99-154">Указывает полное имя DNS конечной точки.</span><span class="sxs-lookup"><span data-stu-id="31e99-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="31e99-155">Диспетчер трафика возвращает это значение в ответах DNS, когда направляет трафик в эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="31e99-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="31e99-156">Укажите этот параметр только для типа конечной точки ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="31e99-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="31e99-157">Для других типов конечных точек укажите вместо этого параметр *TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="31e99-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="31e99-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="31e99-158">-TargetResourceId</span></span>
<span data-ttu-id="31e99-159">Определяет ИД ресурса конечного ресурса.</span><span class="sxs-lookup"><span data-stu-id="31e99-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="31e99-160">Укажите этот параметр только для типов конечных точек AzureEndpoint и NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="31e99-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="31e99-161">Для типа конечной точки ExternalEndpoint вместо этого укажите *целевой* параметр.</span><span class="sxs-lookup"><span data-stu-id="31e99-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="31e99-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31e99-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="31e99-163">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="31e99-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="31e99-164">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="31e99-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="31e99-165">Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile..</span><span class="sxs-lookup"><span data-stu-id="31e99-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="31e99-166">-Type</span><span class="sxs-lookup"><span data-stu-id="31e99-166">-Type</span></span>
<span data-ttu-id="31e99-167">Определяет тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="31e99-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="31e99-168">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="31e99-168">Valid values are:</span></span> 

- <span data-ttu-id="31e99-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="31e99-169">AzureEndpoints</span></span>
- <span data-ttu-id="31e99-170">Внешниеendpoints</span><span class="sxs-lookup"><span data-stu-id="31e99-170">ExternalEndpoints</span></span>
- <span data-ttu-id="31e99-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="31e99-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="31e99-172">-Weight</span><span class="sxs-lookup"><span data-stu-id="31e99-172">-Weight</span></span>
<span data-ttu-id="31e99-173">Определяет вес, который Диспетчер трафика назначает конечной точке.</span><span class="sxs-lookup"><span data-stu-id="31e99-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="31e99-174">Допустимые значения — это значения от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="31e99-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="31e99-175">Значение по умолчанию — 1(1).</span><span class="sxs-lookup"><span data-stu-id="31e99-175">The default value is one (1).</span></span>
<span data-ttu-id="31e99-176">Этот параметр используется только в том случае, если в профиле Диспетчера трафика настроен способ маршрутинга "Взвешемый трафик".</span><span class="sxs-lookup"><span data-stu-id="31e99-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="31e99-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e99-177">CommonParameters</span></span>
<span data-ttu-id="31e99-178">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e99-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e99-179">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e99-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e99-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31e99-180">INPUTS</span></span>

### <span data-ttu-id="31e99-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31e99-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="31e99-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31e99-182">OUTPUTS</span></span>

### <span data-ttu-id="31e99-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31e99-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="31e99-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31e99-184">NOTES</span></span>

## <span data-ttu-id="31e99-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31e99-185">RELATED LINKS</span></span>

[<span data-ttu-id="31e99-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31e99-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="31e99-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="31e99-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="31e99-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="31e99-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="31e99-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31e99-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


