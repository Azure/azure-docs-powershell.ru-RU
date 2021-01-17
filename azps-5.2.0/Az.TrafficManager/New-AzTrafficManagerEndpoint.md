---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391439"
---
# <span data-ttu-id="afa93-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afa93-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="afa93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afa93-102">SYNOPSIS</span></span>
<span data-ttu-id="afa93-103">Создает конечную точку в профиле Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="afa93-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="afa93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afa93-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afa93-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afa93-105">DESCRIPTION</span></span>
<span data-ttu-id="afa93-106">Cmdlet **New-AzTrafficManagerEndpoint** создает конечную точку в профиле Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="afa93-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="afa93-107">Этот cmdlet зафиксировать каждую новую конечную точку службе Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="afa93-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="afa93-108">Чтобы добавить несколько конечных точек к локальному объекту профиля Диспетчера трафика и зафиксировать изменения за одну операцию, используйте Add-AzTrafficManagerEndpointConfig управления.</span><span class="sxs-lookup"><span data-stu-id="afa93-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="afa93-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afa93-109">EXAMPLES</span></span>

### <span data-ttu-id="afa93-110">Пример 1. Создание внешней конечной точки для профиля</span><span class="sxs-lookup"><span data-stu-id="afa93-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="afa93-111">Эта команда создает внешнюю конечную точку с именем contoso в профиле ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="afa93-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="afa93-112">Пример 2. Создание конечной точки Azure для профиля</span><span class="sxs-lookup"><span data-stu-id="afa93-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="afa93-113">Эта команда создает конечную точку Azure с именем contoso в профиле ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="afa93-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="afa93-114">Конечная точка Azure указывает на azure Web App, и ее ИД диспетчера ресурсов Azure задается путем URI в *TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="afa93-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="afa93-115">Эта команда не указывает параметр *EndpointLocation,* так как ресурс Web App обеспечивает расположение.</span><span class="sxs-lookup"><span data-stu-id="afa93-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="afa93-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afa93-116">PARAMETERS</span></span>

### <span data-ttu-id="afa93-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="afa93-117">-CustomHeader</span></span>
<span data-ttu-id="afa93-118">Список пользовательских пар имен и значений для запросов к запросам на имя и значение.</span><span class="sxs-lookup"><span data-stu-id="afa93-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="afa93-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa93-119">-DefaultProfile</span></span>
<span data-ttu-id="afa93-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afa93-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afa93-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="afa93-121">-EndpointLocation</span></span>
<span data-ttu-id="afa93-122">Определяет расположение конечной точки, используемой методом маршрутации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="afa93-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="afa93-123">Этот параметр применяется только к конечным точкам типа ExternalEndpoints или NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="afa93-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="afa93-124">Этот параметр необходимо указать при перена указании метода маршрутизировать трафик производительности.</span><span class="sxs-lookup"><span data-stu-id="afa93-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="afa93-125">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="afa93-125">Specify an Azure region name.</span></span>
<span data-ttu-id="afa93-126">Полный список регионов Azure см. в области Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.)</span><span class="sxs-lookup"><span data-stu-id="afa93-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="afa93-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="afa93-127">-EndpointStatus</span></span>
<span data-ttu-id="afa93-128">Определяет состояние конечной точки.</span><span class="sxs-lookup"><span data-stu-id="afa93-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="afa93-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="afa93-129">Valid values are:</span></span> 

- <span data-ttu-id="afa93-130">Включено</span><span class="sxs-lookup"><span data-stu-id="afa93-130">Enabled</span></span> 
- <span data-ttu-id="afa93-131">Отключено</span><span class="sxs-lookup"><span data-stu-id="afa93-131">Disabled</span></span> 

