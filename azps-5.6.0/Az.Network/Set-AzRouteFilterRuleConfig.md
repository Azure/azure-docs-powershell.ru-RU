---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: a58a6216d49539d4fc40f9c9131a335f7a31b87f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990895"
---
# <span data-ttu-id="76cdf-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76cdf-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="76cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="76cdf-103">Изменяет правило фильтрации маршрутов фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="76cdf-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="76cdf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76cdf-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76cdf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76cdf-105">DESCRIPTION</span></span>
<span data-ttu-id="76cdf-106">**Cmdlet Set-AzRouteFilterRuleConfig** изменяет правило фильтрации маршрутов фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="76cdf-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="76cdf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76cdf-107">EXAMPLES</span></span>

### <span data-ttu-id="76cdf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76cdf-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="76cdf-109">Первая команда получает фильтр маршрутов с именем RouteFilter01 и сохраняет его в $rf переменной.</span><span class="sxs-lookup"><span data-stu-id="76cdf-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="76cdf-110">Вторая команда изменяет правило фильтра маршрутов с именем "Правило01" и сохраняет обновленный фильтр маршрутов в $rf переменной.</span><span class="sxs-lookup"><span data-stu-id="76cdf-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="76cdf-111">Третья команда сохраняет обновленный фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="76cdf-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="76cdf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76cdf-112">PARAMETERS</span></span>

### <span data-ttu-id="76cdf-113">-Access</span><span class="sxs-lookup"><span data-stu-id="76cdf-113">-Access</span></span>
<span data-ttu-id="76cdf-114">Тип доступа правила.</span><span class="sxs-lookup"><span data-stu-id="76cdf-114">The access type of the rule.</span></span>
<span data-ttu-id="76cdf-115">Возможные значения: "Разрешить", "Запретить"</span><span class="sxs-lookup"><span data-stu-id="76cdf-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="76cdf-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="76cdf-116">-CommunityList</span></span>
<span data-ttu-id="76cdf-117">Список значений сообщества, по которые фильтр маршрутов будет фильтроваться по</span><span class="sxs-lookup"><span data-stu-id="76cdf-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="76cdf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cdf-118">-DefaultProfile</span></span>
<span data-ttu-id="76cdf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76cdf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76cdf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="76cdf-120">-Force</span></span>
<span data-ttu-id="76cdf-121">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="76cdf-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="76cdf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="76cdf-122">-Name</span></span>
<span data-ttu-id="76cdf-123">Имя правила фильтрации маршрутов</span><span class="sxs-lookup"><span data-stu-id="76cdf-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="76cdf-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="76cdf-124">-RouteFilter</span></span>
<span data-ttu-id="76cdf-125">Маршрутизатор</span><span class="sxs-lookup"><span data-stu-id="76cdf-125">The RouteFilter</span></span>

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

### <span data-ttu-id="76cdf-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="76cdf-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="76cdf-127">Тип правила фильтрации маршрутов.</span><span class="sxs-lookup"><span data-stu-id="76cdf-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="76cdf-128">Возможные значения: Community</span><span class="sxs-lookup"><span data-stu-id="76cdf-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="76cdf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76cdf-129">-Confirm</span></span>
<span data-ttu-id="76cdf-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76cdf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76cdf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76cdf-131">-WhatIf</span></span>
<span data-ttu-id="76cdf-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76cdf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76cdf-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76cdf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76cdf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cdf-134">CommonParameters</span></span>
<span data-ttu-id="76cdf-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76cdf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cdf-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76cdf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cdf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76cdf-137">INPUTS</span></span>

### <span data-ttu-id="76cdf-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76cdf-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="76cdf-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76cdf-139">OUTPUTS</span></span>

### <span data-ttu-id="76cdf-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76cdf-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="76cdf-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76cdf-141">NOTES</span></span>

## <span data-ttu-id="76cdf-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76cdf-142">RELATED LINKS</span></span>

[<span data-ttu-id="76cdf-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76cdf-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76cdf-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76cdf-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76cdf-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76cdf-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76cdf-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="76cdf-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="76cdf-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76cdf-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="76cdf-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76cdf-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="76cdf-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76cdf-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="76cdf-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="76cdf-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
