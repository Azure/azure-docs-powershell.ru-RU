---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073085"
---
# <span data-ttu-id="32561-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32561-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="32561-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32561-102">SYNOPSIS</span></span>
<span data-ttu-id="32561-103">Изменяет правило фильтра маршрутов для фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="32561-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="32561-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32561-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32561-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32561-105">DESCRIPTION</span></span>
<span data-ttu-id="32561-106">Командлет **Set-AzRouteFilterRuleConfig** изменяет правило фильтра маршрутов для фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="32561-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="32561-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32561-107">EXAMPLES</span></span>

### <span data-ttu-id="32561-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32561-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="32561-109">Первая команда получает фильтр маршрутов с именем RouteFilter01 и сохраняет его в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="32561-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="32561-110">Вторая команда изменяет правило фильтра маршрутов с именем Rule01 и сохраняет обновленный фильтр маршрутов в переменной $rf.</span><span class="sxs-lookup"><span data-stu-id="32561-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="32561-111">Третья команда сохраняет обновленный фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="32561-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="32561-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32561-112">PARAMETERS</span></span>

### <span data-ttu-id="32561-113">-Доступ</span><span class="sxs-lookup"><span data-stu-id="32561-113">-Access</span></span>
<span data-ttu-id="32561-114">Тип доступа для правила.</span><span class="sxs-lookup"><span data-stu-id="32561-114">The access type of the rule.</span></span>
<span data-ttu-id="32561-115">Возможные значения: "разрешить", "запретить"</span><span class="sxs-lookup"><span data-stu-id="32561-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="32561-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="32561-116">-CommunityList</span></span>
<span data-ttu-id="32561-117">Список значений сообщества, по которому будет фильтроваться фильтр маршрутов</span><span class="sxs-lookup"><span data-stu-id="32561-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="32561-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32561-118">-DefaultProfile</span></span>
<span data-ttu-id="32561-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32561-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32561-120">-Force</span><span class="sxs-lookup"><span data-stu-id="32561-120">-Force</span></span>
<span data-ttu-id="32561-121">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="32561-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32561-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32561-122">-Name</span></span>
<span data-ttu-id="32561-123">Имя правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="32561-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="32561-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-124">-RouteFilter</span></span>
<span data-ttu-id="32561-125">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-125">The RouteFilter</span></span>

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

### <span data-ttu-id="32561-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="32561-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="32561-127">Тип правила фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="32561-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="32561-128">Возможные значения: "сообщество"</span><span class="sxs-lookup"><span data-stu-id="32561-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="32561-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32561-129">-Confirm</span></span>
<span data-ttu-id="32561-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32561-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32561-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32561-131">-WhatIf</span></span>
<span data-ttu-id="32561-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32561-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32561-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32561-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32561-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32561-134">CommonParameters</span></span>
<span data-ttu-id="32561-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32561-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32561-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32561-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32561-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32561-137">INPUTS</span></span>

### <span data-ttu-id="32561-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="32561-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32561-139">OUTPUTS</span></span>

### <span data-ttu-id="32561-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="32561-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="32561-141">NOTES</span></span>

## <span data-ttu-id="32561-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32561-142">RELATED LINKS</span></span>

[<span data-ttu-id="32561-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32561-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32561-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32561-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32561-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32561-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32561-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32561-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="32561-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="32561-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="32561-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="32561-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32561-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
