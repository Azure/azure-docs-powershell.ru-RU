---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3cd01d2e9bb3673e2c0e42ea43418c9601796a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567581"
---
# <span data-ttu-id="817cf-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="817cf-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="817cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="817cf-102">SYNOPSIS</span></span>
<span data-ttu-id="817cf-103">Добавляет правило фильтра маршрутов к фильтру маршрутов.</span><span class="sxs-lookup"><span data-stu-id="817cf-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="817cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="817cf-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="817cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="817cf-105">DESCRIPTION</span></span>
<span data-ttu-id="817cf-106">Командлет Add-AzureRmRouteFilterRuleConfig добавляет правило фильтра маршрутов в фильтр маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="817cf-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="817cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="817cf-107">EXAMPLES</span></span>

### <span data-ttu-id="817cf-108">--------------------------Пример 1: Добавление правила фильтра маршрутов в фильтр маршрута--------------------------</span><span class="sxs-lookup"><span data-stu-id="817cf-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
<span data-ttu-id="817cf-109">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="817cf-109">@{paragraph=PS C:\\\>}</span></span>















```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="817cf-110">Первая команда получает фильтр маршрутов с именем routefilter01 с помощью командлета Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="817cf-110">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="817cf-111">Команда сохраняет фильтр в переменной $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="817cf-111">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="817cf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="817cf-112">PARAMETERS</span></span>

### <span data-ttu-id="817cf-113">-Доступ</span><span class="sxs-lookup"><span data-stu-id="817cf-113">-Access</span></span>
<span data-ttu-id="817cf-114">Задает доступ к правилу фильтра маршрутов, допустимые значения — Deny или Allow.</span><span class="sxs-lookup"><span data-stu-id="817cf-114">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="817cf-115">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="817cf-115">-CommunityList</span></span>
<span data-ttu-id="817cf-116">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="817cf-116">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="817cf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="817cf-117">-Force</span></span>
<span data-ttu-id="817cf-118">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="817cf-118">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="817cf-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="817cf-119">-Name</span></span>
<span data-ttu-id="817cf-120">Указывает имя правила фильтра маршрутов, которое нужно добавить в фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="817cf-120">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="817cf-121">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="817cf-121">-RouteFilter</span></span>
<span data-ttu-id="817cf-122">Указывает фильтр маршрутов, к которому этот командлет добавляет правило фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="817cf-122">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="817cf-123">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="817cf-123">-RouteFilterRuleType</span></span>
<span data-ttu-id="817cf-124">Указывает тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="817cf-124">Specifies the route filter rule type.</span></span>
<span data-ttu-id="817cf-125">Допустимые значения: Community</span><span class="sxs-lookup"><span data-stu-id="817cf-125">Valid values are: Community</span></span>

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

### <span data-ttu-id="817cf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="817cf-126">-Confirm</span></span>
<span data-ttu-id="817cf-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="817cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="817cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="817cf-128">-WhatIf</span></span>
<span data-ttu-id="817cf-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="817cf-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="817cf-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="817cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="817cf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817cf-131">-DefaultProfile</span></span>
<span data-ttu-id="817cf-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="817cf-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="817cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817cf-133">CommonParameters</span></span>
<span data-ttu-id="817cf-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="817cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817cf-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="817cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817cf-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="817cf-136">INPUTS</span></span>

### <span data-ttu-id="817cf-137">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="817cf-137">PSRouteFilter</span></span>
<span data-ttu-id="817cf-138">Параметр "RouteFilter" принимает значение типа "PSRouteFilter" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="817cf-138">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="817cf-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="817cf-139">OUTPUTS</span></span>

### <span data-ttu-id="817cf-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="817cf-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="817cf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="817cf-141">NOTES</span></span>
<span data-ttu-id="817cf-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="817cf-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="817cf-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="817cf-143">RELATED LINKS</span></span>

[<span data-ttu-id="817cf-144">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="817cf-144">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="817cf-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="817cf-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="817cf-146">New-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="817cf-146">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="817cf-147">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="817cf-147">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="817cf-148">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="817cf-148">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="817cf-149">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="817cf-149">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