<span data-ttu-id="afa93-132">Если состояние включено, конечная точка переназначна на состояние "Состояние конечной точки" и включена в способ маршрутинга трафика.</span><span class="sxs-lookup"><span data-stu-id="afa93-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="afa93-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="afa93-133">-GeoMapping</span></span>
<span data-ttu-id="afa93-134">Список регионов, которые были назначены данной конечной точке при использовании метода маршрутинга для географических данных.</span><span class="sxs-lookup"><span data-stu-id="afa93-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="afa93-135">Полный список принятых значений можно получить в документации Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="afa93-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="afa93-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="afa93-136">-MinChildEndpoints</span></span>
<span data-ttu-id="afa93-137">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="afa93-137">Specify an Azure region name.</span></span>
<span data-ttu-id="afa93-138">Полный список регионов Azure см. в области Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (.)</span><span class="sxs-lookup"><span data-stu-id="afa93-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="afa93-139">-Name</span><span class="sxs-lookup"><span data-stu-id="afa93-139">-Name</span></span>
<span data-ttu-id="afa93-140">Указывает имя конечной точки Диспетчера трафика, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa93-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="afa93-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="afa93-141">-Priority</span></span>
<span data-ttu-id="afa93-142">Определяет приоритет, который Диспетчер трафика назначает конечной точке.</span><span class="sxs-lookup"><span data-stu-id="afa93-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="afa93-143">Этот параметр используется только в том случае, если в профиле Диспетчера трафика настроен метод маршрутинга "Приоритет трафика".</span><span class="sxs-lookup"><span data-stu-id="afa93-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="afa93-144">Допустимые значения — это integers from 1–1000.</span><span class="sxs-lookup"><span data-stu-id="afa93-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="afa93-145">Нижние значения представляют более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="afa93-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="afa93-146">При указании приоритета необходимо указать приоритеты для всех конечных точек в профиле, и две конечные точки не могут иметь одинаковое значение приоритета.</span><span class="sxs-lookup"><span data-stu-id="afa93-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="afa93-147">Если приоритеты не указаны, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с одной (1), в том порядке, в который перечислены конечные точки профиля.</span><span class="sxs-lookup"><span data-stu-id="afa93-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="afa93-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="afa93-148">-ProfileName</span></span>
<span data-ttu-id="afa93-149">Имя профиля Диспетчера трафика, к которому этот cmdlet добавляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="afa93-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="afa93-150">Чтобы получить профиль, используйте New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="afa93-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="afa93-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa93-151">-ResourceGroupName</span></span>
<span data-ttu-id="afa93-152">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afa93-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="afa93-153">Этот cmdlet создает конечную точку Диспетчера трафика в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="afa93-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="afa93-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="afa93-154">-SubnetMapping</span></span>
<span data-ttu-id="afa93-155">Список диапазонов адресов или подсетей, которые были назначены этой конечной точке при использовании метода маршрутизации трафика "Подсеть".</span><span class="sxs-lookup"><span data-stu-id="afa93-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="afa93-156">-Target</span><span class="sxs-lookup"><span data-stu-id="afa93-156">-Target</span></span>
<span data-ttu-id="afa93-157">Указывает полное имя DNS конечной точки.</span><span class="sxs-lookup"><span data-stu-id="afa93-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="afa93-158">Диспетчер трафика возвращает это значение в ответах DNS, когда направляет трафик в эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="afa93-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="afa93-159">Укажите этот параметр только для типа конечной точки ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="afa93-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="afa93-160">Для других типов конечных точек укажите вместо этого параметр *TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="afa93-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="afa93-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="afa93-161">-TargetResourceId</span></span>
<span data-ttu-id="afa93-162">Определяет ИД ресурса конечного ресурса.</span><span class="sxs-lookup"><span data-stu-id="afa93-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="afa93-163">Укажите этот параметр только для типов конечных точек AzureEndpoint и NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="afa93-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="afa93-164">Для типа конечной точки ExternalEndpoint вместо этого укажите *целевой* параметр.</span><span class="sxs-lookup"><span data-stu-id="afa93-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="afa93-165">-Type</span><span class="sxs-lookup"><span data-stu-id="afa93-165">-Type</span></span>
<span data-ttu-id="afa93-166">Тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="afa93-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="afa93-167">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="afa93-167">Valid values are:</span></span> 

- <span data-ttu-id="afa93-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="afa93-168">AzureEndpoints</span></span>
- <span data-ttu-id="afa93-169">Внешниеendpoints</span><span class="sxs-lookup"><span data-stu-id="afa93-169">ExternalEndpoints</span></span>
- <span data-ttu-id="afa93-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="afa93-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="afa93-171">-Weight</span><span class="sxs-lookup"><span data-stu-id="afa93-171">-Weight</span></span>
<span data-ttu-id="afa93-172">Определяет вес, который Диспетчер трафика назначает конечной точке.</span><span class="sxs-lookup"><span data-stu-id="afa93-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="afa93-173">Допустимые значения — это integers from 1–1000.</span><span class="sxs-lookup"><span data-stu-id="afa93-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="afa93-174">Значение по умолчанию — 1 (1).</span><span class="sxs-lookup"><span data-stu-id="afa93-174">The default value is one (1).</span></span>
<span data-ttu-id="afa93-175">Этот параметр используется только в том случае, если профиль диспетчера трафика настроен с помощью маршрутизируемых методов взвешного трафика.</span><span class="sxs-lookup"><span data-stu-id="afa93-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="afa93-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa93-176">CommonParameters</span></span>
<span data-ttu-id="afa93-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa93-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa93-178">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa93-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa93-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afa93-179">INPUTS</span></span>

### <span data-ttu-id="afa93-180">Нет</span><span class="sxs-lookup"><span data-stu-id="afa93-180">None</span></span>

## <span data-ttu-id="afa93-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afa93-181">OUTPUTS</span></span>

### <span data-ttu-id="afa93-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afa93-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="afa93-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afa93-183">NOTES</span></span>

## <span data-ttu-id="afa93-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afa93-184">RELATED LINKS</span></span>

[<span data-ttu-id="afa93-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afa93-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afa93-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afa93-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afa93-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afa93-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afa93-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="afa93-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="afa93-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="afa93-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="afa93-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afa93-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afa93-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="afa93-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


