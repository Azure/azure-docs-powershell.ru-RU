---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915250"
---
# <span data-ttu-id="3c7bc-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c7bc-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="3c7bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c7bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7bc-103">Добавляет правило фильтра маршрутов к фильтру маршрутов.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c7bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c7bc-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c7bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7bc-105">DESCRIPTION</span></span>
<span data-ttu-id="3c7bc-106">Командлет Add-AzureRmRouteFilterRuleConfig добавляет правило фильтра маршрутов в фильтр маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="3c7bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c7bc-107">EXAMPLES</span></span>

### <span data-ttu-id="3c7bc-108">--------------------------Пример 1: Добавление правила фильтра маршрутов в фильтр маршрута--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c7bc-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="3c7bc-109">Первая команда получает фильтр маршрутов с именем routefilter01 с помощью командлета Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="3c7bc-110">Команда сохраняет фильтр в переменной $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="3c7bc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c7bc-111">PARAMETERS</span></span>

### <span data-ttu-id="3c7bc-112">-Доступ</span><span class="sxs-lookup"><span data-stu-id="3c7bc-112">-Access</span></span>
<span data-ttu-id="3c7bc-113">Задает доступ к правилу фильтра маршрутов, допустимые значения — Deny или Allow.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="3c7bc-114">-CommunityList</span></span>
<span data-ttu-id="3c7bc-115">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="3c7bc-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7bc-116">-DefaultProfile</span></span>
<span data-ttu-id="3c7bc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3c7bc-118">-Force</span></span>
<span data-ttu-id="3c7bc-119">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="3c7bc-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3c7bc-120">-Name</span></span>
<span data-ttu-id="3c7bc-121">Указывает имя правила фильтра маршрутов, которое нужно добавить в фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3c7bc-122">-RouteFilter</span></span>
<span data-ttu-id="3c7bc-123">Указывает фильтр маршрутов, к которому этот командлет добавляет правило фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="3c7bc-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="3c7bc-125">Указывает тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="3c7bc-126">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="3c7bc-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c7bc-127">-Confirm</span></span>
<span data-ttu-id="3c7bc-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c7bc-129">-WhatIf</span></span>
<span data-ttu-id="3c7bc-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c7bc-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7bc-132">CommonParameters</span></span>
<span data-ttu-id="3c7bc-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7bc-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7bc-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c7bc-135">INPUTS</span></span>

### <span data-ttu-id="3c7bc-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3c7bc-136">PSRouteFilter</span></span>
<span data-ttu-id="3c7bc-137">Параметр "RouteFilter" принимает значение типа "PSRouteFilter" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="3c7bc-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7bc-138">OUTPUTS</span></span>

### <span data-ttu-id="3c7bc-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3c7bc-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3c7bc-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c7bc-140">NOTES</span></span>
<span data-ttu-id="3c7bc-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="3c7bc-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3c7bc-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c7bc-142">RELATED LINKS</span></span>

[<span data-ttu-id="3c7bc-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c7bc-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="3c7bc-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3c7bc-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)







[<span data-ttu-id="3c7bc-145">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3c7bc-145">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

