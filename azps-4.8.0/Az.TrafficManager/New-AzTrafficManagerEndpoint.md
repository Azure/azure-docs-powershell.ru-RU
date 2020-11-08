---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079318"
---
# <span data-ttu-id="8a7e9-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a7e9-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="8a7e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7e9-103">Создает конечную точку в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="8a7e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a7e9-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a7e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a7e9-105">DESCRIPTION</span></span>
<span data-ttu-id="8a7e9-106">Командлет **New-AzTrafficManagerEndpoint** создает конечную точку в профиле диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="8a7e9-107">Этот командлет фиксирует каждую новую конечную точку в службе диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="8a7e9-108">Чтобы добавить несколько конечных точек к локальному объекту профиля диспетчера трафика и внести изменения в одну операцию, используйте командлет Add-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="8a7e9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a7e9-109">EXAMPLES</span></span>

### <span data-ttu-id="8a7e9-110">Пример 1: создание внешней конечной точки для профиля</span><span class="sxs-lookup"><span data-stu-id="8a7e9-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="8a7e9-111">Эта команда создает внешнюю конечную точку с именем Contoso в профиле с именем ContosoProfile в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="8a7e9-112">Пример 2: создание конечной точки Azure для профиля</span><span class="sxs-lookup"><span data-stu-id="8a7e9-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="8a7e9-113">Эта команда создает конечную точку Azure с именем Contoso в профиле с именем ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="8a7e9-114">Конечная точка Azure указывает на веб-приложение Azure, ИД которого Azure Resource Manager предоставляется путем URI в *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="8a7e9-115">В команде не указан параметр *EndpointLocation* , так как ресурс веб-приложения предоставляет расположение.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="8a7e9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a7e9-116">PARAMETERS</span></span>

### <span data-ttu-id="8a7e9-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="8a7e9-117">-CustomHeader</span></span>
<span data-ttu-id="8a7e9-118">Список имен настраиваемых заголовков и пар значений для пробных запросов.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="8a7e9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7e9-119">-DefaultProfile</span></span>
<span data-ttu-id="8a7e9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a7e9-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="8a7e9-121">-EndpointLocation</span></span>
<span data-ttu-id="8a7e9-122">Указывает расположение конечной точки для использования в методе маршрутизации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="8a7e9-123">Этот параметр применим только к конечным точкам типа ExternalEndpoints или NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="8a7e9-124">Этот параметр необходимо указывать при использовании метода маршрутизации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="8a7e9-125">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-125">Specify an Azure region name.</span></span>
<span data-ttu-id="8a7e9-126">Полный список областей Azure см. в разделе регионы Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="8a7e9-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="8a7e9-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="8a7e9-127">-EndpointStatus</span></span>
<span data-ttu-id="8a7e9-128">Задает состояние конечной точки.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="8a7e9-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8a7e9-129">Valid values are:</span></span> 

- <span data-ttu-id="8a7e9-130">Включаем</span><span class="sxs-lookup"><span data-stu-id="8a7e9-130">Enabled</span></span> 
- <span data-ttu-id="8a7e9-131">Отключает</span><span class="sxs-lookup"><span data-stu-id="8a7e9-131">Disabled</span></span> 

