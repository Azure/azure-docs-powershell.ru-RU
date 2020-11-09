---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249889"
---
# <span data-ttu-id="b5996-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5996-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b5996-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5996-102">SYNOPSIS</span></span>
<span data-ttu-id="b5996-103">Добавляет правило фильтра маршрутов к фильтру маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b5996-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="b5996-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5996-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5996-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5996-105">DESCRIPTION</span></span>
<span data-ttu-id="b5996-106">Командлет Add-AzRouteFilterRuleConfig добавляет правило фильтра маршрутов в фильтр маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="b5996-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="b5996-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5996-107">EXAMPLES</span></span>

### <span data-ttu-id="b5996-108">Пример 1: Добавление правила фильтра маршрутов к фильтру маршрутов</span><span class="sxs-lookup"><span data-stu-id="b5996-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="b5996-109">Первая команда получает фильтр маршрутов с именем routefilter01 с помощью командлета Get-AzRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="b5996-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="b5996-110">Команда сохраняет фильтр в переменной $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="b5996-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="b5996-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5996-111">PARAMETERS</span></span>

### <span data-ttu-id="b5996-112">-Доступ</span><span class="sxs-lookup"><span data-stu-id="b5996-112">-Access</span></span>
<span data-ttu-id="b5996-113">Задает доступ к правилу фильтра маршрутов, допустимые значения — Deny или Allow.</span><span class="sxs-lookup"><span data-stu-id="b5996-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="b5996-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="b5996-114">-CommunityList</span></span>
<span data-ttu-id="b5996-115">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="b5996-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="b5996-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5996-116">-DefaultProfile</span></span>
<span data-ttu-id="b5996-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5996-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5996-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b5996-118">-Force</span></span>
<span data-ttu-id="b5996-119">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="b5996-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b5996-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5996-120">-Name</span></span>
<span data-ttu-id="b5996-121">Указывает имя правила фильтра маршрутов, которое нужно добавить в фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b5996-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="b5996-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b5996-122">-RouteFilter</span></span>
<span data-ttu-id="b5996-123">Указывает фильтр маршрутов, к которому этот командлет добавляет правило фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b5996-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="b5996-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b5996-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="b5996-125">Указывает тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b5996-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="b5996-126">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="b5996-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="b5996-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5996-127">-Confirm</span></span>
<span data-ttu-id="b5996-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5996-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5996-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5996-129">-WhatIf</span></span>
<span data-ttu-id="b5996-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5996-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5996-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5996-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5996-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5996-132">CommonParameters</span></span>
<span data-ttu-id="b5996-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5996-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5996-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5996-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5996-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5996-135">INPUTS</span></span>

### <span data-ttu-id="b5996-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b5996-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b5996-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5996-137">OUTPUTS</span></span>

### <span data-ttu-id="b5996-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b5996-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b5996-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5996-139">NOTES</span></span>
<span data-ttu-id="b5996-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="b5996-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b5996-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5996-141">RELATED LINKS</span></span>

[<span data-ttu-id="b5996-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5996-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b5996-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5996-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b5996-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5996-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b5996-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5996-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b5996-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b5996-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b5996-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b5996-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b5996-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b5996-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b5996-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b5996-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)