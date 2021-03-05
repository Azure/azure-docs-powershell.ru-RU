---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: a3180cd693ae4c234656ba5d0812900ce8c308b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998133"
---
# <span data-ttu-id="c824b-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="c824b-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="c824b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c824b-102">SYNOPSIS</span></span>
<span data-ttu-id="c824b-103">Создание или обновление пользовательского поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="c824b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c824b-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c824b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c824b-105">DESCRIPTION</span></span>
<span data-ttu-id="c824b-106">Создание или обновление пользовательского поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="c824b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c824b-107">EXAMPLES</span></span>

### <span data-ttu-id="c824b-108">Пример 1. Создание пользовательского поставщика</span><span class="sxs-lookup"><span data-stu-id="c824b-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="c824b-109">Создание пользовательского поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="c824b-109">Create a custom resource provider</span></span>

### <span data-ttu-id="c824b-110">Пример 2. Создание пользовательского поставщика с связи</span><span class="sxs-lookup"><span data-stu-id="c824b-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="c824b-111">Создайте пользовательского поставщика с маршрутом для его объединений.</span><span class="sxs-lookup"><span data-stu-id="c824b-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="c824b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c824b-112">PARAMETERS</span></span>

### <span data-ttu-id="c824b-113">-Action</span><span class="sxs-lookup"><span data-stu-id="c824b-113">-Action</span></span>
<span data-ttu-id="c824b-114">Список действий, которые реализует настраиваемый поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="c824b-115">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств ACTION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c824b-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c824b-116">-AsJob</span></span>
<span data-ttu-id="c824b-117">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c824b-117">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c824b-118">-DefaultProfile</span></span>
<span data-ttu-id="c824b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c824b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c824b-120">-Location</span></span>
<span data-ttu-id="c824b-121">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="c824b-121">Resource location</span></span>

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

### <span data-ttu-id="c824b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c824b-122">-Name</span></span>
<span data-ttu-id="c824b-123">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c824b-124">-NoWait</span></span>
<span data-ttu-id="c824b-125">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c824b-125">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c824b-126">-ResourceGroupName</span></span>
<span data-ttu-id="c824b-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="c824b-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c824b-128">-ResourceType</span></span>
<span data-ttu-id="c824b-129">Список типов ресурсов, которые реализует настраиваемый поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="c824b-130">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств RESOURCETYPE и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c824b-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c824b-131">-SubscriptionId</span></span>
<span data-ttu-id="c824b-132">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c824b-132">The Azure subscription ID.</span></span>
<span data-ttu-id="c824b-133">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="c824b-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="c824b-134">-Tag</span></span>
<span data-ttu-id="c824b-135">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="c824b-135">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-136">-Проверка</span><span class="sxs-lookup"><span data-stu-id="c824b-136">-Validation</span></span>
<span data-ttu-id="c824b-137">Список проверки, которые нужно выполнить по запросам поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="c824b-138">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств проверки и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c824b-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c824b-139">-Confirm</span></span>
<span data-ttu-id="c824b-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c824b-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c824b-141">-WhatIf</span></span>
<span data-ttu-id="c824b-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c824b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c824b-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c824b-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c824b-144">CommonParameters</span></span>
<span data-ttu-id="c824b-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c824b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c824b-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c824b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c824b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c824b-147">INPUTS</span></span>

## <span data-ttu-id="c824b-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c824b-148">OUTPUTS</span></span>

### <span data-ttu-id="c824b-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="c824b-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="c824b-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c824b-150">NOTES</span></span>

<span data-ttu-id="c824b-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c824b-151">ALIASES</span></span>

<span data-ttu-id="c824b-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c824b-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c824b-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c824b-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c824b-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c824b-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c824b-155">ACTION <ICustomRpActionRouteDefinition[]>: список действий, которые реализует поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="c824b-156">`Endpoint <String>`: URI конечной точки определения маршрутов, к который настраиваемый поставщик ресурсов будет запрашивать у поставщика прокси-серверов.</span><span class="sxs-lookup"><span data-stu-id="c824b-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="c824b-157">Это может быть в виде плоского URI (например, ' ') или может указывать маршрут по маршруту https://testendpoint/ (например, ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="c824b-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="c824b-158">`Name <String>`: имя определения маршрута.</span><span class="sxs-lookup"><span data-stu-id="c824b-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="c824b-159">Оно становится именем расширения ARM (например, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="c824b-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="c824b-160">`[RoutingType <ActionRouting?>]`. Типы маршрутов, поддерживаемые для запросов на действие.</span><span class="sxs-lookup"><span data-stu-id="c824b-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="c824b-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: список типов ресурсов, которые реализует настраиваемый поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="c824b-162">`Endpoint <String>`: URI конечной точки определения маршрутов, к который настраиваемый поставщик ресурсов будет запрашивать у поставщика прокси-серверов.</span><span class="sxs-lookup"><span data-stu-id="c824b-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="c824b-163">Это может быть в виде плоского URI (например, ' ') или может указывать маршрут по маршруту https://testendpoint/ (например, ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="c824b-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="c824b-164">`Name <String>`: имя определения маршрута.</span><span class="sxs-lookup"><span data-stu-id="c824b-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="c824b-165">Оно становится именем расширения ARM (например, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="c824b-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="c824b-166">`[RoutingType <ResourceTypeRouting?>]`. Типы маршрутов, поддерживаемые для запросов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="c824b-167">VALIDATION <ICustomRpValidations[]>: список проверки для запуска по запросам поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c824b-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="c824b-168">`Specification <String>`: ссылка на спецификацию проверки.</span><span class="sxs-lookup"><span data-stu-id="c824b-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="c824b-169">Спецификацию необходимо разо всех raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="c824b-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="c824b-170">`[ValidationType <ValidationType?>]`. Тип проверки, которая будет запускаться для запроса на соответствие.</span><span class="sxs-lookup"><span data-stu-id="c824b-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="c824b-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c824b-171">RELATED LINKS</span></span>

