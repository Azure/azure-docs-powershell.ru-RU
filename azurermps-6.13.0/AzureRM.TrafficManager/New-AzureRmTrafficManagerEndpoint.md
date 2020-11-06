---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 79b3b6bc1097e28a0d11c7c5a44a5b0b80b4718b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558160"
---
# <span data-ttu-id="d9b8c-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9b8c-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d9b8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b8c-103">Создает конечную точку в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9b8c-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9b8c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b8c-106">Командлет **New-AzureRmTrafficManagerEndpoint** создает конечную точку в профиле диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="d9b8c-107">Этот командлет фиксирует каждую новую конечную точку в службе диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="d9b8c-108">Чтобы добавить несколько конечных точек к локальному объекту профиля диспетчера трафика и внести изменения в одну операцию, используйте командлет Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="d9b8c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9b8c-109">EXAMPLES</span></span>

### <span data-ttu-id="d9b8c-110">Пример 1: создание внешней конечной точки для профиля</span><span class="sxs-lookup"><span data-stu-id="d9b8c-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="d9b8c-111">Эта команда создает внешнюю конечную точку с именем Contoso в профиле с именем ContosoProfile в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d9b8c-112">Пример 2: создание конечной точки Azure для профиля</span><span class="sxs-lookup"><span data-stu-id="d9b8c-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="d9b8c-113">Эта команда создает конечную точку Azure с именем Contoso в профиле с именем ContosoProfile в группе ресурсов ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="d9b8c-114">Конечная точка Azure указывает на веб-приложение Azure, ИД которого Azure Resource Manager предоставляется путем URI в *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="d9b8c-115">В команде не указан параметр *EndpointLocation* , так как ресурс веб-приложения предоставляет расположение.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="d9b8c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9b8c-116">PARAMETERS</span></span>

### <span data-ttu-id="d9b8c-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="d9b8c-117">-CustomHeader</span></span>
<span data-ttu-id="d9b8c-118">Список имен настраиваемых заголовков и пар значений для пробных запросов.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="d9b8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b8c-119">-DefaultProfile</span></span>
<span data-ttu-id="d9b8c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b8c-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="d9b8c-121">-EndpointLocation</span></span>
<span data-ttu-id="d9b8c-122">Указывает расположение конечной точки для использования в методе маршрутизации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="d9b8c-123">Этот параметр применим только к конечным точкам типа ExternalEndpoints или NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="d9b8c-124">Этот параметр необходимо указывать при использовании метода маршрутизации трафика производительности.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="d9b8c-125">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-125">Specify an Azure region name.</span></span>
<span data-ttu-id="d9b8c-126">Полный список областей Azure см. в разделе регионы Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="d9b8c-126">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="d9b8c-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="d9b8c-127">-EndpointStatus</span></span>
<span data-ttu-id="d9b8c-128">Задает состояние конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="d9b8c-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d9b8c-129">Valid values are:</span></span> 

- <span data-ttu-id="d9b8c-130">Включаем</span><span class="sxs-lookup"><span data-stu-id="d9b8c-130">Enabled</span></span> 
- <span data-ttu-id="d9b8c-131">Отключает</span><span class="sxs-lookup"><span data-stu-id="d9b8c-131">Disabled</span></span> 

