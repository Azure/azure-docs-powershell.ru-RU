---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314450"
---
# <span data-ttu-id="7e5cb-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="7e5cb-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="7e5cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5cb-103">Создает или обновляет настраиваемый поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="7e5cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e5cb-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7e5cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="7e5cb-106">Создает или обновляет настраиваемый поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="7e5cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e5cb-107">EXAMPLES</span></span>

### <span data-ttu-id="7e5cb-108">Пример 1: Создание настраиваемого поставщика</span><span class="sxs-lookup"><span data-stu-id="7e5cb-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="7e5cb-109">Создание настраиваемого поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="7e5cb-109">Create a custom resource provider</span></span>

### <span data-ttu-id="7e5cb-110">Пример 2: Создание настраиваемого поставщика с ассоциациями</span><span class="sxs-lookup"><span data-stu-id="7e5cb-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="7e5cb-111">Создание настраиваемого поставщика с маршрутом для ассоциаций настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="7e5cb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e5cb-112">PARAMETERS</span></span>

### <span data-ttu-id="7e5cb-113">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="7e5cb-113">-Action</span></span>
<span data-ttu-id="7e5cb-114">Список действий, реализуемых настраиваемым поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="7e5cb-115">Для конструирования щелкните раздел "Заметки" для получения свойств действия и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="7e5cb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e5cb-116">-AsJob</span></span>
<span data-ttu-id="7e5cb-117">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="7e5cb-117">Run the command as a job</span></span>

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

### <span data-ttu-id="7e5cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5cb-118">-DefaultProfile</span></span>
<span data-ttu-id="7e5cb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e5cb-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7e5cb-120">-Location</span></span>
<span data-ttu-id="7e5cb-121">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="7e5cb-121">Resource location</span></span>

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

### <span data-ttu-id="7e5cb-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e5cb-122">-Name</span></span>
<span data-ttu-id="7e5cb-123">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="7e5cb-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="7e5cb-124">-NoWait</span></span>
<span data-ttu-id="7e5cb-125">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="7e5cb-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7e5cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e5cb-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e5cb-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7e5cb-128">-ResourceType</span></span>
<span data-ttu-id="7e5cb-129">Список типов ресурсов, реализованных настраиваемым поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="7e5cb-130">Для конструирования ознакомьтесь с разделом "Заметки" для свойств RESOURCETYPE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7e5cb-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e5cb-131">-SubscriptionId</span></span>
<span data-ttu-id="7e5cb-132">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-132">The Azure subscription ID.</span></span>
<span data-ttu-id="7e5cb-133">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="7e5cb-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="7e5cb-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="7e5cb-134">-Tag</span></span>
<span data-ttu-id="7e5cb-135">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="7e5cb-135">Resource tags</span></span>

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

### <span data-ttu-id="7e5cb-136">-Проверка</span><span class="sxs-lookup"><span data-stu-id="7e5cb-136">-Validation</span></span>
<span data-ttu-id="7e5cb-137">Список проверок, которые необходимо выполнить для запросов настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="7e5cb-138">Для конструирования ознакомьтесь с разделом "Заметки" для свойств проверки и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="7e5cb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e5cb-139">-Confirm</span></span>
<span data-ttu-id="7e5cb-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e5cb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e5cb-141">-WhatIf</span></span>
<span data-ttu-id="7e5cb-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e5cb-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e5cb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5cb-144">CommonParameters</span></span>
<span data-ttu-id="7e5cb-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5cb-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e5cb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5cb-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e5cb-147">INPUTS</span></span>

## <span data-ttu-id="7e5cb-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e5cb-148">OUTPUTS</span></span>

### <span data-ttu-id="7e5cb-149">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="7e5cb-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="7e5cb-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e5cb-150">NOTES</span></span>

<span data-ttu-id="7e5cb-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="7e5cb-151">ALIASES</span></span>

<span data-ttu-id="7e5cb-152">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7e5cb-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e5cb-153">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e5cb-154">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e5cb-155">ACTION <ICustomRpActionRouteDefinition [] >: список действий, реализуемых настраиваемым поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="7e5cb-156">`Endpoint <String>`: URI конечной точки определения маршрута, на который будут запрашивать прокси-сервер для настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="7e5cb-157">Это может быть в виде плоского URI (например, " https://testendpoint/ ") или указывать на маршрут по пути (например, " https://testendpoint/{requestPath} ").</span><span class="sxs-lookup"><span data-stu-id="7e5cb-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="7e5cb-158">`Name <String>`: Имя определения маршрута.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="7e5cb-159">Оно становится именем для расширения ARM (например, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="7e5cb-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="7e5cb-160">`[RoutingType <ActionRouting?>]`: Типы маршрутизации, поддерживаемые для запросов на изменение.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="7e5cb-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: список типов ресурсов, реализованных настраиваемым поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="7e5cb-162">`Endpoint <String>`: URI конечной точки определения маршрута, на который будут запрашивать прокси-сервер для настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="7e5cb-163">Это может быть в виде плоского URI (например, " https://testendpoint/ ") или указывать на маршрут по пути (например, " https://testendpoint/{requestPath} ").</span><span class="sxs-lookup"><span data-stu-id="7e5cb-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="7e5cb-164">`Name <String>`: Имя определения маршрута.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="7e5cb-165">Оно становится именем для расширения ARM (например, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="7e5cb-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="7e5cb-166">`[RoutingType <ResourceTypeRouting?>]`: Типы маршрутизации, которые поддерживаются для запросов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="7e5cb-167">Проверка <ICustomRpValidations [] >: список проверок, которые должны выполняться в запросах настраиваемого поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="7e5cb-168">`Specification <String>`: Ссылка на спецификацию проверки.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="7e5cb-169">Спецификация должна размещаться на raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="7e5cb-170">`[ValidationType <ValidationType?>]`: Тип проверки, которая должна выполняться для соответствующего запроса.</span><span class="sxs-lookup"><span data-stu-id="7e5cb-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="7e5cb-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e5cb-171">RELATED LINKS</span></span>