<span data-ttu-id="8a7e9-132">Если состояние включено, конечная точка проверяется на предмет работоспособности конечной точки и включена в метод маршрутизации трафика.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="8a7e9-133">-Геосоответствие</span><span class="sxs-lookup"><span data-stu-id="8a7e9-133">-GeoMapping</span></span>
<span data-ttu-id="8a7e9-134">Список регионов, сопоставленных с этой конечной точкой, при использовании метода маршрутизации для географического трафика.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="8a7e9-135">Полный список приемлемых значений можно найти в документации диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="8a7e9-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="8a7e9-136">-MinChildEndpoints</span></span>
<span data-ttu-id="8a7e9-137">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-137">Specify an Azure region name.</span></span>
<span data-ttu-id="8a7e9-138">Полный список областей Azure см. в разделе регионы Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="8a7e9-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="8a7e9-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a7e9-139">-Name</span></span>
<span data-ttu-id="8a7e9-140">Указывает имя конечной точки диспетчера трафика, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8a7e9-141">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="8a7e9-141">-Priority</span></span>
<span data-ttu-id="8a7e9-142">Задает приоритет, назначаемый диспетчером трафика конечной точке.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="8a7e9-143">Этот параметр используется только в том случае, если в профиле диспетчера трафика указан метод маршрутизации трафика приоритета.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="8a7e9-144">Допустимые значения — целые числа от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="8a7e9-145">Более низкие значения представляют более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="8a7e9-146">Если указан приоритет, необходимо задать приоритеты для всех конечных точек в профиле, но ни одна из двух конечных точек не может иметь одинаковое значение приоритета.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="8a7e9-147">Если вы не укажете приоритеты, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с единицы (1), в порядке, в котором в профиле указаны конечные точки.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="8a7e9-148">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="8a7e9-148">-ProfileName</span></span>
<span data-ttu-id="8a7e9-149">Указывает имя профиля диспетчера трафика, с которым этот командлет добавляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="8a7e9-150">Чтобы получить профиль, используйте командлеты New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="8a7e9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a7e9-151">-ResourceGroupName</span></span>
<span data-ttu-id="8a7e9-152">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8a7e9-153">Этот командлет создает конечную точку диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8a7e9-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="8a7e9-154">-SubnetMapping</span></span>
<span data-ttu-id="8a7e9-155">Список диапазонов адресов или подсетей, сопоставленных с этой конечной точкой при использовании метода маршрутизации трафика "подсеть".</span><span class="sxs-lookup"><span data-stu-id="8a7e9-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="8a7e9-156">-Target</span><span class="sxs-lookup"><span data-stu-id="8a7e9-156">-Target</span></span>
<span data-ttu-id="8a7e9-157">Указывает полное DNS-имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="8a7e9-158">Диспетчер трафика возвращает это значение в ответах DNS, когда он направляет трафик на эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="8a7e9-159">Указывайте этот параметр только для типа конечной точки ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="8a7e9-160">Для других типов конечных точек укажите вместо него параметр *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="8a7e9-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="8a7e9-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8a7e9-161">-TargetResourceId</span></span>
<span data-ttu-id="8a7e9-162">Указывает идентификатор ресурса для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="8a7e9-163">Указывайте этот параметр только для типов конечных точек AzureEndpoints и NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="8a7e9-164">Для типа конечной точки ExternalEndpoints вместо него укажите *конечный* параметр.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="8a7e9-165">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="8a7e9-165">-Type</span></span>
<span data-ttu-id="8a7e9-166">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="8a7e9-167">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8a7e9-167">Valid values are:</span></span> 

- <span data-ttu-id="8a7e9-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="8a7e9-168">AzureEndpoints</span></span>
- <span data-ttu-id="8a7e9-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="8a7e9-169">ExternalEndpoints</span></span>
- <span data-ttu-id="8a7e9-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="8a7e9-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="8a7e9-171">-Weight</span><span class="sxs-lookup"><span data-stu-id="8a7e9-171">-Weight</span></span>
<span data-ttu-id="8a7e9-172">Определяет вес, который диспетчер трафика назначает конечной точке.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="8a7e9-173">Допустимые значения — целые числа от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="8a7e9-174">Значение по умолчанию — единица (1).</span><span class="sxs-lookup"><span data-stu-id="8a7e9-174">The default value is one (1).</span></span>
<span data-ttu-id="8a7e9-175">Этот параметр используется только в том случае, если профиль диспетчера трафика настроен с помощью метода маршрутизации для взвешенного трафика.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="8a7e9-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7e9-176">CommonParameters</span></span>
<span data-ttu-id="8a7e9-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a7e9-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7e9-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a7e9-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7e9-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a7e9-179">INPUTS</span></span>

### <span data-ttu-id="8a7e9-180">Ничего</span><span class="sxs-lookup"><span data-stu-id="8a7e9-180">None</span></span>

## <span data-ttu-id="8a7e9-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a7e9-181">OUTPUTS</span></span>

### <span data-ttu-id="8a7e9-182">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a7e9-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8a7e9-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a7e9-183">NOTES</span></span>

## <span data-ttu-id="8a7e9-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a7e9-184">RELATED LINKS</span></span>

[<span data-ttu-id="8a7e9-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a7e9-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8a7e9-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a7e9-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8a7e9-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a7e9-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8a7e9-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8a7e9-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8a7e9-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8a7e9-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="8a7e9-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a7e9-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8a7e9-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8a7e9-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