<span data-ttu-id="d9b8c-132">Если состояние включено, конечная точка проверяется на предмет работоспособности конечной точки и включена в метод маршрутизации трафика.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="d9b8c-133">-Геосоответствие</span><span class="sxs-lookup"><span data-stu-id="d9b8c-133">-GeoMapping</span></span>
<span data-ttu-id="d9b8c-134">Список регионов, сопоставленных с этой конечной точкой, при использовании метода маршрутизации для географического трафика.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="d9b8c-135">Полный список приемлемых значений можно найти в документации диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="d9b8c-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="d9b8c-136">-MinChildEndpoints</span></span>
<span data-ttu-id="d9b8c-137">Укажите имя региона Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-137">Specify an Azure region name.</span></span>
<span data-ttu-id="d9b8c-138">Полный список областей Azure см. в разделе регионы Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="d9b8c-138">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="d9b8c-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9b8c-139">-Name</span></span>
<span data-ttu-id="d9b8c-140">Указывает имя конечной точки диспетчера трафика, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d9b8c-141">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="d9b8c-141">-Priority</span></span>
<span data-ttu-id="d9b8c-142">Задает приоритет, назначаемый диспетчером трафика конечной точке.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="d9b8c-143">Этот параметр используется только в том случае, если в профиле диспетчера трафика указан метод маршрутизации трафика приоритета.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="d9b8c-144">Допустимые значения — целые числа от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="d9b8c-145">Более низкие значения представляют более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="d9b8c-146">Если указан приоритет, необходимо задать приоритеты для всех конечных точек в профиле, но ни одна из двух конечных точек не может иметь одинаковое значение приоритета.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="d9b8c-147">Если вы не укажете приоритеты, диспетчер трафика назначает конечным точкам значения приоритетов по умолчанию, начиная с единицы (1), в порядке, в котором в профиле указаны конечные точки.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="d9b8c-148">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="d9b8c-148">-ProfileName</span></span>
<span data-ttu-id="d9b8c-149">Указывает имя профиля диспетчера трафика, с которым этот командлет добавляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="d9b8c-150">Чтобы получить профиль, используйте командлеты New-AzureRmTrafficManagerProfile или Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-150">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="d9b8c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b8c-151">-ResourceGroupName</span></span>
<span data-ttu-id="d9b8c-152">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d9b8c-153">Этот командлет создает конечную точку диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9b8c-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="d9b8c-154">-SubnetMapping</span></span>
<span data-ttu-id="d9b8c-155">Список диапазонов адресов или подсетей, сопоставленных с этой конечной точкой, при использовании метода маршрутизации трафика ̃Subnetâ \ \ ђcustom \ \ ђcustom™.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-155">The list of address ranges or subnets mapped to this endpoint when using the â€˜Subnetâ€™ traffic routing method.</span></span>

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

### <span data-ttu-id="d9b8c-156">-Target</span><span class="sxs-lookup"><span data-stu-id="d9b8c-156">-Target</span></span>
<span data-ttu-id="d9b8c-157">Указывает полное DNS-имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="d9b8c-158">Диспетчер трафика возвращает это значение в ответах DNS, когда он направляет трафик на эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="d9b8c-159">Указывайте этот параметр только для типа конечной точки ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="d9b8c-160">Для других типов конечных точек укажите вместо него параметр *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="d9b8c-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="d9b8c-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d9b8c-161">-TargetResourceId</span></span>
<span data-ttu-id="d9b8c-162">Указывает идентификатор ресурса для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="d9b8c-163">Указывайте этот параметр только для типов конечных точек AzureEndpoints и NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="d9b8c-164">Для типа конечной точки ExternalEndpoints вместо него укажите *конечный* параметр.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="d9b8c-165">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="d9b8c-165">-Type</span></span>
<span data-ttu-id="d9b8c-166">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="d9b8c-167">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="d9b8c-167">Valid values are:</span></span> 

- <span data-ttu-id="d9b8c-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d9b8c-168">AzureEndpoints</span></span>
- <span data-ttu-id="d9b8c-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d9b8c-169">ExternalEndpoints</span></span>
- <span data-ttu-id="d9b8c-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d9b8c-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="d9b8c-171">-Weight</span><span class="sxs-lookup"><span data-stu-id="d9b8c-171">-Weight</span></span>
<span data-ttu-id="d9b8c-172">Определяет вес, который диспетчер трафика назначает конечной точке.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="d9b8c-173">Допустимые значения — целые числа от 1 до 1000.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="d9b8c-174">Значение по умолчанию — единица (1).</span><span class="sxs-lookup"><span data-stu-id="d9b8c-174">The default value is one (1).</span></span>
<span data-ttu-id="d9b8c-175">Этот параметр используется только в том случае, если профиль диспетчера трафика настроен с помощью метода маршрутизации для взвешенного трафика.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="d9b8c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b8c-176">CommonParameters</span></span>
<span data-ttu-id="d9b8c-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b8c-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b8c-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b8c-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9b8c-179">INPUTS</span></span>

### <span data-ttu-id="d9b8c-180">Ничего</span><span class="sxs-lookup"><span data-stu-id="d9b8c-180">None</span></span>
<span data-ttu-id="d9b8c-181">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d9b8c-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9b8c-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9b8c-182">OUTPUTS</span></span>

### <span data-ttu-id="d9b8c-183">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9b8c-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d9b8c-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9b8c-184">NOTES</span></span>

## <span data-ttu-id="d9b8c-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9b8c-185">RELATED LINKS</span></span>

[<span data-ttu-id="d9b8c-186">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9b8c-186">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d9b8c-187">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9b8c-187">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d9b8c-188">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9b8c-188">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d9b8c-189">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d9b8c-189">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d9b8c-190">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d9b8c-190">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="d9b8c-191">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9b8c-191">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d9b8c-192">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d9b8c-192">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


