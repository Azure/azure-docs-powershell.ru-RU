---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 26e759256f5641f1e38553b8a2db4ab444c2aa53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009475"
---
# <span data-ttu-id="7c0c8-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c0c8-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="7c0c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0c8-103">Добавляет правило фильтрации маршрутов в фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="7c0c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7c0c8-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c0c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c0c8-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0c8-106">Новый Add-AzRouteFilterRuleConfig добавляет правило фильтра маршрутов в фильтр маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="7c0c8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7c0c8-107">EXAMPLES</span></span>

### <span data-ttu-id="7c0c8-108">Пример 1. Добавление правила фильтрации маршрутов в фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="7c0c8-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="7c0c8-109">Первая команда получает фильтр маршрутов с именем routefilter01 с помощью Get-AzRouteFilter командлета.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="7c0c8-110">Команда сохраняет фильтр в переменной $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="7c0c8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c0c8-111">PARAMETERS</span></span>

### <span data-ttu-id="7c0c8-112">-Access</span><span class="sxs-lookup"><span data-stu-id="7c0c8-112">-Access</span></span>
<span data-ttu-id="7c0c8-113">Определяет доступ к правилу фильтра маршрутов. Допустимые значения — "Запретить" или "Разрешить".</span><span class="sxs-lookup"><span data-stu-id="7c0c8-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0c8-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="7c0c8-114">-CommunityList</span></span>
<span data-ttu-id="7c0c8-115">Список значений сообщества, по которые фильтр маршрутов будет фильтроваться по</span><span class="sxs-lookup"><span data-stu-id="7c0c8-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0c8-116">-DefaultProfile</span></span>
<span data-ttu-id="7c0c8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c0c8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7c0c8-118">-Force</span></span>
<span data-ttu-id="7c0c8-119">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="7c0c8-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7c0c8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7c0c8-120">-Name</span></span>
<span data-ttu-id="7c0c8-121">Имя правила фильтра маршрутов, которое нужно добавить в фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="7c0c8-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c0c8-122">-RouteFilter</span></span>
<span data-ttu-id="7c0c8-123">Определяет фильтр маршрутов, к которому этот cmdlet добавляет правило фильтрации маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0c8-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="7c0c8-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="7c0c8-125">Определяет тип правила фильтрации маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="7c0c8-126">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="7c0c8-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0c8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c0c8-127">-Confirm</span></span>
<span data-ttu-id="7c0c8-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c0c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c0c8-129">-WhatIf</span></span>
<span data-ttu-id="7c0c8-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c0c8-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c0c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0c8-132">CommonParameters</span></span>
<span data-ttu-id="7c0c8-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c0c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0c8-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c0c8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0c8-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c0c8-135">INPUTS</span></span>

### <span data-ttu-id="7c0c8-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c0c8-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7c0c8-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7c0c8-137">OUTPUTS</span></span>

### <span data-ttu-id="7c0c8-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c0c8-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7c0c8-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7c0c8-139">NOTES</span></span>
<span data-ttu-id="7c0c8-140">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="7c0c8-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7c0c8-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c0c8-141">RELATED LINKS</span></span>

[<span data-ttu-id="7c0c8-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c0c8-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7c0c8-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c0c8-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7c0c8-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c0c8-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7c0c8-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7c0c8-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="7c0c8-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c0c8-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="7c0c8-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c0c8-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="7c0c8-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c0c8-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="7c0c8-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7c0c8-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
